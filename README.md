# Weed for .net/mono
超强跨平台轻量级ORM（无反射；缓存控制；分布式事务；万能绑定）<br/>

Weed3::源码<br/>
Weed3Demo::使用示例<br/>

占位符说明：<br/>
 $.       //表空间占位数（即数据库名）<br/>
 $fcn     //SQL函数占位符<br/>
 ?        //参数占位符<br/>
 ?...     //数组型参数占位符<br/>

网站:<br/>
 http://www.noear.org<br/>

QQ群：<br/>
 22200020<br/>
 
--------------------------------------<br/>
示例（使用代码可与java版互用）<br/>
db.table("user_info")<br/>
&nbsp;&nbsp;&nbsp;&nbsp;.where("user_id<?", 10)<br/>
&nbsp;&nbsp;&nbsp;&nbsp;.select("user_id,name,sex")<br/>
&nbsp;&nbsp;&nbsp;&nbsp;.getList&lt;UserInfoModel&gt;();<br/>

db.table("test")<br/>
&nbsp;&nbsp;&nbsp;&nbsp;.insert(new DataItem().set("log_time", "$DATE(NOW())"));<br/>

db.table("test")<br/>
&nbsp;&nbsp;&nbsp;&nbsp;.where("id IN (?...)", new int[] { 15,14,16}) //数据参数<br/>
&nbsp;&nbsp;&nbsp;&nbsp;.update(new DataItem().set("txt", "NOW()xx").set("num", 44)); <br/>
  
更多示例请参考Weed3Demo <br/>
--------------------------------------<br/>

by noear