# Yazılım Geliştirme Ortamları Kurulum Rehberi

Bu rehber, JavaScript için NVM, Python için virtualenv ve pyenv, Miniconda ve WSL kurulumlarını adım adım anlatmaktadır.

## İçindekiler
- [NVM (Node Version Manager) Kurulumu](#nvm-node-version-manager-kurulumu)
- [Python virtualenv Kurulumu](#python-virtualenv-kurulumu)
- [Python pyenv Kurulumu](#python-pyenv-kurulumu)
- [Miniconda Kurulumu](#miniconda-kurulumu)
- [WSL (Windows Subsystem for Linux) Kurulumu](#wsl-windows-subsystem-for-linux-kurulumu)

## NVM (Node Version Manager) Kurulumu

NVM, birden fazla Node.js sürümünü yönetmenize olanak tanıyan bir araçtır.

### Linux ve macOS için Kurulum

# NVM kurulum scripti indirilir
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash

# veya wget ile
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash

Kurulumdan sonra terminali yeniden başlatın veya aşağıdaki komutu çalıştırın:

export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"

### Windows için Kurulum

Windows'ta NVM-Windows'u kullanabilirsiniz:

1. [NVM-Windows](https://github.com/coreybutler/nvm-windows/releases) adresinden en son sürümü indirin
2. İndirilen kurulum dosyasını çalıştırın
3. Kurulum adımlarını takip edin

### NVM Kullanımı

# Mevcut Node.js sürümlerini listele
nvm ls

# Kullanılabilir Node.js sürümlerini listele
nvm ls-remote

# Belirli bir Node.js sürümünü yükle
nvm install 16.14.0

# Belirli bir sürüme geç
nvm use 16.14.0

# Varsayılan Node.js sürümünü ayarla
nvm alias default 16.14.0

## Python virtualenv Kurulumu

virtualenv, izole Python ortamları oluşturmanıza olanak tanır.

### Kurulum
```sh
# pip ile virtualenv kurulumu
pip install virtualenv
```

### Kullanım
```sh
# Yeni bir sanal ortam oluştur
virtualenv myenv

# Sanal ortamı etkinleştir (Linux/macOS)
source myenv/bin/activate

# Sanal ortamı etkinleştir (Windows)
myenv\Scripts\activate

# Sanal ortamı devre dışı bırak
deactivate
```
## Python pyenv Kurulumu

pyenv, birden fazla Python sürümünü yönetmenize olanak tanır.

### Linux ve macOS için Kurulum

# Gerekli bağımlılıkları kur (Ubuntu/Debian)
sudo apt-get update
sudo apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl

# pyenv kurulumu
curl https://pyenv.run | bash

Kurulumdan sonra .bashrc veya .zshrc dosyanıza aşağıdaki satırları ekleyin:

export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv init -)"

### Windows için Kurulum

Windows için pyenv-win kullanabilirsiniz:

1. PowerShell'i yönetici olarak açın
2. Aşağıdaki komutu çalıştırın:

Invoke-WebRequest -UseBasicParsing -Uri "https://raw.githubusercontent.com/pyenv-win/pyenv-win/master/pyenv-win/install-pyenv-win.ps1" -OutFile "./install-pyenv-win.ps1"; &"./install-pyenv-win.ps1"

### pyenv Kullanımı

# Kullanılabilir Python sürümlerini listele
pyenv install --list

# Belirli bir Python sürümünü yükle
pyenv install 3.9.10

# Global Python sürümünü ayarla
pyenv global 3.9.10

# Yerel Python sürümünü ayarla (proje bazlı)
pyenv local 3.9.10

# Mevcut Python sürümünü kontrol et
pyenv version

## Miniconda Kurulumu

Miniconda, Conda paket yöneticisinin minimal kurulumudur.

### Linux için Kurulum

# İndirme
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O miniconda.sh

# Kurulum
bash miniconda.sh -b -p $HOME/miniconda

# Başlangıçta conda'yı etkinleştir
eval "$($HOME/miniconda/bin/conda shell.bash hook)"

# Conda'yı otomatik olarak başlatma ayarı
conda config --set auto_activate_base false

### macOS için Kurulum

# İndirme
curl https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh -o miniconda.sh

# Kurulum
bash miniconda.sh -b -p $HOME/miniconda

# Başlangıçta conda'yı etkinleştir
eval "$($HOME/miniconda/bin/conda shell.bash hook)"

### Windows için Kurulum

1. [Miniconda](https://docs.conda.io/en/latest/miniconda.html) web sitesinden Windows için kurulum dosyasını indirin
2. İndirilen .exe dosyasını çalıştırın ve kurulum adımlarını takip edin

### Miniconda Kullanımı

# Yeni bir Conda ortamı oluştur
conda create --name myenv python=3.9

# Ortamı etkinleştir
conda activate myenv

# Ortamı devre dışı bırak
conda deactivate

# Paket yükleme
conda install numpy pandas

# Ortamı silme
conda env remove --name myenv

## WSL (Windows Subsystem for Linux) Kurulumu

WSL, Windows üzerinde Linux komut satırı araçlarını ve uygulamalarını çalıştırmanıza olanak tanır.

### Kurulum (WSL 2)

1. Windows PowerShell'i yönetici olarak açın

2. WSL'yi etkinleştirin:

dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

3. Sanal Makine özelliğini etkinleştirin:

dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

4. Bilgisayarınızı yeniden başlatın

5. Linux çekirdek güncellemesini indirin ve yükleyin:
   - [WSL2 Linux çekirdek güncelleme paketi](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)

6. WSL 2'yi varsayılan sürüm olarak ayarlayın:

wsl --set-default-version 2

7. Microsoft Store'dan bir Linux dağıtımı yükleyin (Ubuntu, Debian, vb.)

### WSL Temel Komutları

# Mevcut WSL dağıtımlarını listele
wsl --list --verbose

# Belirli bir dağıtımı başlat
wsl -d Ubuntu

# Belirli bir dağıtımı varsayılan yap
wsl --set-default Ubuntu

# WSL'yi kapat
wsl --shutdown

# WSL dağıtımını silme
wsl --unregister Ubuntu

---

Bu rehberi kendi projelerinize göre düzenleyebilirsiniz. Her bir aracın versiyonları ve komutları güncellenebilir, bu nedenle kurulum öncesinde resmi dokümantasyonu kontrol etmeniz önerilir.

--nvm list 
