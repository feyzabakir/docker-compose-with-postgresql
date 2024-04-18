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
docker-compose up 
```

Running için 

```bash
docker-compose up -d
```

Şimdi `localhost:5050` ile pgAdmin sayfasına ulaşabilirsiniz.

docker-compose.yaml dosyasındaki pgadmin enviromentlarına göre giriş yapabilirsiniz. (`PGADMIN_DEFAULT_EMAIL` ve `PGADMIN_DEFAULT_PASSWORD`)

Daha sonra database'i oluşturup içerisine Name, Surname ve Age sütunlarını ekleyiniz.

Postman üzerinden ekleme ve listeleme işlemlerini gerçekleştirebilirsiniz.

GET: `localhost:3000/student`

POST: `localhost:3000/student/add`  body -> raw alanından JSON formatında verilerinizi ekleyebilirsiniz.

## Resimler

![1](https://github.com/feyzabakir/devops-odev/assets/120409251/9bb1f717-b507-4e10-b029-50fa962456c2)

![2](https://github.com/feyzabakir/devops-odev/assets/120409251/5db0a897-5c71-45fe-b92e-db00cf4885ca)

![3](https://github.com/feyzabakir/devops-odev/assets/120409251/84fdffce-6851-4f48-8a01-75465db913fc)

![4](https://github.com/feyzabakir/devops-odev/assets/120409251/9c39709f-d109-4b3f-b75d-7f22ceb00e0f)

![5](https://github.com/feyzabakir/devops-odev/assets/120409251/17c5c311-9c02-427c-9da6-e9f402ff1721)

## Video

<a href="https://github.com/feyzabakir/devops-odev/issues/1">Video Link</a>
