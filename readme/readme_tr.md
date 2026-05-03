# 🐦 X.com Video Analiz Aracı

> X'ten (eski adıyla Twitter) video içeriği çıkarmak için hafif, hızlı ve çok yönlü bir araç

[🌐 Çevrimiçi Demo](https://twittervideodownloaderx.com/tu) • [📝 Kullanım Kılavuzu](#-kullanım-kılavuzu) • [❓ Sıkça Sorulan Sorular](#-sıkça-sorulan-sorular)

---

## 📋 Proje Genel Bakışı

Bu proje, X.com'da (eski adıyla Twitter) yer alan herkese açık gönderilerden video kaynaklarını güvenli bir şekilde çıkarmak ve çeşitli formatlarda dönüştürme/indirme seçeneği sunmak amacıyla geliştirilmiş web tabanlı bir video analiz aracıdır. Herhangi bir istemci yazılım kurulumu veya hesap kaydı gerektirmez; doğrudan tarayıcınız üzerinden kullanabilirsiniz.

> ⚠️ **Önemli Uyarı**: Bu araç yalnızca kişisel öğrenme, teknik araştırma ve makul kullanım sınırları içinde kullanılmak üzere tasarlanmıştır. Lütfen [X Platformu Geliştirici Sözleşmesi](https://developer.twitter.com/en/developer-terms/agreement) ve ülkenizde geçerli olan telif hakkı yasalarına uyun. Başkalarının haklarını ihlal eden amaçlarla kullanılması kesinlikle yasaktır.

---

## ✨ Temel Özellikler

- 🔗 **Bağlantı Analizi**: Standart X.com gönderi URL'lerini destekler; video ve animasyonlu GIF'leri otomatik olarak tanır
- 📥 **Çoklu Format Dışa Aktarma**:
  - Orijinal kalitede MP4 video
  - Ses çıkarma → MP3 formatı
  - Video klibi → Animasyonlu GIF'e dönüştürme
- 🌍 **Çok Dilli Arayüz**: Türkçe, İngilizce, Çince, Japonca, Korece dahil toplam 16 dil desteği
- 📱 **Çapraz Platform Uyumluluğu**: Chrome / Firefox / Safari / Edge tarayıcılarında sorunsuz çalışır; mobil cihazlar ve tabletler için optimize edilmiş deneyim
- 🔒 **Gizlilik Öncelikli**: Hesap kaydı gerekmez, kişisel veri toplanmaz; analiz süreci tamamen anonimdir
- ⚡ **Hızlı İşleme**: Analiz ortalama 5 saniyeden kısa sürede tamamlanır; eşzamanlı istek desteği

---

## 🚀 Hızlı Başlangıç

### Çevrimiçi Kullanım (önerilen)
1. [https://twittervideodownloaderx.com/tu](https://twittervideodownloaderx.com/tu) adresine gidin
2. Hedef gönderinin bağlantısını kopyalayın (örnek: `https://x.com/user/status/123456789`)
3. Bağlantıyı giriş alanına yapıştırın → 「Analiz Et」butonuna tıklayın
4. İstediğiniz formatı seçin → Tarayıcı talimatlarını izleyerek dosyayı kaydedin

### Yerel Dağıtım (geliştiriciler için)
```bash
# Deposu klonlayın
git clone https://github.com/your-repo/x-video-parser.git

# Bağımlılıkları yükleyin
cd x-video-parser && npm install

# Ortam değişkenlerini yapılandırın (isteğe bağlı)
cp .env.example .env

# Geliştirme sunucusunu başlatın
npm run dev
```

> 💡 Not: Bu proje Node.js + Express tabanlı bir mimari kullanır. Ayrıntılı dağıtım belgeleri için `/docs/DEPLOY.md` dosyasına bakınız.

---

## 🛠 Teknoloji Yığını

| Modül | Kullanılan Teknolojiler |
|-------|-------------------------|
| Ön Yüz | Vue 3 + TypeScript + Vite |
| Arka Yüz | Node.js + Express + Axios |
| Video İşleme | ffmpeg.wasm (hafif ön yüz dönüştürme) |
| Proxy Yönlendirme | Cloudflare Workers / Özel Ara Katman Yazılımı |
| Uluslararasılaştırma | vue-i18n + JSON Dil Paketleri |

---

## 📚 Kullanım Kılavuzu

### Temel Çalışma Akışı
```
1. Gönderi bağlantısını alın
   └─ X.com'da hedef gönderiyi açın → Tarayıcı adres çubuğundan URL'yi kopyalayın

2. Analiz isteği gönderin
   └─ Bağlantıyı araç giriş alanına yapıştırın → 「Video İndir」butonuna tıklayın

3. Çıktı formatını seçin
   ├─ 🎬 MP4 olarak indir: Orijinal kalitede kaydet
   ├─ 🎵 MP3'e dönüştür: Ses parçasını çıkar
   └─ 🎞 GIF'e dönüştür: Kısa animasyon oluştur (önerilen: ≤15 saniye)

4. Dosyayı kaydedin
   └─ Kaynak yeni sekmede açılacak → Sağ tık/menü → 「Farklı kaydet」
```

### Mobil Cihazlarda Kullanım İpuçları
- iOS Safari: Paylaş butonu → 「Dosyalara Kaydet」
- Android Chrome: Videoya basılı tutun → 「Video indir」
- Video otomatik oynatılıyorsa: Oynatıcı sağ üst köşedeki `⋮` simgesine tıklayın → 「İndir」seçeneğini seçin

---

## ❓ Sıkça Sorulan Sorular

**S: İndirilen dosyalar nereye kaydedilir?**  
C: Dosyalar, tarayıcınızda yapılandırılan indirme klasörüne kaydedilir. Bu yolu tarayıcı ayarlarından kontrol edebilir veya değiştirebilirsiniz.

**S: Özel hesapları veya kısıtlı içeriği analiz edebilir miyim?**  
C: Hayır. Bu araç yalnızca herkese açık olarak ayarlanmış gönderilerle çalışır ve orijinal içeriğin erişim ayarlarına saygı duyar.

**S: Dönüştürme sonrası görüntü/ses kalitesi düşer mi?**  
C: MP4 formatı orijinal kaliteyi korur. MP3 formatı 128 kbps standart kodlama kullanır. GIF formatı ise dosya boyutu ve akıcılık arasında denge kurmak için süreye göre kare hızını optimize eder.

**S: İndirme geçmişi veya önbellek saklanır mı?**  
C: Hayır. Tüm kaynaklar geçici bir proxy aracılığıyla doğrudan kullanıcının cihazına iletilir; sunucu herhangi bir istek veya medya dosyası saklamaz.

**S: Analiz başarısız olursa ne yapmalıyım?**  
C: Lütfen şunları kontrol edin: ① Bağlantının geçerli bir herkese açık gönderiye ait olup olmadığı ② İnternet bağlantınızın stabil olup olmadığı ③ Farklı bir tarayıcı deneyin. Sorun devam ederse, bir Issue açarak bildirmekten çekinmeyin.

---

## ⚖️ Yasal Uyumluluk ve Sorumluluk Reddi

- Bu araç, platformların **hiçbir teknik koruma önlemini atlamaz veya ihlal etmez**; yalnızca genel arayüzler aracılığıyla meta verileri alır
- Kullanıcı, kendi kullanımının yerel yasalara ve platformun hizmet şartlarına uygun olduğunu doğrulamaktan sorumludur
- Önerilen kullanım senaryoları: Kişisel arşivleme, eğitim amaçlı gösterimler, içerik oluşturma için referans materyaller... her zaman adil kullanım (Fair Use) çerçevesinde
- Hak ihlali şüphesi taşıyan bir içerik fark ederseniz, lütfen [X'in bu telif hakkı bildirim formu aracılığıyla](https://help.twitter.com/forms/dmca) resmi kanala başvurun

---

## 🤝 Katkı Sağlama Kılavuzu

Pull Request'lerinizi ve Issue bildirimlerinizi memnuniyetle karşılıyoruz! Katkı sağlamadan önce lütfen aşağıdaki belgeleri inceleyin:
- [Kod Standartları](/CONTRIBUTING.md)
- [Çok Dilli Çeviri Kılavuzu](/locales/README.md)
- [Güvenlik ve Uyumluluk Gereksinimleri](/SECURITY.md)

---

## 📄 Lisans

Bu proje [MIT Lisansı](/LICENSE) altında yayınlanmaktadır. Eğitim ve araştırma amaçlı ücretsiz olarak kullanılabilir. Ticari kullanım için, lütfen geçerli yasal düzenlemelere uyumu dikkatlice kontrol ediniz.

---

> 🌟 Bu araç sizin için faydalı olduysa, ✨bir Yıldız (Star) vermeyi unutmayın! Desteğiniz, bu projeyi sürdürmeye ve geliştirmeye devam etmemiz için en büyük motivasyon kaynağıdır~

*Son güncelleme: Mayıs 2026 | Sürüm: v2.1.0*