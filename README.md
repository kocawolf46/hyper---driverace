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
