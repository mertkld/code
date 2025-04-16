Geliştirici Ortamları Kurulum Rehberi
Bu rehber, farklı programlama dilleri ve ortamları için kurulum ve kullanım bilgilerini içermektedir. Aşağıdaki konuları detaylı olarak bulabilirsiniz:
İçindekiler

JavaScript için NVM Kurulumu
Python için Virtualenv Kurulumu
Python için Pyenv Kurulumu
Miniconda Kurulumu ve Kullanımı
WSL (Windows Subsystem for Linux) Kurulumu

JavaScript için NVM Kurulumu
NVM (Node Version Manager), birden fazla Node.js sürümünü yönetmenize olanak tanıyan bir araçtır.
Linux ve macOS'ta Kurulum
bash# NVM'i kurmak için aşağıdaki komutu çalıştırın
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash

# veya wget kullanarak:
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
Windows'ta Kurulum
Windows için nvm-windows kullanabilirsiniz. Kurulum dosyasını GitHub'dan indirip çalıştırmanız yeterlidir.
Temel NVM Komutları
bash# Mevcut Node.js sürümlerini listeleme
nvm ls

# Yüklenebilir Node.js sürümlerini görüntüleme
nvm ls-remote

# Belirli bir Node.js sürümünü yükleme
nvm install 18.16.0

# Belirli bir sürüme geçiş yapma
nvm use 18.16.0

# Varsayılan Node.js sürümünü ayarlama
nvm alias default 18.16.0
Python için Virtualenv Kurulumu
Virtualenv, izole Python ortamları oluşturmanızı sağlayan bir araçtır.
Kurulum
bash# pip ile virtualenv kurulumu
pip install virtualenv
Kullanım
bash# Yeni bir sanal ortam oluşturma
virtualenv venv

# Windows'ta sanal ortamı aktifleştirme
venv\Scripts\activate

# Linux/macOS'ta sanal ortamı aktifleştirme
source venv/bin/activate

# Paket yükleme
pip install paket_adi

# Sanal ortamdan çıkma
deactivate
Python için Pyenv Kurulumu
Pyenv, birden fazla Python sürümünü yönetmenize olanak tanır.
Linux ve macOS'ta Kurulum
bash# Gerekli bağımlılıkları yükleme (Ubuntu/Debian için)
sudo apt-get update
sudo apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev \
libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
xz-utils tk-dev libffi-dev liblzma-dev python-openssl git

# pyenv kurulumu
curl https://pyenv.run | bash
Kurulumdan sonra .bashrc veya .zshrc dosyanıza aşağıdaki satırları ekleyin:
bashexport PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv init -)"
Temel Pyenv Komutları
bash# Yüklenebilir Python sürümlerini listeleme
pyenv install --list

# Belirli bir Python sürümünü yükleme
pyenv install 3.11.3

# Küresel Python sürümünü ayarlama
pyenv global 3.11.3

# Proje dizini için Python sürümünü ayarlama
pyenv local 3.11.3

# Yüklü Python sürümlerini listeleme
pyenv versions
Miniconda Kurulumu ve Kullanımı
Miniconda, Python paket ve ortam yönetimi için hafif bir çözümdür.
Kurulum
Windows:
Miniconda İndirme Sayfası'ndan kurulum dosyasını indirin ve çalıştırın.
Linux:
bash# Kurulum dosyasını indirme
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh

# Kurulumu çalıştırma
bash Miniconda3-latest-Linux-x86_64.sh
macOS:
bash# Kurulum dosyasını indirme
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh

# Kurulumu çalıştırma
bash Miniconda3-latest-MacOSX-x86_64.sh
Conda Ortamları ile Çalışma
bash# Yeni bir conda ortamı oluşturma
conda create --name myenv python=3.11

# Ortamı aktifleştirme
conda activate myenv

# Paket yükleme
conda install numpy pandas

# Ortamdan çıkma
conda deactivate

# Ortamları listeleme
conda env list

# Ortamı silme
conda env remove --name myenv
WSL Kurulumu
WSL (Windows Subsystem for Linux), Windows 10 ve 11'de Linux ortamını çalıştırmanıza olanak tanır.
WSL Kurulumu (Windows 10/11)

PowerShell'i yönetici olarak açın ve aşağıdaki komutu çalıştırın:

powershellwsl --install
Bu komut varsayılan olarak Ubuntu dağıtımını yükleyecektir.

Bilgisayarınızı yeniden başlatın.
Kurulumu tamamlayın: Bilgisayar yeniden başladıktan sonra, Ubuntu otomatik olarak açılacak ve kullanıcı adı ve şifre belirlemenizi isteyecektir.

Belirli Bir Linux Dağıtımı Yükleme
powershell# Mevcut dağıtımları görüntüleme
wsl --list --online

# Belirli bir dağıtımı yükleme (örneğin, Ubuntu 22.04)
wsl --install -d Ubuntu-22.04
WSL Komutları
powershell# Yüklü WSL dağıtımlarını görüntüleme
wsl --list

# Belirli bir dağıtımı başlatma
wsl -d Ubuntu-22.04

# WSL'yi kapatma
wsl --shutdown

# WSL sürümünü kontrol etme
wsl --status

# WSL 1'den WSL 2'ye geçiş yapma
wsl --set-version Ubuntu-22.04 2

# Varsayılan WSL sürümünü ayarlama
wsl --set-default-version 2

Bu rehber, geliştirme ortamlarınızı hazırlamanıza yardımcı olacak temel kurulum ve kullanım bilgilerini içermektedir. Herhangi bir sorunla karşılaşırsanız veya daha fazla bilgiye ihtiyaç duyarsanız, ilgili projelerin resmi dokümantasyonlarına başvurabilirsiniz.
