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
