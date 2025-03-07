# AIC-python-highschool

## 資料へのリンク

### [講義資料はこちらにあります。](https://drive.google.com/drive/folders/1pCcRNl8uMgQS5kGeErFf_4HnILDUw7eY)

## 環境設定のコマンド

最終的なゴールについては全て同じ。次のコマンドでポップアウトが正しく出力されたらTAを呼び確認する。
```bash
$ python3 -m tkinter
```

## 共通操作：エディタ(Visual Studio Code) インストール

[VSCode](https://code.visualstudio.com/download)から対応するOSのインストーラをダウンロードし実行する。

同意するところは同意し、それ以外はデフォルトの設定で進める。

ここから先はそれぞれでやることが異なるため、先のリンクで確認すること。

## 共通操作 : 講義資料の展開
説明の都合上、必ずデスクトップ上に講義資料のzipファイルを持ってきて、その場で展開する。

## Windows (PowerShell): 初級者向け
[PowerShell](Powershell.md)

## Windows (Windows Subsystem for Linux): やや中級者向け
[WSL](./WSL.md)

## Mac
[Mac](./Mac.md)または[Mac_pyenv](./Mac_pyenv.md)


## 設定後の実行方法（pyenvを使用しない場合）
前提として、仮想環境で実行することを想定している。
開いているシェルの先頭に(myenv)が付いていない時は仮想環境ではないため仮想環境にする必要がある。

Powershellの場合
```powershell
> myenv\Scripts\Activate
```
WSL Macの場合
```bash
$ myenv/bin/activate
```

なお、終了するときはどちらも次のコマンドで修了しもとのシェルに戻る
```bash
deactivate
```
基本的には作業が終わったらdeactivateを行うように心掛ける。


## プログラム実行時
基本的には仮想環境下で次のコマンドで実行できる。(以下はtennisの場合)

Windowsの場合
```powershell
(myenv)> python3 reversi.py
```

Mac の場合
```bash
(myenv)$ python3 reversi.py
```

Mac_pyenvの場合
```bash
python reversi.py
```

WSLの場合
```bash
(myenv) $ python3 reversi.py
```
