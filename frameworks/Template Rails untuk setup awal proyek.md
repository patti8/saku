// template.rb
```ruby
# template.rb
# can be use rails new my_app -m template.rb or use github link


say "Mengatur Database: PostgreSQL"
gsub_file "Gemfile", /sqlite3/, "pg"

say "Menginstall TailwindCSS"
run "rails tailwindcss:install"

say "Menambahkan Devise untuk Autentikasi"
gem "devise"
run "bundle install"
generate "devise:install"
generate "devise User"

say "Menambahkan StimulusJS"
run "rails stimulus:install"

say "Menambahkan konfigurasi Rubocop"
file ".rubocop.yml", <<-YAML
AllCops:
  TargetRubyVersion: 3.2
  NewCops: enable
Layout/LineLength:
  Max: 120
YAML

say "Menambahkan Dockerfile"
file "Dockerfile", <<-DOCKER
FROM ruby:3.2
WORKDIR /app
COPY . .
RUN bundle install
CMD ["rails", "server", "-b", "0.0.0.0"]
DOCKER

say "Menambahkan docker-compose.yml"
file "docker-compose.yml", <<-YAML
version: '3'
services:
  db:
    image: postgres
    environment:
      POSTGRES_USER: user
      POSTGRES_PASSWORD: password
    ports:
      - "5432:5432"
  web:
    build: .
    ports:
      - "3000:3000"
    depends_on:
      - db
YAML

say "Setup awal selesai! Jalankan `rails db:create db:migrate` untuk mulai."
```
