# Stuff I can never remember...

## git
### sort branches by last commit:

* git for-each-ref --sort=-committerdate refs/heads/
* git branch --sort=-committerdate    (ver 2.7.0+)

## oracle
### reset password:
ALTER USER me IDENTIFIED BY my_new_password

### date vs. timestamp
Date: date and time values down to the second (e.g. 1/1/10 13:01:01)
TimeStamp: an extension of date, includes date and time values down to the fractional second (e.g. 1/1/10 13:01:01:0009)

#### inserting
INSERT INTO TABLE_NAME(DATE_FIELD)
VALUES(to_date('2016-01-01 01:01:01', 'yyyy-mm-dd hh24:mi:ss'))

#### { chars | strings | clobs }
100 left-most characters
* select substr(message, -100) from alerts order by alertid;
100 right-most characters
* select substr(message, 100) from alerts order by alertid;

JDBC inserting a clob value from a clob field using a prepared statment:
```java
Clob srcClob = (Clob)value;
Clob tgtClob = stmt.getConnection().createClob();
tgtClob.setString(1, srcClob.getSubString(1, (int)srcClob.length()));
stmt.setClob(icol, tgtClob);
```
