<h1 align="center"> NVM (Node Version Manager) Kurulumu & Kullanımı</h1>

<p align="center">
  <img src="https://github.com/user-attachments/assets/a96dd5ca-3286-4e08-8303-577172a61761" width="500" alt="NVM Demo Görseli"/>
</p>

---

##  NVM Nedir?

**NVM (Node Version Manager)**, adından da anlaşılacağı gibi bir **Node.js sürüm yöneticisidir.**  
Bilgisayarına birden fazla **Node sürümünü aynı anda kurmanı**, aralarında kolayca geçiş yapmanı sağlar.  

Bu sayede her proje için ihtiyaç duyduğun **farklı Node.js versiyonlarını sorunsuz bir şekilde** yönetebilirsin.

Kısaca: `nvm use 16`, `nvm use 18` diyerek ortama ışınlanırsın.  
Sistemine karışmaz, root izin istemez, her şey kontrollü!

---

## Kurulum

### Linux & macOS İçin

#### Kurulum Scripti (cURL)

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
```

#### Alternatif: wget

```sh
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
```

 Kurulumdan sonra terminali yeniden başlatın veya elle kaynak dosyasını çalıştırın:

```sh
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
```

---

###  Windows İçin

**NVM-Windows kullanılır (resmi değil ama kararlı).**

1. [NVM-Windows Releases](https://github.com/coreybutler/nvm-windows/releases) sayfasına gidin  
2. En son `.exe` dosyasını indirin  
3. Kurulum adımlarını takip edin

>  Kurulum sırasında Node.js yolunu ve indirilecek dizini dikkatlice seçin.

---

## ⚙ NVM Komutları

| Komut | Açıklama |
|-------|----------|
| `nvm ls` | Yüklü Node.js sürümlerini listeler |
| `nvm ls-remote` | Kullanılabilir tüm sürümleri listeler |
| `nvm install <versiyon>` | Belirtilen Node.js sürümünü kurar |
| `nvm use <versiyon>` | O sürüme geçiş yapar |
| `nvm alias default <versiyon>` | Varsayılan sürümü belirler |

🧪Örnekler:

```sh
nvm install 18.17.0
nvm use 18.17.0
nvm alias default 18.17.0
```

---

##  Proje Bazlı Kullanım

Bir projeye `.nvmrc` adında bir dosya ekleyip içine şu satırı yazarsan:

```txt
18.17.0
```

Ardından terminalde bulunduğun klasörde:

```sh
nvm use
```

dediğinde otomatik olarak o sürüme geçer.  


---

## Avantajları

- 🌀 Projeler arası geçişte Node sürüm derdi yaşamazsın  
- 🧩 Global Node.js kurulumunu bozmaz  
- 🪄 Kolay, sade ve güvenli yönetim  
- 🧠 Sürüm uyumsuzluğu ve hata riskini minimuma indirir  

---

## Daha Fazla Bilgi İçin

🔗 [Resmi NVM GitHub Sayfası](https://github.com/nvm-sh/nvm)  
🔗 [NVM-Windows (coreybutler)](https://github.com/coreybutler/nvm-windows)

---

