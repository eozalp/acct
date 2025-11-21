Aşağıdaki kod bloğunu kopyalayıp GitHub deponuzda `README.md` dosyası olarak kaydedebilirsiniz.

```markdown
# 💎 Esnaf Glass v4.3 (PWA Sürümü)

**Küçük İşletmeler ve Freelancerlar için Tek Dosyalı, İnternetsiz Finans Yöneticisi.**

![Lisans](https://img.shields.io/badge/lisans-MIT-blue.svg)
![Durum](https://img.shields.io/badge/durum-%C3%87evrimd%C4%B1%C5%9F%C4%B1%20%C3%87al%C4%B1%C5%9F%C4%B1r-green.svg)
![Platform](https://img.shields.io/badge/platform-Web%20%7C%20iOS%20%7C%20Android-orange.svg)

Esnaf Glass, tamamen tarayıcınızda çalışan, sunucu veya kurulum gerektirmeyen modern bir finans takip uygulamasıdır. Hem dokunmatik arayüzü hem de ileri düzey kullanıcılar için geliştirici terminali (CLI) barındırır.

**Sunucu yok. Veritabanı kurulumu yok. İnternet bağlantısı gerekmez.**

---

## ✨ Özellikler

*   **📱 Progressive Web App (PWA):** iOS ve Android cihazlarda uygulama mağazasına gerek kalmadan kurulur. %100 çevrimdışı (offline) çalışır.
*   **💰 Finans Takibi:** Peşin/Veresiye Satışlar, Giderler ve Stok Yönetimi.
*   **👥 Veresiye Defteri:** Müşteri ve tedarikçilerle olan borç/alacak (cari) durumunu takip edin.
*   **📊 Analizler:** Anlık Net Varlık hesaplaması, haftalık ciro grafikleri ve kar marjı tahmini.
*   **💻 Dahili Terminal (CLI):** İşlemleri komut yazarak çok hızlı bir şekilde girin (Alias desteği ile).
*   **🔒 %100 Gizlilik:** Tüm veriler sadece sizin tarayıcınızda (`localStorage`) saklanır. Buluta gitmez.
*   **🎨 Dinamik Temalar:** Karanlık, Açık, Matrix ve Mavi temalar arasında geçiş yapın.
*   **📂 Yedekleme:** Verilerinizi JSON veya Excel (CSV) formatında dışa aktarın.

---

## 🚀 Nasıl Kullanılır?

### Seçenek 1: İndir ve Çalıştır
1.  `esnaf_glass_v4.3_pwa.html` dosyasını indirin.
2.  Herhangi bir modern tarayıcıda (Chrome, Safari, Edge) dosyayı açın.
3.  Uygulama anında kullanıma hazırdır!

### Seçenek 2: GitHub Pages (Önerilen)
1.  Bu depoyu (repository) Fork'layın.
2.  **Settings** > **Pages** menüsüne gidin.
3.  Kaynağı `main` branch olarak seçin.
4.  Size verilen linke tıklayın (örn: `kullaniciadi.github.io/esnaf-glass`).

---

## 📲 Mobil Kurulum (PWA)

Esnaf Glass, telefonunuzda yerel bir uygulama gibi çalışacak şekilde tasarlanmıştır.

### iOS (iPhone/iPad)
1.  Siteyi **Safari** ile açın.
2.  Alt menüdeki **Paylaş** butonuna (kare içinde yukarı ok) dokunun.
3.  Aşağı kaydırıp **"Ana Ekrana Ekle"** seçeneğine dokunun.

### Android
1.  Siteyi **Chrome** ile açın.
2.  Sağ üstteki **Menü** (üç nokta) butonuna dokunun.
3.  **"Uygulamayı Yükle"** veya **"Ana Ekrana Ekle"** seçeneğine dokunun.

---

## 💻 Terminal (CLI) Kullanım Kılavuzu

Hızlı işlem yapmak isteyenler için terminal modülü.
**Açmak için:** Üst menüdeki `>_` ikonuna tıklayın veya klavyedeki `~` (é/tilde) tuşuna basın.

### 1. Temel Komutlar

| Komut | Açıklama | Örnek |
| :--- | :--- | :--- |
| `help` | Komut listesini gösterir | `help` |
| `status` | Kasa, stok ve işlem sayısını gösterir | `status` |
| `theme` | Temayı değiştirir | `theme matrix` |
| `calc` | Hesap makinesi | `calc 500 * 1.2` |

### 2. İşlem Ekleme

**Gelir / Satış:**
```bash
# Peşin Satış (Kasa Artar, Stok Düşer)
add income 100 "Kahve"

# Veresiye Satış (Kişi Borçlanır, Stok Düşer)
add income 500 -v "Ahmet Yılmaz" "Tamirat"
```

**Gider / Mal Alımı:**
```bash
# Gider Ekleme
add expense 50 "Yemek"

# Mal Alımı (Peşin)
add buy 2000 "Yedek Parça"
```

### 3. Cari İşlemler (Borç/Alacak)

```bash
# Ödeme Yap (Bizden para çıkar, borcumuz düşer)
pay give "Toptancı Ali" 1000 "Fatura Ödemesi"

# Tahsilat Yap (Kasa artar, alacağımız düşer)
pay take "Müşteri Ayşe" 500 "Elden Tahsilat"
```

### 4. Kısayollar (Alias)
Sürekli yazdığınız komutları kısaltabilirsiniz.

```bash
# 's' harfini 'add income' olarak tanımla
alias set s "add income"

# Artık sadece 's' yazarak satış yapabilirsiniz:
s 50 "Hızlı Satış"
```

---

## 💾 Yedekleme ve Güvenlik

Bu uygulama verilerinizi sunucuya göndermez. Veriler tarayıcınızın **Önbelleğinde (Local Storage)** tutulur.

*   **Veri Kaybını Önlemek İçin:** Düzenli aralıklarla **Ayarlar (⚙️) -> Yedekleme** menüsünden "İndir (JSON)" diyerek yedeğinizi alın.
*   **Tarayıcı Temizliği:** Tarayıcı geçmişini veya çerezleri temizlerseniz veriler silinebilir. Bu durumda aldığınız yedeği geri yükleyebilirsiniz.

---

## 🛠 Teknik Bilgi

*   **Teknoloji:** HTML5, CSS3, Vanilla JavaScript.
*   **Dosya Boyutu:** < 100KB (Görseller SVG olarak gömülüdür).
*   **Servis Çalışanı (SW):** Uygulama açıldığında kendini önbelleğe alır ve internet bağlantısı kesildiğinde çalışmaya devam eder.

---

## 📄 Lisans

Bu proje **MIT Lisansı** ile sunulmuştur. Kişisel veya ticari amaçlarla özgürce kullanabilir, değiştirebilir ve dağıtabilirsiniz.
```
