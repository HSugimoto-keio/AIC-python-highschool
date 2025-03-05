## Mac版

### パッケージマネージャ(Homebrew) インストール
```zsh
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
```zsh
$ brew update
```
```zsh
$ brew upgrade
```

### 処理系(Python) インストール＆設定
```zsh
$ brew install python
```
```zsh
$ python3 -m venv myenv
```
```zsh
$ source myenv/bin/activate
```

### 今回使用するGUIライブラリ(tkinter) インストール
```zsh
(myenv)$ brew install tcl-tk
```
```zsh
(myenv)$ echo 'export PATH="/opt/homebrew/opt/tcl-tk/bin:$PATH"' >> ~/.zshrc
```
```zsh
(myenv)$ echo 'export LDFLAGS="-L/opt/homebrew/opt/tcl-tk/lib"' >> ~/.zshrc
```
```zsh
(myenv)$ echo 'export CPPFLAGS="-I/opt/homebrew/opt/tcl-tk/include"' >> ~/.zshrc
```
```zsh
(myenv)$ echo 'export PKG_CONFIG_PATH="/opt/homebrew/opt/tcl-tk/lib/pkgconfig"' >> ~/.zshrc
```
```zsh
(myenv)$ source ~/.zshrc
```
```zsh
(myenv)$ python3 -m pip install pytk
```