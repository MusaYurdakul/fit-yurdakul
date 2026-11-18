# 🏋️ Fit Yurdakul — Kişisel Veriye Dayalı Fitness Uygulaması

> 🔒 **Bu proje ticari olarak geliştirilmektedir — kaynak kodu kapalıdır.** Bu depo yalnızca tanıtım amaçlıdır. Demo veya detaylı bilgi için [iletişime geçebilirsiniz](#-i̇letişim).

Antrenman, toparlanma ve beslenmeyi tek yerde takip eden; önerilerini genel kalıplardan değil **kullanıcının kendi verisinden** üreten mobil öncelikli fitness uygulaması. Yakında mobil uygulama olarak yayında.

## ✨ Özellikler

**🏋️ Antrenman**
- Hedefe göre (kas, güç, performans) ve kilo fazına göre (bulk / cut) otomatik plan oluşturucu
- Set, tekrar ve ağırlık takibi; dinlenme sayacı, tahmini 1RM ve kişisel rekor (PR) tespiti
- **İnternet olmadan antrenman:** setler cihazda kaydedilir, bağlantı gelince senkronize edilir
- Takvim: antrenmanı atla, başka güne taşı; taşıma için akıllı gün önerisi

**📈 Kişisel öneri motoru**
- Kademeli yüklenme (progressive overload) önerileri: her öneri kanıtıyla birlikte gösterilir
- Öneriler kullanıcı onaylamadan plana uygulanmaz; kabul / ret / erteleme
- Haftalık uyum, kas grubu dengesi ve performans grafikleri

**🥗 Beslenme**
- Kalori ve makro hedefleri, kilo trendine göre kalibrasyon
- Besin arama ve **barkod okuma**, öğün kaydı (çevrimdışı da çalışır)

**❤️ Toparlanma**
- Uyku, dinlenik nabız ve günlük check-in'den **hazırlık skoru**
- Deload ve hafifletme önerileri
- Bluetooth nabız kemeriyle canlı nabız takibi
- Apple Sağlık dışa aktarımı ve CSV'den veri aktarımı (dosya cihazda işlenir, sunucuya yüklenmez)

**🤖 Yapay zekâ açıklamaları**
- AI yalnızca motorun ürettiği sonuçları **açıklar**, kendisi hesap yapmaz
- Uydurma sayı koruması: yanıttaki her sayı gerçek veriyle doğrulanır
- AI yalnızca kullanıcının açık izniyle çalışır; ad, e-posta gibi kimlik bilgileri gönderilmez

## 🏗️ Mimari

```
Mobil uygulama (PWA, çevrimdışı öncelikli)
        │
        ▼
API (REST, şema doğrulama) ──► Domain servisleri ──► PostgreSQL
        │
        ▼
Fitness motoru (bağımsız paket, istemci ve sunucuda aynı kurallar)
        │
        ▼
AI açıklama katmanı (sağlayıcıdan bağımsız, onaylı aksiyonlar)
```

- **Monorepo:** web istemcisi, API, fitness motoru ve ortak şemalar ayrı paketler
- **Çevrimdışı öncelikli:** IndexedDB kuyruğu, idempotent senkronizasyon, çoklu cihaz desteği
- **Gizlilik:** sağlık verisi loglanmaz, hesap silme tek işlemde gerçek silmedir, verini dışa aktarabilirsin
- **Kalite:** 60+ test dosyası (birim + veritabanı entegrasyonu) ve uçtan uca (Playwright) testler

## 🛠️ Teknolojiler

`TypeScript` · `React` · `Vite (PWA)` · `TanStack Query` · `Node.js` · `Fastify` · `Prisma` · `PostgreSQL` · `Zod` · `Vitest` · `Playwright`

## 🖼️ Ekran Görüntüleri

*Yakında eklenecek.*

## 📫 İletişim

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/musa-sefa-yurdakul-19b2b23b6/)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:yurdakulsefamusa@gmail.com)

---

© 2026 Musa Sefa Yurdakul — Tüm hakları saklıdır. Ayrıntılar: [LICENSE](LICENSE).
