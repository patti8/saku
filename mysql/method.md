### MENGHAPUS 2 ANGKA DIBELAKANG
referensinya [disini](https://stackoverflow.com/questions/47500190/remove-last-digit-from-all-data-in-column-in-mysql)
contoh implementasinya seperti ini : 

```sql
select count  = SUBSTRING(count, 1, CHAR_LENGTH(count) - 1)
```

### LAST DAY AND FIRST DAY

```sql
     CONCAT(
    DATE_FORMAT(DATE_ADD(DATE_SUB(NOW(), INTERVAL DAYOFMONTH(NOW())-1 DAY), INTERVAL -1 MONTH), "%Y-%m-%d")
    , " sd. ",
    LAST_DAY(DATE_FORMAT(DATE_ADD(NOW(), INTERVAL -1 MONTH), "%Y-%m-%d"))
  ) as RANGE_TANGGAL
```