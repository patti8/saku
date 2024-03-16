# Ruby On Rails
![rails](https://upload.wikimedia.org/wikipedia/commons/thumb/6/62/Ruby_On_Rails_Logo.svg/1200px-Ruby_On_Rails_Logo.svg.png)
Rails is a web application development framework written in the Ruby programming language. It is designed to make programming web applications easier by making assumptions about what every developer needs to get started. It allows you to write less code while accomplishing more than many other languages and frameworks. [more](https://guides.rubyonrails.org/getting_started.html)


### 1. Rails Command
- Cara menjalankan server : 
```bash
rails s
```

jika menggunakan port atau ip public dapat menggunakan perintah dibawah ini:
```
rails s -b 0.0.0.0 -p 53012
```

### 2. Stimulus for Rails
Stimulus for Rails makes it easy to use this modest framework with both import-mapped and JavaScript-bundled apps. It relies on either importmap-rails to make Stimulus available via ESM or a Node-capable Rails (like via jsbundling-rails) to include Stimulus in the bundle. Make sure to install one of these first!. [more](https://github.com/hotwired/stimulus-rails)

#### A). 3 langkah install stimulus
   1. Tambahkan gem stimulus-rails pada Gemfile: ```gem 'stimulus-rails'```
   2. kemudian jalankan ```./bin/bundle install``` di terminal
   3. kemudian jalankan ```./bin/rails stimulus:install```.
    Ada juga cara manual yang dapat dilakukan untuk lengkap dapat dilihat pada [link dokumentasinya](https://github.com/hotwired/stimulus-rails)

Hal utama dalam stimulus, yaitu controller, action dan target. Controller berfungsi sebagai class utama yang menampung fungsi yang akan dilakukan terhadap suatu objek tertentu. Action sebagai method untuk menjalan perintah yang diinginkan atau perubahan yang akan dilakukan terhadap objek tersebut. Dan target contoh sederhana yaitu objek yang akan kita ubah.

##### B). Controller
cara penggunaan stimulus controller dengan meletakan atribut ```data-controller``` ke dalam tag HTML
```html
<div data-controller="model" ></div>
```

##### C). Target
cara penggunaan target dengan meletakan atribut ```data-namacontroller-target``` ke dalam tag HTML
```html
<div data-controller="hello">
    <input data-hello-target="name" type="text">
</div>
```

#####  D). Action
cara penggunaan action dengan meletakan atribut ```data-action="namacontroller#namaaction"``` ke dalam tag HTML
```html
<div data-controller="hello">
    <input data-action="hello#say" type="text">
</div>
```
##### References for Basic to Learn: 
- https://www.w3schools.com/jsref/dom_obj_all.asp
- https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model


### 3. Best Rails Gem for Vscode Extension
- ```gem install htmlbeautifier ``` for erb linter, and for extension VSCODE you must to install **ERB Formatter/Beautify** 
- ```gem 'rubocop', require: false``` for ruby linter, and for extension VSCODE you must to install **rubocop**

### 4. FORM HELPER
untuk implementasi tag form HTML di [Ruby on Rails](https://guides.rubyonrails.org/getting_started.html), contohnya seperti : 
```ruby
<%= form_for @person do |f| %>
  <%= f.label :first_name %>:
  <%= f.text_field :first_name %><br />

  <%= f.label :last_name %>:
  <%= f.text_field :last_name %><br />

  <%= f.submit %>
<% end %>
```

yang akan menjadi seperti ini kalau di HTML : 
```html 
<form action="/people" class="new_person" id="new_person" method="post">
  <input name="authenticity_token" type="hidden" value="NrOp5bsjoLRuK8IW5+dQEYjKGUJDe7TQoZVvq95Wteg=" />
  <label for="person_first_name">First name</label>:
  <input id="person_first_name" name="person[first_name]" type="text" /><br />

  <label for="person_last_name">Last name</label>:
  <input id="person_last_name" name="person[last_name]" type="text" /><br />

  <input name="commit" type="submit" value="Create Person" />
</form>
```
referensi lanjutannya pada link [ActionView::Helpers::FormHelper](https://api.rubyonrails.org/v5.1/classes/ActionView/Helpers/FormHelper.html).


### 5. Render Partial
**render partial** merupakan metode untuk merender sub template. untuk lebih lanjutnya bisa ke [link ini](https://api.rubyonrails.org/classes/ActionView/PartialRenderer.html)

- contohnya kita merender template ```_account.html.erb``` yang berada dengan file utama, misalnya template tersebut akan dirender pada file ```index.html.erb``` yang diletakan path path ``accounts/index.html.erb

```erb
<%= render 'account' %>
```

### 6. Stimulus & Slim Select 2.0
referensinya dari :
 - [slimselectjs.com](https://slimselectjs.com) 
 - [Ruby on Rails #94 Rails 7 Select Box with Search using Slim-Select
](https://slimselectjs.com)


