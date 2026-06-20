# BacklinkManager — Ürün Tanıtım Dökümanı

**Kurumsal Backlink İzleme ve Dijital Varlık Yönetimi Platformu**

---

## Platform Nedir?

BacklinkManager, dijital pazarlama ajanslarının ve SEO profesyonellerinin müşteri sitelerindeki backlinkleri, uptime durumunu, SSL sertifikalarını, domain sürelerini, anahtar kelimeleri ve Core Web Vitals değerlerini **tek bir merkezi panel** üzerinden gerçek zamanlı izlemesini sağlayan bir SaaS platformudur.

Platform; otomatik tarama motorları, akıllı bildirim sistemi, çok katmanlı yetkilendirme ve güçlü bir API altyapısıyla kurumsal ölçekte çalışmak üzere tasarlanmıştır.

---

## Kimler İçin?

| Hedef Kitle | Kullanım Senaryosu |
|-------------|-------------------|
| **Dijital Pazarlama Ajansları** | Onlarca müşteri sitesinin backlink ve uptime durumunu merkezi panelden yönetme |
| **SEO Profesyonelleri** | Backlink kayıplarını anında tespit edip müşteriye bildirme |
| **Web Yöneticileri** | SSL ve domain bitiş tarihlerini kaçırmama, güvenlik tehditlerini otomatik takip etme |
| **Kurumsal IT Ekipleri** | Çok kullanıcılı takım yönetimi, API entegrasyonu, özel bildirim kanalları |

---

## Ne Sorunu Çözüyor?

**Backlink takibi manuel ve zaman alıcıdır.** Ajanslar onlarca ya da yüzlerce müşteri sitesini takip etmek için her siteyi tek tek ziyaret etmek veya birden fazla araç kullanmak zorunda kalır.

BacklinkManager bu süreci tamamen otomatikleştirir:

- ❌ "Müşteri sitenin linkimizi kaldırmış, 3 hafta sonra fark ettik."
- ✅ **Kaldırıldığı saat, e-posta ve Slack bildirimi gelir.**

---

## Temel Özellikler

### Backlink İzleme

Gerçek bir tarayıcı motoruna dayanan tarama altyapısı, sitenin **statik HTML kaynağını** analiz eder:

- `EXACT` (birebir) ve `CONTAINS` (içerir) eşleşme modu
- Glob pattern desteği — örneğin `mobitek.org/m*.svg` ile tüm logo varyantlarını tek girişle izleme
- Görsel URL erişilebilirlik doğrulaması (logo dosyası gerçekten açılıyor mu?)
- JS widget entegrasyonu — panelden kapatılan logo "bulunamadı" olarak işaretlenir
- Çoklu snippet hedefi — bir site için birden fazla hedef HTML ayrı ayrı izlenir
- Değişim tespiti — önceki tarama ile karşılaştırma, durum geçişlerinde bildirim

### Uptime İzleme

- HTTP status code tabanlı kontrol, özelleştirilebilir beklenen kodlar
- Her dakika kontrol, DOWN/UP geçişlerinde anında uyarı
- Uptime istatistikleri ve tarihsel grafik

### SSL Sertifika Takibi

- Sertifika bitiş tarihi otomatik kontrolü
- 30, 15 ve 7 gün öncesi uyarı e-postaları
- Site bazlı kontrol aralığı ayarı

### Domain Bitiş İzleme (WHOIS)

- WHOIS sorgusuna dayalı domain bitiş tarihi takibi
- Site bazlı kontrol sıklığı (1–720 saat)
- Bitiş öncesi otomatik uyarı

### Anahtar Kelime İzleme

- Sayfada belirli bir kelimenin varlığını/yokluğunu izleme
- Büyük/küçük harf duyarlılığı seçeneği
- Rakip siteler için de aynı kontrol

### Core Web Vitals (Performans)

- Playwright tabanlı gerçek tarayıcı ölçümü
- LCP (Largest Contentful Paint), CLS, FID değerleri
- Günlük ölçüm, tarihsel karşılaştırma

### Güvenlik Taraması

- Google Safe Browsing API entegrasyonu
- Zararlı site tespitinde otomatik uyarı
- Günlük kontrol

### Rakip Analizi

- Rakip siteleri için backlink, uptime, keyword, SSL, domain takibi
- Marka (Brand) bazlı gruplama
- Takım bazlı atama ve yetkilendirme

---

## Bildirim Sistemi

**7 farklı kanal**, tek bir etkinlikte hepsine veya seçilenlere bildirim gönderilebilir:

| Kanal | Açıklama |
|-------|----------|
| **E-posta** | Şablonlu, özelleştirilebilir |
| **In-App** | Panel içi bildirim merkezi |
| **Web Push** | Tarayıcı push bildirimi (VAPID) |
| **Webhook** | Özel payload şablonu, 3x retry |
| **Slack** | Kanal entegrasyonu |
| **Discord** | Sunucu webhook entegrasyonu |
| **Microsoft Teams** | Teams kanal entegrasyonu |

**Akıllı susturma özellikleri:**

- **Bakım modu** — Site bakım sürecindeyken tüm uyarılar susturulur
- **Sessiz saatler** — Gece gelen gereksiz bildirimler engellenir
- **Site bazlı kurallar** — Her site için hangi olaylarda, hangi adreslere bildirim gidecek ayrı ayrı tanımlanabilir

---

## Alert Kuralları

Önceden tanımlanmış bildirim senaryolarının ötesinde, kullanıcılar **özel koşul/aksiyon kuralları** oluşturabilir:

- "Son 3 uptime kontrolünde DOWN ise ekibi bildir"
- "Backlink 7 gündür bulunamıyorsa yöneticiye e-posta at"
- Her 10 dakikada bir otomatik değerlendirme

---

## Raporlama

- **Haftalık / Aylık e-posta raporları** — Site sağlığı özeti, backlink ve uptime trendi
- **Admin tetiklemeli raporlar** — İstediğiniz zaman manuel rapor gönderimi
- **Anlık istatistikler** — Panel içinde grafik ve tablolarla görselleştirme

---

## Takım Yönetimi

Çok kullanıcılı yapı, farklı yetki seviyelerinde takım çalışmasını destekler:

**Takım rolleri:** OWNER / ADMIN / VIEWER

**Site bazlı yetkiler:**

| Yetki | Açıklama |
|-------|----------|
| `canView` | Siteyi görebilir |
| `canEdit` | Site ayarlarını değiştirebilir |
| `canDelete` | Siteyi silebilir |
| `canTriggerScan` | Manuel tarama başlatabilir |
| `canManageAlerts` | Alert kurallarını yönetebilir |

**E-posta ile davet** — Yeni üyeler davet linki ile sisteme dahil edilir.

---

## Durum Sayfaları

Müşterileriniz veya son kullanıcılarınız için **public durum sayfaları** oluşturun:

- Özel URL (`/s/[slug]`) veya **özel domain** (kendi domain'inizi bağlayın)
- Bileşen bazlı durum gösterimi
- Olay (incident) yönetimi ve duyuru
- Ziyaretçi e-posta aboneliği (durum değişikliğinde otomatik bildirim)

---

## API ve Entegrasyon

Tüm platform verilerine programatik erişim:

- **REST API** — Tüm varlıklar için tam CRUD
- **OpenAPI 3 / Swagger UI** — Otomatik üretilen dokümantasyon (`/admin/api-docs`)
- **API Key yönetimi** — `blm_` prefix, SHA-256 hash güvenliği, rotasyon
- **Rate limiting** — Kötüye kullanım koruması

---

## Güvenlik Altyapısı

| Özellik | Detay |
|---------|-------|
| **Kimlik doğrulama** | E-posta + şifre (bcrypt), JWT tabanlı oturum |
| **İki faktörlü doğrulama (2FA)** | TOTP uyumlu authenticator uygulamaları (Google, Authy vb.) + yedek kodlar |
| **Admin zorunlu 2FA** | Yönetici, belirli kullanıcılar için 2FA'yı zorunlu kılabilir |
| **IP kısıtlama** | Admin/dashboard paneli whitelist IP listesiyle kısıtlanabilir |
| **Bakım modu** | Sistem bakım modunda; admin hariç tüm kullanıcı erişimi engellenebilir |
| **Dinamik RBAC** | Her rol için sayfa/özellik izinleri admin panelinden ayarlanır |
| **Audit log** | Tüm önemli işlemler kayıt altına alınır |

---


## Teknik Altyapı (Özet)

Platform, kurumsal ölçekte çalışmak üzere tasarlanmış modern bir yığın üzerine inşa edilmiştir:

| Bileşen | Teknoloji |
|---------|-----------|
| Uygulama | Next.js 14 (App Router) |
| Dil | TypeScript (strict mod) |
| Veritabanı | PostgreSQL 15 + Prisma ORM |
| Queue sistemi | Redis + BullMQ |
| Tarama motoru | Playwright (Chromium) |
| Oturum | NextAuth v5 (JWT) |
| Deployment | Docker Compose + Traefik |
| CI/CD | Jenkins + ntfy bildirimleri |

**Yüksek erişilebilirlik için tasarım:**

- Tüm arka plan işleri (tarama, uptime, keyword, performans, güvenlik) ayrı container'larda çalışır
- Worker heartbeat sistemi — her worker'ın sağlık durumu gerçek zamanlı izlenir
- Otomatik yeniden deneme (exponential backoff) — geçici hatalar için iş kaybı olmaz
- Queue kalıcılığı — Redis yeniden başlatılsa bile bekleyen işler korunur

---



## Nasıl Çalışır?

```
1. Siteyi ekleyin
   → URL, hedef snippet ve tarama sıklığını belirleyin

2. Sistem otomatik çalışır
   → Cron scheduler belirlenen aralıklarda tarama başlatır
   → Worker statik HTML'i çeker ve snippet'i analiz eder

3. Sonuç değerlendirmesi
   → Bulundu / Bulunamadı / Erişim hatası

4. Durum değişmişse bildirim
   → E-posta, Slack, webhook veya seçtiğiniz kanala anında uyarı

5. Panel üzerinden takip
   → Tarihsel grafik, tarama geçmişi, kök neden analizi
```

---




## Örnek Kullanım Senaryoları

### Senaryo 1 — Ajans + Müşteri Logo Takibi

Dijital pazarlama ajansı, müşteri sitelerine yerleştirdiği logo linklerin aktif olup olmadığını günlük takip eder. Logo kaldırıldığında veya panel üzerinden pasif yapıldığında, ajans yöneticisi anında Slack bildirimi alır ve müşteriyle iletişime geçer.

### Senaryo 2 — SSL Sona Erme Uyarısı

Yönettiğiniz 30 sitenin SSL sertifikaları merkezi panelden takip edilir. Herhangi birinin sertifikası 30, 15 veya 7 gün içinde dolacaksa otomatik e-posta uyarısı gelir. Manuel kontrol gerekmez.

### Senaryo 3 — Rakip Analizi

Rakip siteler eklenip backlink profilleri, anahtar kelime kullanımı ve uptime durumu düzenli olarak izlenir. Rakip sitenin önemli bir backlink kaybettiği tespit edildiğinde fırsat değerlendirilebilir.

### Senaryo 4 — Public Durum Sayfası

Kurumsal müşterilere özel `status.sirketim.com` domain'i ile durum sayfası oluşturulur. Bakım penceresi açıldığında abone olan kullanıcılara otomatik e-posta gönderilir.

### Senaryo 5 — Takım Bazlı Yönetim

Büyük ajans, her müşteri için ayrı takım oluşturur. İlgili ekip üyeleri yalnızca kendi müşterilerinin sitelerini görür ve yönetir. Merkezi admin tüm sistemi gözetir.

---


