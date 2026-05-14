# 🛒 E-Commerce REST API

ASP.NET Core Web API ile geliştirilmiş, modern bir e-ticaret uygulamasının backend servisi.

## 🚀 Teknolojiler

- **ASP.NET Core 8** — Web API framework
- **Entity Framework Core** — ORM
- **MSSQL** — Veritabanı
- **JWT** — Authentication & Authorization
- **Cloudinary** — Resim depolama
- **BCrypt** — Şifre hashleme
- **Swagger** — API dokümantasyonu

## 📌 Özellikler

### 🔐 Authentication
- JWT tabanlı kimlik doğrulama
- Role bazlı yetkilendirme (Admin / Müşteri)
- BCrypt ile güvenli şifre hashleme
- Token expire kontrolü

### 📦 Ürün Yönetimi
- Ürün CRUD işlemleri
- Otomatik slug üretimi (SEO dostu URL)
- Cloudinary ile resim yükleme/silme
- Soft delete (arşivleme) sistemi
- Kategori bazlı filtreleme
- Arama özelliği

### 🗂️ Kategori Yönetimi
- Kategori CRUD işlemleri
- Otomatik slug üretimi
- Kategoriye bağlı ürün yönetimi

### 🛒 Sepet & Sipariş
- Kullanıcıya özel sepet yönetimi
- Stok kontrolü
- Sipariş oluşturma
- Sipariş iptal (stok iadesi ile)
- Sipariş durum takibi

### ❤️ Favoriler
- Kullanıcıya özel favori listesi
- Toggle (ekle/çıkar) sistemi

### 👤 Kullanıcı Yönetimi
- Kayıt & Giriş
- Profil güncelleme
- Müşteri listeleme (Admin)

## ⚙️ Kurulum

### Gereksinimler
- .NET 8 SDK
- MSSQL Server
- Cloudinary hesabı

### 1. Repoyu klonla
```bash
git clone https://github.com/fatmaozkan1dvlp/ecommerce-api.git
cd ecommerce-api
```

### 2. `appsettings.json` ayarlarını tamamla
```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=...;Database=ECommerceDb;Trusted_Connection=True;"
  },
  "Jwt": {
    "Key": "en-az-32-karakterlik-gizli-anahtar",
    "Issuer": "ECommerceAPI",
    "Audience": "ECommerceClient"
  },
  "Cloudinary": {
    "CloudName": "your_cloud_name",
    "ApiKey": "your_api_key",
    "ApiSecret": "your_api_secret"
  },
  "AdminSeed": {
    "AdSoyad": "Admin",
    "EMail": "admin@example.com",
    "Sifre": "Adminsifre!"
  }
}
```

### 3. Migration uygula
```bash
dotnet ef database update
```

### 4. Çalıştır
```bash
dotnet run
```


## 👩‍💻 Geliştirici

Bu proje backend geliştirme pratiği amacıyla yapılmıştır.
