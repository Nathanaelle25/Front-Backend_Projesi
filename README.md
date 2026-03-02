📘 BEUBlog – Full Stack Blog Platformu
📌 Proje Hakkında

BEUBlog, [buraya projenin amacını yaz] amacıyla geliştirilmiş modern bir full-stack blog platformudur.

Proje kapsamında kullanıcıların blog yazıları oluşturabilmesi, düzenleyebilmesi ve yönetebilmesi hedeflenmiştir. Sistem rol tabanlı yetkilendirme ve JWT kimlik doğrulama mekanizması ile güvenli hale getirilmiştir.

🎯 Proje Amacı

Bu projenin temel amacı:

[Amaç 1]

[Amaç 2]

[Amaç 3]

👉 Buraya 3 akademik amaç yazmanı istiyorum.
Örneğin: full-stack mimariyi öğrenmek, REST API geliştirmek, JWT kullanımı vb.

🛠️ Kullanılan Teknolojiler
Frontend

React 18

Vite

React Router DOM

Axios

React Quill

Lucide React

Backend

Node.js

Express.js

MongoDB

Mongoose

JWT (JSON Web Token)

Multer

bcryptjs

DevOps

Docker

Docker Compose

Nginx

✨ Özellikler

Kullanıcı kayıt ve giriş sistemi

JWT tabanlı kimlik doğrulama

Rol tabanlı yetkilendirme (Admin / Kullanıcı)

Blog yazısı oluşturma, düzenleme ve silme

Kategori yönetimi

Yazı beğenme sistemi

Admin onaylı içerik moderasyonu

Görsel yükleme desteği

Karanlık / Aydınlık tema desteği

🏗️ Sistem Mimarisi

Proje iki ana bileşenden oluşmaktadır:

Frontend (Client-Side)
React tabanlı SPA yapısında geliştirilmiştir. REST API üzerinden backend ile iletişim kurmaktadır.

Backend (Server-Side)
Express.js ile geliştirilmiş RESTful API servisidir. MongoDB veritabanı ile veri yönetimi sağlanmaktadır.

👉 Sana soru:
Frontend ile backend arasındaki iletişim hangi protokol üzerinden oluyor? (Tek kelime cevap)

⚙️ Kurulum
Docker ile Kurulum
git clone <repo-url>
cd beublog
export JWT_SECRET=guclu-bir-secret-key
docker compose up -d
Manuel Kurulum
Backend
cd backend
npm install
npm start
Frontend
cd frontend
npm install
npm run dev
🔌 API Endpointleri
Kimlik Doğrulama

POST /api/auth/register

POST /api/auth/login

GET /api/auth/me

Yazılar

GET /api/posts

POST /api/posts

PUT /api/posts/:id

DELETE /api/posts/:id

Kategoriler

GET /api/categories

POST /api/categories

📁 Proje Yapısı
beublog/
│
├── backend/
├── frontend/
├── docker-compose.yml
📷 Ekran Görüntüleri

