substring_index（“待截取有用部分的字符串”，“截取数据依据的字符”，截取字符的位置N）

```sql
案例1：

//根据自己设定的顺序进行排序
select id,substring_index('11000,10000,10001,3602,3600',id,1)  from test 
where id in (10000,3602,3600,10001,11000)          
order by substring_index('11000,10000,10001,3602,3600',id,1) ;


案例2:

SELECT SUBSTRING_INDEX(‘15,151,152,16’, ’ , ’ , 1); //结果是15  //以第一个逗号为分割截取

SELECT SUBSTRING_INDEX(‘15,151,152,16’, ’ , ’ , 2); //结果是15,151  //以第二个逗号为分割截取

SELECT SUBSTRING_INDEX(‘15,151,152,16’, ’ , ’ , -1); //结果是16   //从后面开始算第一个逗号

案例3：

substring_index( ‘1,3,2,4,6,5’, id, 1 ) 获取每个id前面的数据，比如：id=1 对于数据“1,3,2,4,6,5”，没有数据sub_data=‘’

id=2 对于数据“1,3,2,4,6,5”，sub_data=‘1,3,’

ORDER BY substring_index( ‘1,3,2,4,6,5’, id, 1 );  会根据你的 “1,3,2,4,6,5” 的顺序进行排序

```

[案例1结果](https://blog.csdn.net/z457181562/article/details/82968702)。
