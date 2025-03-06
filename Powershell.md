## PowerShell版

### 事前設定
これは仮想環境が実行できるようにするための設定
（Powershellでやる人はvenvを使う必要は今回はないため、もしできなかった場合は仮想環境に関する処理はしないで続行することにする。）

管理者権限でPowershellを起動し、以下のコマンドを実行する。
```powershell
> PowerShell Set-ExecutionPolicy RemoteSigned
```
実行できたらバツボタンで抜ける


### 処理系(Python) インストール
まず次のリンクを開き、インストーラをダウンロードしクリック。

[Python](https://www.python.org/downloads/windows/)

今回はLatest Python3 Release - Python 3.13.2を選択。（厳密には機種によるが、）FilesのWindows installer (64-bit)を選択。exeファイルを管理者権限で実行する。

* もし管理者権限の実行ができない等がある場合は貸出PCに切り替える必要があるのでTAに連絡

インストーラが立ち上がったら下の方にある **「Add Python to PATH」のチェックボックスにチェックし**、「Install Now」をクリック


（他はこだわりがなければ全てデフォルトの設定で画面の指示に従い、インストールが終了するのを待つ）

インストールが終了したらPowerShellを起動し、次のコマンドを実行し、内容を確認する。

```powershell
> python3 --version
```
このときにPython3.13.2が表示されていれば正常。

されていない場合は、インストーラをもう一度起動し、アンインストールしてからもう一度順番にやり直す。

### Python用パッケージマネージャ(pip)　インストール
```powershell
> python3 -m ensurepip --default-pip
```

### Python用仮想環境(venv)

```powershell
> python3 -m venv myenv
```
```powershell
> myenv\Scripts\Activate
```


### 今回使用するGUIライブラリ(tkinter) インストール

```powershell
(myenv)> python3 -m pip install pytk
```