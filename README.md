## Açıklama

Uygulama, PostgreSQL veritabanı üzerinde öğrenci ekler ve listeler. Docker kullanılarak konteynerize edilmiştir ve PgAdmin kullanılarak görsel bir arayüz üzerinden erişim sağlayabilirsiniz.

### Kullanılan Teknolojiler:
- Node.js: Uygulama geliştirme için kullanılmıştır.
- Express.js: Web sunucusu oluşturmak ve API'ler sağlamak için kullanılmıştır.
- Docker: Uygulamanın konteynerize edilmesi ve taşınabilirliğinin sağlanması için kullanılmıştır.
- PgAdmin: PostgreSQL veritabanı yönetimi için görsel bir arayüz sağlamak için kullanılmıştır.

 Bilgisayarınızda node.js'in yüklü olması gerekmektedir. 

İndirilmesi gereken paketler:
  
`
 $ npm install nodemon
`

PostgreSQL paketi:

`
 $ npm install pg
`

## Proje Kurulumu

```bash
 git clone https://github.com/feyzabakir/devops-odev.git
```
Visual Studio Code'da bir terminal açın

```bash
docker build -t db-app .
```

```bash
docker run -d -p 3000:3000 --name app db-app
```

```bash
docker stop app
```

```bash
docker rm app
```

```bash
docker-compose up -d
```

Running için tekrar

```bash
docker-compose up -d
```

Şimdi `localhost:5050` ile pgAdmin sayfasına ulaşabilirsiniz.

docker-compose.yaml dosyasındaki pgadmin enviromentlarına göre giriş yapabilirsiniz. (`PGADMIN_DEFAULT_EMAIL` ve `PGADMIN_DEFAULT_PASSWORD`)

Daha sonra database'i oluşturup içerisine Name, Surname ve Age sütunlarını ekleyiniz.

Postman üzerinden ekleme ve listeleme işlemlerini gerçekleştirebilirsiniz.

GET: `localhost:3000/student`

POST: `localhost:3000/student/add`  body -> raw alanından JSON formatında verilerinizi ekleyebilirsiniz.


