<h1 align="center">📚 Geliştirici Kurulum Rehberi 🚀</h1>

<p align="center">
  <i>“Kurulum yapmayı bilmeyen, kod yazamaz.” – Modern Zamanların Yazılımcısı</i>
</p>

---

## 🧠 İçindekiler

- [NVM ile Node.js Kurulumu](#nvm-ile-nodejs-kurulumu)
- [Python Virtualenv Kurulumu](#python-virtualenv-kurulumu)
- [Python venv Modülü](#python-venv-modülü)
- [Miniconda Kurulumu](#miniconda-kurulumu)
- [WSL (Windows Subsystem for Linux) Kurulumu](#wsl-windows-subsystem-for-linux-kurulumu)

---

## 🟩 NVM ile Node.js Kurulumu

📦 NVM (Node Version Manager), farklı Node sürümlerini aynı sistemde yönetmeni sağlar. Projeden projeye geçerken versiyon sorunları yaşamazsın.

### 🔧 Kurulum

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
Kurulumdan sonra terminale şunu ekle:
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
✅ Node.js Kur
nvm install --lts
nvm use --lts
🐍 Python Virtualenv Kurulumu
🔧 Kurulum
pip install virtualenv
🧪 Ortam Oluştur
virtualenv myenv
source myenv/bin/activate  # Linux/macOS
.\myenv\Scripts\activate   # Windows
🧬 Python venv Modülü
Python 3.3+ ile gelen dahili araç. Ekstra modül gerekmez.

🚀 Kullanım
python3 -m venv myenv
source myenv/bin/activate  # Linux/macOS
.\myenv\Scripts\activate   # Windows
🍃 Miniconda Kurulumu
Anaconda’nın hafif versiyonu. Bilimsel işler, ML, veri bilimi için candır.

🔽 İndir
👉 Miniconda İndir

🧪 Ortam Oluştur
conda create --name myenv python=3.11
conda activate myenv

🧱 WSL (Windows Subsystem for Linux) Kurulumu
Windows’ta Linux ortamı. Yani iki dünyanın da en iyisi. Batman vs Ironman gibi.

🏁 Kurulum

wsl --install
Eğer hata alırsan:

wsl --set-default-version 2

🐧 Dağıtım Seç

wsl --list --online
wsl --install -d Ubuntu

