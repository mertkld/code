
    h1, h2 {
      color: #2c3e50;
      font-family: Arial, sans-serif;
    }
    code {
      background-color: #f4f4f4;
      padding: 2px 4px;
      border-radius: 4px;
      font-family: Consolas, monospace;
    }
    pre {
      background: #eee;
      padding: 10px;
      border-radius: 5px;
    }
  </style>
</head>
<body>

<h1>🚀 Ortam Kurulum Rehberi</h1>
<p>Bu rehberde JavaScript için <code>nvm</code>, Python için <code>virtualenv</code>, <code>pyenv</code>, <code>miniconda</code> ve Windows ortamında Linux kullanmak için <code>WSL2</code> kurulumu detaylı şekilde anlatılmıştır.</p>

<h2>📦 JavaScript - NVM Kurulumu</h2>
<pre><code>curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
source ~/.bashrc
nvm install --lts
nvm use --lts
node -v
npm -v
</code></pre>

<h2>🐍 Python - virtualenv Kurulumu</h2>
<pre><code>pip install virtualenv
virtualenv venv
source venv/bin/activate  # Windows için: .\\venv\\Scripts\\activate
deactivate
</code></pre>

<h2>🧪 Python - pyenv Kurulumu</h2>
<pre><code>curl https://pyenv.run | bash

# .bashrc veya .zshrc içine ekle:
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv virtualenv-init -)"

# terminali yeniden başlat
pyenv install 3.11.7
pyenv global 3.11.7
python -V
</code></pre>

<h2>🔬 Python - Miniconda Kurulumu</h2>
<pre><code># İndir: https://docs.conda.io/en/latest/miniconda.html
bash Miniconda3-latest-Linux-x86_64.sh
conda create -n myenv python=3.11
conda activate myenv
conda deactivate
</code></pre>

<h2>🐧 WSL2 Kurulumu (Windows Subsystem for Linux)</h2>
<pre><code>wsl --install
wsl --set-default-version 2
wsl --list --online
wsl --install -d Ubuntu
wsl
</code></pre>

</body>
</html>
"""


file_path

