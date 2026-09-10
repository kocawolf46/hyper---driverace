🏎️ HYPERDRIVE — PC'de Çalıştırma Rehberi
1️⃣ En Kolay Yöntem — Kurulum Yok
Bu proje vite-plugin-singlefile sayesinde tek bir HTML dosyasına derlenir. Yani bağımlılık, sunucu veya Node.js gerekmez.

Adımlar:

Proje klasörünü açın → dist klasörüne girin
index.html dosyasına çift tıklayın
Varsayılan tarayıcınızda (Chrome / Edge / Firefox) oyun açılır
🏁 "YARIŞA BAŞLA" butonuna basın
Notlar:

İnternet bağlantısı gerekmez — tüm Three.js kodu dosyanın içine gömülüdür (~1.1 MB)
Bu dosyayı USB belleğe kopyalayıp başka bir bilgisayarda da çalıştırabilirsiniz
E-posta ile gönderebilir, bulut depolamada paylaşabilirsiniz
2️⃣ Geliştirici Yöntemi — Kod Düzenlemek İçin
Gereksinimler: Node.js v18 veya üstü → https://nodejs.org (LTS sürümü)

Terminal komutları (proje klasöründe):

Komut	Ne yapar
node -v	Node.js kurulumunu doğrular
npm install	Bağımlılıkları yükler (three, react, zustand, tailwind...)
npm run dev	Geliştirme sunucusu → http://localhost:5173
npm run build	Production derlemesi → dist/index.html
npm run preview	Derlenmiş dosyayı yerel sunucuda önizler
npm run dev ile hot reload aktiftir — kodu değiştirdiğinizde tarayıcı otomatik güncellenir, oyunu anında test edebilirsiniz.

🎮 Kontroller
Tuş	Aksiyon
W / ↑	Gaz
S / ↓	Fren / geri
A D / ← →	Direksiyon
Shift veya N	Nitro 🚀
Q	Önceki boyut
E	Sonraki boyut
ESC	Duraklat / devam
🌀 Boyutlar ve Strateji
Boyut	Renk	Karakter
SİBER	Camgöbeği	Dengeli başlangıç
NEON	Magenta	Hız bonusu
ALTIN	Sarı	Nitro bonusu
NEO	Yeşil	Tutuş bonusu
ATEŞ	Turuncu	Maksimum hız
İpuçları:

Nitroyu düzlüklerde kullanın, virajlarda boşa gider
Nitro barı zamanla kendini doldurur (saniyede ~5 birim)
Boyut değiştirmek hızınızı sıfırlamaz — virajdan önce geçiş yapın
Her boyutta pistin rengi ve atmosferi değişir, gözünüz yorulmasın diye uygun boyutu seçin
❓ Sorun Giderme
Sorun	Çözüm
Siyah ekran	Tarayıcıda chrome://gpu adresine gidin, WebGL aktif olmalı. Donanım hızlandırmayı açın
Arabalar görünmüyor	3 saniyelik geri sayım bitince araçlar sahnede belirir. W ile gaz verin
Düşük FPS	Gereksiz sekmeleri kapatın, tarayıcı penceresini küçültün, diğer uygulamaları kapatın
Tuşlar çalışmıyor	Sayfaya bir kez tıklayın (odak gerekir), Türkçe Q klavyede de WASD aynı çalışır
Ses yok	Oyun şu an sessizdir — Web Audio API henüz eklenmedi
Tam ekran	F11 tuşu ile tarayıcı tam ekranı önerilir
📦 Teknik Özet
Motor: Three.js (WebGL) + React Three Fiber
Durum yönetimi: Zustand
Stil: Tailwind CSS v4
Derleyici: Vite 7
Çıktı: Tek dosya dist/index.html
Pist: 200 segmentli prosedürel döngü, yükseklik dalgaları, neon bariyerler
Rakipler: 5 bağımsız AI araç, pist üzerinde bağımsız ilerler
Kamera: Yumuşatılmış takip kamerası (lerp)
Masaüstü kısayolu: index.html dosyasına sağ tıklayın → Bir kısayol oluştur → kısayolu masaüstüne taşıyın. Artık simgeye tıklayarak oyunu direkt açabilirsiniz. 🏁

İyi yarışlar! 💨

HYPERDRIVE ARABA YARISI - BILGISAYARDA CALISTIRMA KILAVUZU

GEREKSINIMLER

Bilgisayarinizda Node.js programi kurulu olmalidir.
Eger kurulu degilse https://nodejs.org adresine giderek yesil renkli LTS surumunu indirip kurun.
CALISTIRMA ADIMLARI

Adim 1: Komut Satirini (Terminal) Acin

Windows kullaniyorsaniz proje klasorunun icine girin. Ustteki adres cubuguna cmd yazip Enter tusuna basin.
Mac veya Linux kullaniyorsaniz Terminal uygulamasini acin ve "cd klasor_yolu" komutu ile proje klasorune gidin.
Adim 2: Kutuphaneleri Yukleyin
Terminal ekranina su komutu yazip Enter'a basin:
npm install

Bu islem oyunun ihtiyaci olan React, Three.js, Zustand ve diger paketleri otomatik olarak indirecektir. Islem yaklasik 1-2 dakika surebilir.

Adim 3: Oyunu Baslatin
Paketler yuklendikten sonra ayni terminal ekranina su komutu yazin:
npm run dev

Ekranda sunucu baglantisi belirecektir (genellikle http://localhost:5173).

Adim 4: Tarayicida Oynayin
Chrome, Edge, Opera veya Firefox tarayicinizi acin.
Adres cubuguna su adresi yazip Enter'a basin:
http://localhost:5173

Oyun ana menusu acilacaktir. "YARISA BASLA" butonuna basarak oynayabilirsiniz.

ALTERNATIF YONTEM (TEK DOSYA HALINDE CALISTIRMA)
Eger oyunu internet baglantisi olmadan, sadece cift tiklayarak tek bir HTML dosyasi uzerinden acmak isterseniz:

Terminale "npm run build" yazip Enter'a basin.
Proje icinde olusan "dist" klasorune gidin.
"index.html" dosyasina cift tiklayarak oyunu dogrudan tarayicinizda calistirin.
OYUN KONTROLLERI

W veya Yukari Ok: Gaz (Ileri gitme)
S veya Asagi Ok: Fren ve Geri vites
A veya Sol Ok: Sola donus
D veya Sag Ok: Saga donus
Shift veya N tusu: Nitro Boost (Yuksek hiz ve alev efekti)
Q ve E tuslari: Boyut degistirme (Pist, arac ve evren temalarini degistirir)
ESC tusu: Oyunu duraklat / Devam et




