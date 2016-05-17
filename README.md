# mysql-escape-array
Escape arrays before putting them in mysql queries like 'where id in (3421, 6789, 6754)

```js
var mysqlEscapeArray = require('mysql-escape-array');
var names = ["bob","joe","bill","Robert' DROP TABLE Students;"];
var sql = 'select * from users where name in ' + mysqlEscapeArray(names);
console.log(sql)
//Returns: select * from users where name in ('bob','joe','bill','Robert\' DROP TABLE Students;')
