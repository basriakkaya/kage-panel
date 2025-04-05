# 🥷 KAGE Panel

KAGE Panel, siber güvenlik testleri için geliştirilmiş hafif, modüler ve genişletilebilir bir web tabanlı recon panelidir.

## 🎯 Özellikler

- 🔍 Nmap port tarama sonuçlarını görüntüleme
- 🌐 WhatWeb teknoloji tespiti
- 📁 Sonuç dosyalarını kolay erişilebilir formatta görüntüleme
- 📌 Hedef domain ekleme ve yönetme
- 🧪 Tek tıkla test başlatma
- 📊 Basit istatistikler

## 🛠️ Teknolojiler

- Frontend: React + Vite + TailwindCSS
- Backend: Node.js + Express
- Tarama Araçları: Nmap, WhatWeb

## 📋 Gereksinimler

- Node.js 18+
- Nmap
- WhatWeb
- Kali Linux (önerilen)

Kali Linux kurulumu için [KALI_KURULUM.md](KALI_KURULUM.md) dosyasına bakın.

## 🚀 Kurulum

1. Repoyu klonlayın:
```bash
git clone https://github.com/kullanıcıadı/kage-panel
cd kage-panel
```

2. Backend kurulumu:
```bash
cd backend
npm install
npm run dev
```

3. Frontend kurulumu (yeni terminal):
```bash
cd frontend
npm install
npm run dev
```

4. Tarayıcıda açın:
```
http://localhost:5173
```

## 📝 Kullanım

1. Hedef domain ekleyin
2. İstediğiniz tarama türünü seçin
3. Sonuçları panelden inceleyin

## 🔒 Güvenlik Notları

Bu tool yalnızca:
- Yasal penetrasyon testlerinde
- Kendi sistemlerinizde
- İzin verilen sistemlerde kullanılmalıdır

## 🤝 Katkıda Bulunma

1. Fork edin
2. Feature branch oluşturun
3. Değişikliklerinizi commit edin
4. Branch'inizi push edin
5. Pull request açın

## 📜 Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Detaylar için [LICENSE](LICENSE) dosyasına bakın.

## ✨ Gelecek Özellikler

- [ ] Betik takip / loglama sistemi
- [ ] Hedef bazlı klasörleme
- [ ] Zafiyet öneri sistemi
- [ ] PDF / JSON rapor alma
- [ ] API entegrasyonları (Slack, Telegram, Discord) 
