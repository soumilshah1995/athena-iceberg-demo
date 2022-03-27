# athena-iceberg-demo
athena-iceberg-demo

# Youtube Video : https://www.youtube.com/watch?v=Q_bPwA5Qwb0

```
# ======================================
# Query 1 
# =======================================

CREATE TABLE iceberg_test 
(
  name string , 
  phone_numbers string ,
  city string ,
  address string ,
  date_feild string
)

LOCATION
    's3://XXXXX/data/'
TBLPROPERTIES (
    'table_type'='ICEBERG'
);

# ======================================
# Query 2
# =======================================


insert into learndb.iceberg_test (
SELECT ALL name,phone_numbers, city,address, date
FROM "learndb"."data"
)


# ======================================
# Query 3
# =======================================


delete from learndb.iceberg_test where name='Mary Bryan'


# ======================================
# Query 4
# =======================================

UPDATE   learndb.iceberg_test
SET name='soumil'
where city='Douglasburgh';
```
