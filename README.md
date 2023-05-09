# mushroom-patch
A Custom Application File Format for Storing Mushroom Patches

### Table Schema

|TMS|||||
|----|----|----|----|----|
|id|filename|from_version|to_version|content|
|INTEGER|TEXT|INTEGER|INTEGER|BLOB|

### Usage

#### Sample Input 1

```sql
SELECT filename FROM TMS ORDER BY to_version, from_version;
```

#### Sample Output 1

||filename|
|----|----|
|1|MaplePatch13to17.exe|
|2|MaplePatch17to18.exe|
|3|MaplePatch13to19.exe|

#### Sample Input 2 (Slow)

```sql
SELECT * FROM TMS ORDER BY to_version, from_version;
```

#### Sample Output 2 (Slow)

||id|filename|from_version|to_version|content|
|----|----|---|----|----|----|
|1|2|MaplePatch13to17.exe|13|17|BLOB|
|2|1|MaplePatch17to18.exe|17|18|BLOB|
|3|3|MaplePatch13to19.exe|13|19|BLOB|

### See Also
- [SQLite As An Application File Format](https://sqlite.org/appfileformat.html)
