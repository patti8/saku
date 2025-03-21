### MENGHAPUS 2 ANGKA DIBELAKANG
referensinya [disini](https://stackoverflow.com/questions/47500190/remove-last-digit-from-all-data-in-column-in-mysql)
contoh implementasinya seperti ini : 

```sql
select count  = SUBSTRING(count, 1, CHAR_LENGTH(count) - 1)
```