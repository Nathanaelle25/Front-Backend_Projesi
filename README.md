WebProgramlama
📦 BEUBlog

Modern, full-stack blog platformu. React frontend ve Node.js/Express backend ile geliştirilmiş, Docker üzerinden kolayca deploy edilebilir.

🚀 Teknoloji Yığını
Frontend

React 18 + Vite

React Router DOM

React Quill (WYSIWYG editör)

Axios

Lucide React

Backend

Node.js + Express 5

MongoDB + Mongoose

JWT kimlik doğrulama

Multer (dosya yükleme)

bcryptjs (parola şifreleme)

DevOps

Docker & Docker Compose

Nginx (production frontend sunucusu)

✨ Özellikler

Kullanıcı kayıt & giriş (JWT tabanlı)

Rol tabanlı yetkilendirme (user/admin)

Blog yazısı oluşturma, düzenleme, silme

React Quill ile zengin metin editörü

Kategori sistemi (admin yönetimi)

Yazı beğenme sistemi

Admin moderasyon sistemi (yazı onay/askıya alma)

Dosya yükleme desteği (JPEG, PNG, GIF, WebP, SVG — max 10MB)

Aydınlık/Karanlık tema desteği

Tamamen Türkçe arayüz

🐳 Kurulum
1. Docker ile (Önerilen)
# Repoyu klonla
git clone <repo-url>
cd beublog

# JWT secret
export JWT_SECRET=guclu-bir-secret-key

# Servisleri çalıştır
docker compose up -d

Uygulama adresleri:

Frontend: http://localhost

Backend: http://localhost:5000

MongoDB: localhost:27017

2. Manuel Kurulum
🔧 Backend
cd backend
npm install

# .env dosyasını oluştur
echo "PORT=5000" > .env
echo "MONGODB_URI=mongodb://localhost:27017/blogdb" >> .env
echo "JWT_SECRET=guclu-bir-secret-key" >> .env

npm start
💻 Frontend
cd frontend
npm install
npm run dev
📁 Proje Yapısı
beublog/
├── docker-compose.yml
├── backend/
│   ├── server.js
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── make-admin.js
│   └── migrate-slugs.js
└── frontend/
    └── src/
        ├── App.jsx
        ├── api.js
        ├── context/
        ├── components/
        └── pages/
📡 API Endpointleri
🔐 Kimlik Doğrulama
Metot	Endpoint	Açıklama
POST	/api/auth/register	Yeni kullanıcı kaydı
POST	/api/auth/login	Giriş yapma
GET	/api/auth/me	Kullanıcı bilgisi
PUT	/api/auth/me/profile	Profil güncelleme
PUT	/api/auth/me/password	Parola değiştirme
GET	/api/auth/me/posts	Kullanıcının yazıları
📝 Yazılar
Metot	Endpoint	Açıklama
GET	/api/posts	Yazı listesi
POST	/api/posts	Yeni yazı oluştur
GET	/api/posts/by-slug/:slug	Slug ile yazı getir
PUT	/api/posts/:id	Yazı güncelle
DELETE	/api/posts/:id	Yazı sil
PUT	/api/posts/:id/like	Yazıyı beğen
PUT	/api/posts/:id/status	Yazı durum değişikliği (admin)
📂 Kategoriler
Metot	Endpoint	Açıklama
GET	/api/categories	Listele
POST	/api/categories	Ekle (admin)
DELETE	/api/categories/:id	Sil (admin)
🖼️ Dosya Yükleme
Metot	Endpoint	Açıklama
POST	/api/upload	Görsel yükle
🛠️ Yardımcı Scriptler
# Kullanıcıyı admin yap
node backend/make-admin.js

# Yazılara slug ekle (migrasyon)
node backend/migrate-slugs.js
⚙️ Ortam Değişkenleri
Değişken	Açıklama	Varsayılan
PORT	Backend portu	5000
MONGODB_URI	MongoDB bağlantısı	mongodb://localhost:27017/blogdb
JWT_SECRET	JWT imza anahtarı	zorunlu
