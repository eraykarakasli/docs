# Gizlilik Politikası — Ezan Saatçim Pro

**Yürürlük tarihi:** 20 Nisan 2026
**Sürüm:** 1.0.0
**Uygulama adı:** Ezan Saatçim Pro
**Geliştirici / İletişim:** M. Eray Karakaşlı — `m.eraykarakasli@gmail.com`

Bu gizlilik politikası, Ezan Saatçim Pro mobil uygulamasının ("Uygulama") kullanıcılarının kişisel verilerinin nasıl işlendiğini, saklandığını ve korunduğunu açıklar. Uygulamayı indirip kullanarak bu politikayı kabul etmiş sayılırsınız.

---

## 1. Topladığımız Veriler

Uygulama **kullanıcı hesabı oluşturmaz**, kimlik bilgisi talep etmez ve kullanıcıların kişisel verilerini (ad, e-posta, telefon, T.C. kimlik no vb.) **sunucularımıza göndermez**.

Uygulamanın çalışması için aşağıdaki veriler **yalnızca cihazda** işlenir:

### 1.1. Konum Bilgisi
- **Ne işleniyor:** GPS veya ağ tabanlı konum (enlem/boylam).
- **Neden:** Namaz vakitlerinin hesaplanması, kıble yönünün belirlenmesi, yakın camilerin listelenmesi, hava durumu bilgisinin gösterilmesi ve (isteğe bağlı) cami çevresinde otomatik sessiz mod.
- **Saklama:** Son bilinen konum yalnızca cihaz üzerinde (`SharedPreferences`) tutulur. Sunucularımıza iletilmez.
- **Üçüncü taraflar:**
  - Ters coğrafi kodlama için OpenStreetMap Nominatim (`nominatim.openstreetmap.org`) — yalnızca koordinat gönderilir, kimlik bilgisi gönderilmez.
  - Yakın cami sorgusu için OpenStreetMap Overpass API (`overpass-api.de`, `overpass.kumi.systems`).
  - Harita karoları için CartoDB (`cartocdn.com`).
  - Yol tarifi için OSRM (`routing.openstreetmap.de`).
  - Hava durumu için Open-Meteo (`api.open-meteo.com`).

### 1.2. Bildirim Tercihleri ve Uygulama Ayarları
- **Ne işleniyor:** Hesaplama yöntemi, bildirim önceliği, sessiz mod yarıçapı, tema tercihi, son okunan sure gibi ayarlar.
- **Saklama:** Yalnızca cihazda (`SharedPreferences`, Isar veritabanı).
- **Sunucuya gönderilmez.**

### 1.3. Namaz Takip Verisi
- **Ne işleniyor:** Kullanıcının işaretlediği kıldım/kaçırdım/kaza durumları.
- **Saklama:** Yalnızca cihazda (Isar veritabanı). Sunucuya gönderilmez.

### 1.4. Cihaz ve Kullanım Bilgisi (Firebase Analytics)
- **Ne işleniyor:** Anonim kullanım istatistikleri (ekran görünümleri, oturum süresi, cihaz modeli, işletim sistemi sürümü, uygulama sürümü, genel bölge bilgisi).
- **Amaç:** Uygulamanın hangi özelliklerinin kullanıldığını anlamak, hataları tespit etmek, performansı iyileştirmek.
- **Kişisel veri içermez.** Google, bu verileri Firebase Analytics kullanım şartları çerçevesinde işler.

### 1.5. Bildirim Token'ı (Firebase Cloud Messaging)
- **Ne işleniyor:** Cihaza özel FCM token'ı (kandil/özel gün gibi dini gün bildirimlerinin ulaştırılabilmesi için).
- **Amaç:** Toplu dini gün bildirimleri (`religious_days` topic) göndermek.
- **Kişisel veri içermez.** Token sizi doğrudan tanımlamaz, sadece cihazınızı hedefler. Abone olmak istemezseniz bildirim izinlerini Android ayarlarından kapatabilirsiniz.

### 1.6. Uzaktan Yapılandırma (Firebase Remote Config)
- **Ne işleniyor:** Fitre, nisab, hicri takvim sapma değerleri gibi sayısal parametrelerin sunucudan okunması.
- **Kullanıcıdan veri çekmez.** Yalnızca uygulama sunucudan değerleri indirir.

---

## 2. Veri İşleme Amaçları

Veriler yalnızca aşağıdaki amaçlar için işlenir:
- Namaz vakitlerinin doğru hesaplanması
- Kıble yönünün gösterilmesi
- Yakın camilerin ve yol tariflerinin listelenmesi
- Hava durumunun gösterilmesi
- Cami sessiz modu (opsiyonel)
- Dini gün ve kandil bildirimleri
- Uygulama performansının ve özelliklerinin iyileştirilmesi (anonim analitik)

---

## 3. Üçüncü Taraf Servisler

Aşağıdaki servisler uygulama tarafından kullanılır. Her birinin kendi gizlilik politikası vardır:

| Servis | Amaç | Gizlilik Politikası |
|---|---|---|
| Google Firebase (Analytics, Messaging, Remote Config) | Analitik, bildirim, yapılandırma | https://firebase.google.com/support/privacy |
| OpenStreetMap Nominatim | Ters coğrafi kodlama | https://osmfoundation.org/wiki/Privacy_Policy |
| OpenStreetMap Overpass | Yakın cami sorgusu | https://osmfoundation.org/wiki/Privacy_Policy |
| CartoDB | Harita karoları | https://carto.com/privacy/ |
| OSRM (routing.openstreetmap.de) | Yol tarifi | https://routing.openstreetmap.de |
| Open-Meteo | Hava durumu | https://open-meteo.com/en/terms |
| everyayah.com | Kur'an ses yayını (CDN) | https://everyayah.com |

Uygulama, bu servislere **yalnızca teknik olarak gerekli olan minimum veriyi** (çoğunlukla anonim koordinat) gönderir.

---

## 4. İzinler

Uygulamanın Android'de istediği izinler ve kullanım nedenleri:

- **Konum (hassas + yaklaşık):** Namaz vakti, kıble, yakın camiler, hava durumu.
- **Arka plan konumu:** (Yalnızca cami sessiz modu açıkken) kullanıcının açıkça aktive ettiği cami çevresinde ringer modunu değiştirmek için.
- **Bildirim gönderme:** Ezan vakti ve dini gün hatırlatmaları.
- **Tam zamanlı alarm + tam ekran bildirim:** Ezan vakti bildirimlerinin zamanında tetiklenmesi.
- **Ön plan hizmeti (mediaPlayback, location):** Ezan ses çalma servisi ve cami sessiz modu.
- **Bildirim politikası erişimi (DND):** Cami sessiz modunda ringer modunu değiştirebilmek için.
- **İnternet:** Yukarıda listelenen üçüncü taraf servislerle iletişim.
- **Pil optimizasyonunu devre dışı bırakma (isteğe bağlı):** Bildirimlerin zamanında gelmesini garantilemek için.

Tüm izinler Android sistem ayarlarından yönetilebilir; reddetmek veya geri almak her zaman mümkündür. Bazı özellikler ilgili izin olmadığında çalışmaz (örn. konum izni reddedildiğinde namaz vakti hesaplanamaz).

---

## 5. Verilerin Saklama Süresi

- Yerel veriler (konum cache, namaz takip, ayarlar): Kullanıcı uygulamayı kaldırana kadar cihazda kalır.
- Firebase Analytics: Google'ın varsayılan saklama politikasına tabidir (14 ay, Google Firebase Console üzerinden ayarlanabilir).
- FCM token'ları: Cihaz uygulamayı kaldırdığında Google tarafından geçersiz kılınır.

---

## 6. Veri Güvenliği

- Kişisel veri sunucularımıza **iletilmez**, dolayısıyla sunucu ihlali riski taşımaz.
- Tüm üçüncü taraf servis çağrıları HTTPS üzerinden şifrelenerek yapılır.
- Yerel veriler cihazın işletim sistemi güvenlik modeli (Android uygulama sandbox'ı) altında korunur.

---

## 7. Çocukların Gizliliği

Uygulama tüm yaş gruplarına uygundur ve **13 yaş altından bilerek veri toplamaz**. Bir velinin çocuğunun verisinin işlendiğini düşünmesi durumunda aşağıdaki iletişim adresinden ulaşabilir.

---

## 8. Kullanıcı Hakları (KVKK / GDPR)

Türkiye'de ikamet eden kullanıcılar için 6698 sayılı Kişisel Verilerin Korunması Kanunu (KVKK) kapsamında; AB'de ikamet eden kullanıcılar için GDPR kapsamında aşağıdaki haklara sahipsiniz:

- İşlenen verilerinizin kapsamını öğrenme
- Yanlış işlenmiş verilerin düzeltilmesini isteme
- Silinmesini isteme (uygulamayı kaldırmanız yerel verilerin silinmesini sağlar; Firebase Analytics için talep üzerine silme talebi iletilir)
- İşlemeye itiraz etme
- Veri taşınabilirliği

Bu hakları kullanmak için: `m.eraykarakasli@gmail.com`

---

## 9. Politika Değişiklikleri

Bu politika zamanla güncellenebilir. Güncellemeler uygulama içinde ve bu sayfada yayımlanır. Önemli değişikliklerde uygulama içi bildirim ile bilgilendirme yapılır. Yürürlük tarihi her güncellemede revize edilir.

---

## 10. İletişim

Gizlilik ile ilgili tüm soru, talep ve şikayetleriniz için:

**M. Eray Karakaşlı**
E-posta: `m.eraykarakasli@gmail.com`

---

*Son güncelleme: 20 Nisan 2026*
