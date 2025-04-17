<h2 align="center">🐍 Python pyenv Kurulumu ve Kullanımı</h2>

<p align="center">
  <img src="https://github.com/user-attachments/assets/7397de76-b7e5-4dae-8128-d95303527193" width="700" alt="pyenv Logo"/>
</p>



---

## 🧠 pyenv Nedir?

**pyenv**, birden fazla Python sürümünü sistemine kurmanı ve aralarında kolayca geçiş yapmanı sağlayan bir araçtır.

- Proje bazlı Python sürüm yönetimi sağlar  
- Sistemdeki varsayılan Python’a karışmaz  
- `python`, `python3`, `pip` gibi komutları otomatik yönlendirir

---

## 🛠️ Kurulum (Linux & macOS)

### 🔽 Otomatik Kurulum (cURL ile)

```sh
curl https://pyenv.run | bash
```

### ⚙️ Ortam Değişkenleri (Kurulum sonrası)

Aşağıdakileri `~/.bashrc`, `~/.zshrc` ya da kabuğuna göre uygun config dosyana ekle:

```sh
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv virtualenv-init -)"
```

👉 Ardından terminali yeniden başlat veya:

```sh
source ~/.bashrc
```

---

## 🪟 Windows için

Windows kullanıcıları için `pyenv` yerine önerilen araç:  
🔗 [pyenv-win GitHub](https://github.com/pyenv-win/pyenv-win)

Kurulum adımları orada detaylı açıklanmıştır.

---

## 🚀 Kullanım

### 📌 Python Sürümü Kur

```sh
pyenv install 3.11.8
```

### 🔁 Varsayılan Sürümü Ayarla

```sh
pyenv global 3.11.8
```

### 📦 Projeye Özel Sürüm Ayarla

Proje dizininde:

```sh
pyenv local 3.10.6
```

`.python-version` dosyası oluşturulur ve bulunduğun dizinde bu sürüm kullanılır.

---

## 🧪 Faydalı Komutlar

| Komut | Açıklama |
|-------|----------|
| `pyenv versions` | Yüklü sürümleri listeler |
| `pyenv install -l` | Kurulabilir sürümleri listeler |
| `pyenv uninstall <sürüm>` | Sürümü kaldırır |
| `pyenv doctor` | Kurulumu test eder (ek eklenti gerekebilir) |

---

## 📦 pyenv + virtualenv

```sh
# pyenv ile virtualenv kur
pyenv install 3.10.0
pyenv virtualenv 3.10.0 myenv

# Ortamı aktifleştir
pyenv activate myenv

# Ortamdan çık
pyenv deactivate
```

> 🔗 Daha fazla bilgi: [https://github.com/pyenv/pyenv](https://github.com/pyenv/pyenv)

---

<p align="center">
  <sub>Her projeye özel Python, her ortama özel düzen. 🐍</sub>
</p>
