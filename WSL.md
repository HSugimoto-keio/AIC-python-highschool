## WSL版

### WSLのインストール
Powershellを**管理者権限**で開く
```powershell
> wsl --install
```
「正常に修了しました」が表示されたら、パソコンを再起動する。


起動したらWSLを起動。（ない場合はPowershellでwslと打つとwslの画面に行く）
最初の起動時にはwsl上のディストリビューション（厳密には正しくないが、パソコンの中に作った仮想的なコンピュータ）にアカウントとパスワードを作る必要がある。必要事項を書く。

例：

Enter new UNIX username: （使いたいユーザー名:username）

New password: (そのアカウントのパスワード)

Retype new password: (上とおなじパスワードを入力)

なお、パスワードは後々使うため忘れないようにすること。メモ帳でメモしても良い。

これが終わると次のような表示（今回は**基本の状態**とよぶ）になる

```bash
username@machinename:~$ 
```
基本の状態では$の左隣が~になっていることを必ず確認すること。

### フォルダの移動

展開済みの講義資料のファイルはそのままではwslが正しく読むことができない。仮想のコンピュータが読み取れるところに置く必要がある。
* エクスプローラ（バインダーみたいなマーク）を２つ広げ、片方は展開済みの講義資料のフォルダを、もう片方はLinux（ペンギンマーク）を開く。

* 講義資料をLinuxにドラッグアンドドロップする。

### Python仮想環境(venv) インストール＆設定

```bash
$ cd
```
```bash
$ sudo apt update -y
```
```bash
$ sudo apt install python3-pip python3-venv -y
```
```bash
$ python3 -m venv myenv
```
```bash
$ source myenv/bin/activate
```
### 今回使用するGUIライブラリ(tkinter) インストール
```bash
(myenv)$ sudo apt install python3-tk
```