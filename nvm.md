

# NVM (Node Version Manager) Kurulumu


**NVM (Node Version Manager), adından da anlaşılacağı gibi bir Node.js sürüm yöneticisidir.
Bilgisayarında birden fazla Node sürümünü aynı anda kurmanı, aralarında kolayca geçiş yapmanı sağlar.**

<p align="center">
  <img src="https://github.com/user-attachments/assets/a96dd5ca-3286-4e08-8303-577172a61761" width="500" alt="Demo Görseli"/>
</p>




## Linux ve macOS için Kurulum

### NVM kurulum scripti indirilir
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash

### veya wget ile
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
```sh
Kurulumdan sonra terminali yeniden başlatın veya aşağıdaki komutu çalıştırın:

export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
```
## Windows için Kurulum

**Windows'ta NVM-Windows'u kullanabilirsiniz:**
```sh
1. [NVM-Windows](https://github.com/coreybutler/nvm-windows/releases) adresinden en son sürümü indirin
2. İndirilen kurulum dosyasını çalıştırın
3. Kurulum adımlarını takip edin
```
## NVM Kullanımı

**Mevcut Node.js sürümlerini listele**
 ```sh
nvm ls
```
**Kullanılabilir Node.js sürümlerini listele**
 ```sh
nvm ls-remote
```
**Belirli bir Node.js sürümünü yükle**
 ```sh
nvm install 16.14.0
```
**Belirli bir sürüme geç**
 ```sh
nvm use 16.14.0
```
**Varsayılan Node.js sürümünü ayarla**
 ```sh
nvm alias default 16.14.0
```
