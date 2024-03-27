# Install POSTGRESQL with Docker

-  pull ```docker images``` dengan perintah ```docker pull postgres```
- buat docker container dengan perintah dibawah ini :
```bash
docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres
```