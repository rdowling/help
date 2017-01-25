# handy stuff

## bash (https://www.blockloop.io/mastering-bash-and-terminal)

### history
* `ctrl-r` - reverse search history (reverse-i-search)
* `ctrl-s` - forward search history (reverse-i-search)
* `ctrl-p` - previous command in history
* `ctrl-n` - next command in history

### cursor movement
* `ctrl-a` - move the cursor to the beginning of the current line
* `ctrl-e` - move the cursor to the end of the current line
* `alt-b`  - move the cursor backwards one word
* `alt-f`  - move the cursor forward one word
* `ctrl-k` - delete from cursor to the end of the line
* `ctrl-u` -  delete from cursor to the beginning of the line
* `alt-d`  - delete the word in front of the cursor
* `ctrl-w` - delete the word behind of the cursor

### processes
* `ctrl-z` - send process to background
* `ctrl-c` - kill current process

### working with files
* `less` - paged viewing with vim (ex view lots of git pending changes: `git status | less`)
* `find` - find named files (ex search curdir for file auth.py: `find . -type f -name auth.py`)

## git

### sort branches by last commit
* `git for-each-ref --sort=-committerdate refs/heads/`
* `git branch --sort=-committerdate`  - ver 2.7.0+

### list branches
* `git branch -a`  - list all branches, local & remote
* `git branch -r`  - list remote branches

## oracle
### reset password
ALTER USER me IDENTIFIED BY my_new_password

### date vs. timestamp
Date: date and time values down to the second (e.g. 1/1/10 13:01:01)
TimeStamp: an extension of date, includes date and time values down to the fractional second (e.g. 1/1/10 13:01:01:0009)

#### inserting
INSERT INTO TABLE_NAME(DATE_FIELD)
VALUES(to_date('2016-01-01 01:01:01', 'yyyy-mm-dd hh24:mi:ss'))

#### { chars | strings | clobs }
100 left-most characters
* `select substr(message, -100) from alerts order by alertid;`
100 right-most characters
* `select substr(message, 100) from alerts order by alertid;`

JDBC inserting a clob value from a clob field using a prepared statment:
```java
Clob srcClob = (Clob)value;
Clob tgtClob = stmt.getConnection().createClob();
tgtClob.setString(1, srcClob.getSubString(1, (int)srcClob.length()));
stmt.setClob(icol, tgtClob);
```


## markdown
https://guides.github.com/features/mastering-markdown/
