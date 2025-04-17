## 🐍 Python Virtual Environment (Sanal Ortam) Kurulumu

Python projelerinde bağımlılıkları izole tutmak için **virtual environment** kullanmak büyük önem taşır.  
Her projeye özel bir ortam oluşturarak, paketlerin çakışmasını engelleyebilirsin.

---

### ✅ 1. `venv` ile Sanal Ortam Kurulumu (Python 3.3+)

```sh
# Ortamı oluştur
python3 -m venv venv

# Ortamı aktifleştir
# Linux/macOS
source venv/bin/activate

# Windows
venv\Scripts\activate

# Ortamdan çıkmak için
deactivate
```

> 🔍 `venv`, Python’ın yerleşik modülüdür. Harici kurulum gerekmez.

---

### 🚀 2. `virtualenv` ile Sanal Ortam (Daha Esnek)

```sh
# Kurulum
pip install virtualenv

# Ortamı oluştur
virtualenv venv

# Ortamı aktifleştir
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
```

> ⚙️ `virtualenv`, eski Python sürümleriyle uyumludur ve daha fazla kontrol sunar.

---

### 💡 Notlar

- Sanal ortamda olduğunda terminal prompt'unda genellikle `(venv)` gibi bir ibare görünür.
- Ortam aktifken `pip install` komutları sadece o ortama kurulum yapar.
- Her projede bir `venv/` klasörü oluşturmak, iyi bir geliştirici alışkanlığıdır. 🧠

---

### 📦 `.gitignore` Hatırlatması

Sanal ortam klasörünü Git'e dahil etmemelisin. `.gitignore` dosyana şunu ekle:

```
venv/
```

---

### 📁 Proje Yapısı Örneği

```plaintext
my-project/
├── venv/               ← Sanal ortam (Git'e eklenmez)
├── requirements.txt    ← Paket listesi
├── main.py
└── README.md
```

---

### 📌 Ekstra: Paketleri Kaydetmek ve Yüklemek

```sh
# Tüm kurulu paketleri requirements.txt'ye yaz
pip freeze > requirements.txt

# requirements.txt'den paketleri yükle
pip install -r requirements.txt
```

---

<p align="center">
  <sub>Python ortamını temiz tut. Her proje kendi kum havuzunda oynasın 🏖️</sub>
</p>