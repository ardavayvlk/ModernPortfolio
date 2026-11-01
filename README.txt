# ModernPortfolio

ModernPortfolio, C# ve ASP.NET Core MVC mimarisi kullanılarak geliştirilmiş, dinamik ve modern bir kişisel portfolyo web uygulamasıdır. Katmanlı mimarı prensiplerine (Repository & Service Pattern) uygun olarak tasarlanmış ve veri tabanı işlemleri için Dapper ORM kullanılmıştır.

---

## 🛠️ Teknolojiler ve Mimari

* **Backend:** .NET / ASP.NET Core MVC
* **Veri Erişimi (ORM):** Dapper
* **Veri Tabanı:** SQL Server / PostgreSQL
* **Front-End:** HTML5, CSS3, JavaScript, Bootstrap 5
* **Kapsayıcılık:** Docker / Docker Compose
* **Mimari:** Repository Pattern, Service Layer, ViewModels

---

## 📁 Proje Yapısı

```text
ModernPortfolio/
├── Areas/              # Yönetim (Admin) paneli modülleri
│   └── Admin/
├── Controllers/        # Kullanıcı arayüzü controller sınıfları
├── Models/             # Veri tabanı varlıkları (Entities)
├── Repositories/       # Veri erişim katmanı ve Dapper sorguları
├── Scripts/            # SQL veri tabanı kurulum ve Seed betikleri
├── Services/           # İş mantığı (Business Logic) katmanı
├── ViewComponents/     # Modüler UI bileşenleri
├── ViewModels/         # Ekran modelleri ve veri taşıma nesneleri
├── Views/              # Razor görünüm dosyaları
├── wwwroot/            # Statik dosyalar (CSS, JS, Görseller)
├── Dockerfile          # Docker imaj yapılandırması
└── docker-compose.yml  # Container orkestrasyonu


🚀 Kurulum ve Çalıştırma
Projeyi yerel ortamınızda çalıştırmak için aşağıdaki yöntemlerden birini tercih edebilirsiniz.


Yöntem 1: .NET CLI ile Yerel Kurulum
Ön Koşullar
.NET SDK (Sürüm 8.0 veya üzeri)

SQL Server veya PostgreSQL veri tabanı sunucusu

Adımlar
Projeyi klonlayın: git clone [https://github.com/kullanici-adi/ModernPortfolio.git](https://github.com/kullanici-adi/ModernPortfolio.git)
cd ModernPortfolio

Scripts/ dizininde bulunan .sql dosyalarını (örnek: CreateTables.sql, CreateUsersTable.sql, SeedData.sql) veri tabanı sunucunuzda sırasıyla çalıştırarak gerekli tabloları ve başlangıç verilerini oluşturun.

appsettings.json (veya appsettings.Development.json) dosyasındaki ConnectionStrings alanını kendi veri tabanı bilgilerinize göre güncelleyin:
"ConnectionStrings": {
  "DefaultConnection": "Server=YOUR_SERVER;Database=ModernPortfolioDb;Trusted_Connection=True;TrustServerCertificate=True;"
}


Bağımlılıkları yükleyin ve projeyi derleyin:
dotnet restore
dotnet build

Uygulamayı başlatın:

dotnet run


--------------------------------------------------------------------------------------------------------------------------
Yöntem 2: Docker ile Çalıştırma
Projeyi herhangi bir yerel bağımlılık kurmadan doğrudan Docker container ortamında çalıştırabilirsiniz.

Ön Koşullar
Docker Desktop

Adımlar
Docker Compose ile başlatın:

docker-compose up -d --build

Uygulamaya erişin:

Container'lar çalıştıktan sonra tarayıcınızdan http://localhost:8080 (veya compose dosyasında tanımlanan port) adresini ziyaret edebilirsiniz.

docker-compose down

⚙️ Özellikler
Dinamik İçerik Yönetimi: Projeler, yetenekler, hakkımda bilgileri ve referanslar admin paneli üzerinden güncellenebilir.

Performanslı Veri Erişimi: Dapper kullanımı sayesinde yüksek performanslı SQL sorguları.

Güvenlik: Admin paneli için yetkilendirme ve kimlik doğrulama altyapısı.

Responsive Tasarım: Mobil ve masaüstü cihazlarla tam uyumlu modern kullanıcı arayüzü.
