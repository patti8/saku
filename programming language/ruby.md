# Ruby
A dynamic, open source programming language with a focus on simplicity and productivity. It has an elegant syntax that is natural to read and easy to write. [more](https://www.ruby-lang.org/en/about/)
- [download page](https://www.ruby-lang.org/en/downloads/)

## 1. Interaction with JSON File 
resouces from [here](https://hackernoon.com/ruby-how-to-readwrite-json-file-a23h3vxa).
### a). Install gem JSON
copy perintah ```gem install json``` pada terminal untuk menambahkan library tersebut ke local library ruby kita.
### b). Write/Read JSON File
buka file ruby, misalnya ```main.rb```, dan import library ```json``` yang telah diinstall sebelumnya. Kemudian tambahkan perintah berikut pada baris pertama:
```ruby
require 'json'
```
setelah itu coba akses file json yang terletak bersamaan dengan file ```main.rb```, dan buka file tersebut dengan perintah berikut:
```ruby
require 'json'

file = File.read('./file.json')

data_hash = JSON.parse(file)
puts data_hash
```
silahkah jalan perintah tersebut dengan ```ruby main.rb```

## Method

### Hapus yang kosong pada array
```ruby
params[:member_ids].reject(&:blank?)
```