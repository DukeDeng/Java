spool d:\data.csv           【Spool导出文件的完整的路径，若文件已存在则打开，若文件不存在则创建并打开。在执行spool off命令前，不能对该文件进行修改保存】
spool off                      【关闭Spool语句，即结束导出操作，保存并关闭导出文件】
 
set echo off                   【执行sql脚本文件时，则只显示sql命令执行的结果，而不显示出sql命令本身】
set heading off            【只显示数据，不显示select结果的字段名。开启后，每一页数据都将增加一行列名。导出文件会增大，降低导出数据的速度，具体增大量与对速度的影响取决于pagesize参数的设置。】
set linesize 320             【设置每行记录字符长度，1个汉字占两个字符，记录长度不足用空格补齐，长度超出会换行】
set pagesize 24             【设置每页记录条数，默认值为24，设置为0时表示不分页】
set newp none              【设置查询出来的数据分多少页显示，如果需要连续的数据，中间不要出现空行就把newp设置为none，这样输出的数据行都是连续的，中间没有空行】
set newpage 1              【设置每个新页的开头的空行数，默认值为1，即每个新页开头都有1个空行】
set trimspool on            【当输出文件中的记录长度小于linesize时，删除尾随的空格】
set trimout on               【当屏幕上返回记录长度小于linesize时，删除尾随的空格】
set termout off             【执行SQL脚本时，设置屏幕不显示SQL查询的结果】
set colsep ','                   【设置字段间的分隔符，默认为空格。因为该参数影响导出性能，故不建议使用该参数，而是在Select中直接设置格式】
set underline =                     【设置字段名与数据之间的分割符，默认为’—’】
set null text                   【设置空值字段的替代字符串，text自定义】
set numwidth 12            【设置number类型字段的长度，缺省为10】
set timing on              【设置控制台显示“已用时间：XXXX”】
set feedback off           【设置不显示“已选择XX行”】
set serveroutput on        【打开oracle自带的输出方法dbms_output】
set autotrace on             【打开autotrace工具，对执行的sql进行分析】
