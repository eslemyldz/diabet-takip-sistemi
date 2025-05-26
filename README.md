
# Diyabet Takip Sistemi 🩺💻

Bu proje, diyabet hastalarının sağlık verilerini takip edebilmeleri ve doktorlar tarafından değerlendirilebilmesi amacıyla geliştirilmiş web tabanlı bir sistemdir. Sistem; glisemik indeks, insülin direnci, diyabet tipi, laboratuvar sonuçları, ilaç reçeteleri ve randevu yönetimi gibi sağlık bileşenlerini içerir.

---

## 🌐 Genel Özellikler

- Kullanıcı ve doktor giriş sistemi
- Hasta IP'sine göre oturum yönetimi
- Glisemik veri, laboratuvar sonucu, reçete ve randevu takibi
- Doktorların hastaları inceleyip ilaç yazabilmesi ve randevu atayabilmesi
- Web tarayıcısı üzerinden çalışan Flask tabanlı uygulama

---

## 👤 Kullanıcı Rolleri

### 🧑‍⚕️ Doktor
- Hasta laboratuvar sonuçlarını ve reçetelerini görüntüleme
- Yeni ilaç reçetesi yazma (insülin ve hap tipleriyle)
- Hastalarına randevu atama ve düzenleme

### 🧑‍💻 Hasta
- Sisteme giriş yaparak:
  - Laboratuvar sonuçlarını ve reçetelerini görüntüleme
  - Doktor seçerek randevu oluşturma
  - Kendi glisemik bilgilerini takip etme

---

## 🛠️ Kullanılan Teknolojiler

| Katman     | Teknoloji                  |
|------------|----------------------------|
| Backend    | Python (Flask)             |
| Frontend   | HTML, CSS, JavaScript      |
| Veritabanı | SQLite (veya MySQL desteği)|
| Stil       | `style.css`, `panel.css`, `recete.css` |

---

## 📁 Proje Yapısı

```
diyabet-takip-sistemi/
│
├── app.py                       # Flask backend uygulaması
│
├── templates/
│   ├── login.html              # Giriş ekranı
│   ├── hasta_panel.html        # Hasta kontrol paneli
│   ├── hasta_randevu.html      # Randevu alma formu
│   ├── randevu_panel.html      # Doktor randevu paneli
│   ├── lab_sonuclari.html      # Laboratuvar sonuçları görünümü
│   ├── ilac_recete.html        # Doktor reçete ekranı (interaktif)
│   └── ilaç_recete.html        # Alternatif reçete ekranı
│
├── static/
│   ├── style.css               # Genel stil dosyası
│   ├── panel.css               # Panel tasarımı
│   └── recete.css              # Reçete ekranı tasarımı
│
└── README.md                   # Proje dokümantasyonu (bu dosya)
```

---

## 🚀 Kurulum ve Çalıştırma

Aşağıdaki adımları izleyerek projeyi kendi bilgisayarınızda çalıştırabilirsiniz:

### 1. Depoyu klonlayın
```bash
git clone https://github.com/kullaniciadi/diyabet-takip-sistemi.git
cd diyabet-takip-sistemi
```

### 2. Gerekli Python paketlerini yükleyin
```bash
pip install -r requirements.txt
```

> Eğer `requirements.txt` yoksa aşağıdaki paketleri manuel yükleyebilirsiniz:
```bash
pip install Flask
```

### 3. Uygulamayı çalıştırın
```bash
python app.py
```

### 4. Tarayıcıdan açın
```
http://localhost:5000
```

---

## 🔐 Oturum Yönetimi

Kullanıcı ve doktor girişleri, IP adresleri üzerinden kontrol edilerek benzersiz oturumlar yönetilir. Her giriş kullanıcıya özel hasta veya doktor panelini yükler.

---

## 🧪 Laboratuvar Sonuçları

Doktorlar, hastaların geçmişte girdiği laboratuvar sonuçlarını filtreleyebilir ve türüne göre sınıflandırabilir (örneğin: Kan Şekeri, HbA1c, İnsülin vs.).

---

## 💊 Reçete Yönetimi

- Doktorlar hastalara **hap veya insülin** tipi ilaçlar yazabilir.
- Dozaj bilgisi, insülin tipi, açıklamalar sisteme eklenebilir.
- Reçeteler kullanıcıya göre listelenebilir.

---

## 📅 Randevu Sistemi

- Hastalar sistemdeki doktorlardan uygun olanı seçerek randevu alabilir.
- Randevu saatleri sistem tarafından kontrol edilir.
- Doktorlar tüm randevuları randevu panelinden görebilir.

---

## 📌 Notlar

- Flask içinde `url_for()` ile dinamik yönlendirme yapılmıştır.
- Her rol için ayrı HTML şablonları hazırlanmıştır.
- CSS ile responsive ve kullanıcı dostu arayüz tasarımı yapılmıştır.
- Veriler IP bazlı kullanıcı eşleştirmesiyle ilişkilendirilmiştir.

---

## 📝 Lisans

Bu proje eğitim ve sosyal fayda amaçlı geliştirilmiştir. Açık kaynaklı kullanım için uygundur, ancak ticari amaçla kullanımı için geliştiricinin izni gereklidir.

---
