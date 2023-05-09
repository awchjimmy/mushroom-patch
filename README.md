# mushroom-patch
A Custom Application File Format for Storing Mushroom Patches

### Table Schema

|TMS||||||
|----|----|----|----|----|----|
|id|filename|from_version|to_version|sha256|content|
|INTEGER|TEXT|INTEGER|INTEGER|TEXT|BLOB|

### See Also
- [SQLite As An Application File Format](https://sqlite.org/appfileformat.html)
