# 🐉 Kali Linux Kurulum Rehberi

## 📋 İçindekiler
1. [Sistem Gereksinimleri](#sistem-gereksinimleri)
2. [İndirme Seçenekleri](#indirme-seçenekleri)
3. [Kurulum Adımları](#kurulum-adımları)
4. [Kurulum Sonrası Yapılacaklar](#kurulum-sonrası-yapılacaklar)
5. [KAGE Panel için Gerekli Araçlar](#kage-panel-için-gerekli-araçlar)

## 💻 Sistem Gereksinimleri
- Minimum 2GB RAM (önerilen: 4GB veya daha fazla)
- 20GB disk alanı (önerilen: 30GB veya daha fazla)
- x64 işlemci mimarisi
- USB bellek (en az 8GB) veya DVD
- İnternet bağlantısı

## 📥 İndirme Seçenekleri
1. **ISO İndirme**
   - [Kali Linux resmi sitesinden](https://www.kali.org/get-kali/) ISO dosyasını indirin
   - Önerilen sürüm: Kali Linux 64-Bit (installer)

2. **USB Belleğe Yazma**
   - Windows için: Rufus veya Etcher kullanın
   - Linux için: dd komutu veya Etcher kullanın
   ```bash
   sudo dd if=kali-linux.iso of=/dev/sdX bs=4M status=progress
   ```

## 🛠️ Kurulum Adımları
1. **BIOS/UEFI Ayarları**
   - Bilgisayarı yeniden başlatın
   - BIOS/UEFI menüsüne girin (genellikle F2, F12 veya Del tuşu)
   - Boot sıralamasında USB'yi ilk sıraya alın
   - Secure Boot'u devre dışı bırakın

2. **Kurulum Başlangıcı**
   - USB'den boot edin
   - "Graphical Install" seçeneğini seçin
   - Dil ve klavye düzenini seçin

3. **Disk Bölümlendirme**
   ```
   / (root)     : 20GB
   /home        : Kalan alan
   swap         : RAM miktarınız kadar
   ```

4. **Kullanıcı Ayarları**
   - Güçlü bir root şifresi belirleyin
   - Normal kullanıcı hesabı oluşturun

## 🔧 Kurulum Sonrası Yapılacaklar
1. **Sistem Güncellemesi**
   ```bash
   sudo apt update
   sudo apt full-upgrade -y
   ```

2. **Temel Araçların Kurulumu**
   ```bash
   sudo apt install -y \
   git \
   curl \
   wget \
   vim \
   tmux \
   build-essential
   ```

3. **Türkçe Dil Desteği**
   ```bash
   sudo apt install -y locales-all
   sudo dpkg-reconfigure locales
   ```

## 🛡️ KAGE Panel için Gerekli Araçlar
1. **Nmap Kurulumu**
   ```bash
   sudo apt install -y nmap
   ```

2. **WhatWeb Kurulumu**
   ```bash
   sudo apt install -y whatweb
   ```

3. **Node.js Kurulumu**
   ```bash
   curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
   sudo apt install -y nodejs
   ```

4. **KAGE Panel Kurulumu**
   ```bash
   git clone https://github.com/kullanıcıadı/kage-panel
   cd kage-panel
   
   # Backend kurulumu
   cd backend
   npm install
   
   # Frontend kurulumu
   cd ../frontend
   npm install
   ```

## 🔍 Sorun Giderme
1. **Wireless Adaptör Sorunları**
   ```bash
   sudo apt install -y linux-headers-$(uname -r)
   sudo apt install -y firmware-*
   ```

2. **Ekran Çözünürlüğü Sorunları**
   ```bash
   sudo apt install -y xserver-xorg-video-all
   ```

## 📚 Faydalı Kaynaklar
- [Kali Linux Resmi Dokümantasyon](https://www.kali.org/docs/)
- [Kali Linux Tools](https://www.kali.org/tools/)
- [Kali Linux Forums](https://forums.kali.org/)

## 🔒 Güvenlik Notları
1. Root hesabı ile sürekli çalışmaktan kaçının
2. UFW veya iptables ile güvenlik duvarını yapılandırın
3. SSH servisini varsayılan porttan değiştirin
4. Güçlü şifreler kullanın
5. Sistemi düzenli olarak güncelleyin

## ⚠️ Yasal Uyarı
Kali Linux güçlü penetrasyon test araçları içerir. Bu araçları yalnızca:
- Yasal penetrasyon testlerinde
- Kendi sistemlerinizde
- İzin verilen sistemlerde kullanın

İzinsiz kullanım yasal sonuçlar doğurabilir. 