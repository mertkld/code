
<h1 align="center"> Miniconda Kurulumu & Kullanımı</h1>  
<p align="center">  
  <img src="https://repository-images.githubusercontent.com/11167550/6b3b7580-bac8-11ea-893e-f646551f4a70" width="500" alt="Miniconda Demo Görseli"/>
</p>  

---

## Miniconda Nedir?

**Miniconda**, Anaconda'nın daha sade, daha hafif bir versiyonudur.  
Sadece temel **Conda paket yöneticisi**, Python ve birkaç temel araçla gelir.  

> Koca bir yükleme yerine **minimalist, hızlı ve özelleştirilebilir bir ortam** isteyenlerin tercihi.

---

## Kurulum

### Linux & macOS İçin

#### 1. Script ile Kurulum (64-bit)

\`\`\`sh
# Python 3.11 içeren Miniconda sürümünü indir
wget https://repo.anaconda.com/miniconda/Miniconda3-py311_24.1.2-0-Linux-x86_64.sh

# Script'e çalıştırma izni ver ve çalıştır
chmod +x Miniconda3-py311_24.1.2-0-Linux-x86_64.sh
./Miniconda3-py311_24.1.2-0-Linux-x86_64.sh
\`\`\`

Kurulum sırasında:

- Lisans sözleşmesini onayla  
- Kurulum dizinini seç  
- \`conda init\` sorusuna \`yes\` diyerek otomatik yapılandırmayı yap  

Sonrasında terminali yeniden başlat. 🎯

---

### Windows İçin

1. [Miniconda Windows Installer (64-bit)](https://docs.conda.io/en/latest/miniconda.html#windows-installers) bağlantısına tıkla  
2. En son \`.exe\` dosyasını indir  
3. Kurulum sırasında:

   - “Add Miniconda to PATH” seçeneğini **isteğe bağlı olarak** işaretle (genellikle önerilmez)  
   - “Register Miniconda as default Python” seçeneğini işaretle  

> Ardından Windows Terminal’i aç ve kontrol et:  
\`\`\`sh
conda --version
\`\`\`

---

## Temel Conda Komutları

| Komut | Açıklama |
|-------|----------|
| \`conda create -n <isim> python=3.11\` | Yeni bir ortam oluşturur |
| \`conda activate <isim>\` | Ortamı aktif eder |
| \`conda deactivate\` | Aktif ortamdan çıkar |
| \`conda install <paket>\` | Paket kurar |
| \`conda env list\` | Tüm ortamları listeler |
| \`conda remove -n <isim> --all\` | Ortamı tamamen siler |

---

## Proje Bazlı Kullanım

Her proje için ayrı bir ortam = **sıfır sürüm çatışması, maksimum huzur**

Örnek:

\`\`\`sh
conda create -n proje1 python=3.10
conda activate proje1
\`\`\`

\`.env\` veya \`environment.yml\` dosyası ile daha profesyonel bir yaklaşım da mümkün.  

---

## Avantajları

- Hafif, hızlı, sade 🪶  
- Python sürümleri arasında geçiş kolay  
- Sanal ortamlar izole = projeler arası güvenlik  
- Anaconda gibi dev bir yapı yerine “gerektiği kadar” yük  

---

## Daha Fazla Bilgi İçin

🔗 [Miniconda Resmi Dokümantasyonu](https://docs.conda.io/en/latest/miniconda.html)  
🔗 [Conda Komut Referansı](https://docs.conda.io/projects/conda/en/latest/commands.html)  

---

Hazırsan conda dünyasına adım at, hafiflik senin yeni süper gücün 🧙‍♂️  
Bir terminal, bir miniconda ve sen...  
Gerisi sadece \`conda activate\` ✨

---

## Windows İçin Detaylı Kurulum

### 1. Miniconda İndir

🔗 [Miniconda Windows Installer (64-bit)](https://docs.conda.io/en/latest/miniconda.html#windows-installers)  
Sayfadan Python 3.x sürümünü içeren `.exe` dosyasını indir.

### 2. Kurulumu Başlat

İndirilen `.exe` dosyasına çift tıkla ve adımları takip et:

- **Welcome** ekranında "Next"  
- **License Agreement** → "I Agree"  
- **Installation Type** → "Just Me" seç (genel sistem değişikliği istemiyorsan)  
- **Install Location** → Kendi klasörünü seçebilir veya varsayılanı kullanabilirsin  
- **Advanced Options** kısmında:
  - ✔ “Add Miniconda3 to my PATH environment variable” **işaretleme (önerilmez)**  
  - ✔ “Register Miniconda3 as the system Python 3.x” → **işaretle**

Kurulum tamamlandıktan sonra:

### 3. Başlat ve Kontrol Et

Başlat menüsünden “Anaconda Prompt” veya “Miniconda Prompt”u aç.

Kontrol etmek için:

```sh
conda --version
```

Her şey doğruysa sürüm numarasını görürsün.

### 4. Ortam Oluştur ve Kullan

```sh
conda create -n myenv python=3.11
conda activate myenv
```

Artık bu ortam içinde Python projelerini güvenle çalıştırabilirsin 🔒🐍

---

