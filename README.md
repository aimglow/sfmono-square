# sfmono-square
作者： [delphinus](https://github.com/delphinus/homebrew-sfmono-square)

[delphinus](https://github.com/delphinus/homebrew-sfmono-square)さんが作成してくれた、SF Mono Square.
僕にとっていろいろ試してきた中で史上最高のフォントだと感じています。

MacOS環境はもちろんのこと、開発環境として用意しているCodeServerすべてにインストールして大活用させていたいています。
感謝しかありません。

このリポジトリは、本家が提供しているBrewからインストールし、Linux環境やWindows環境にもインストールできるように、出来上がった*.otfファイルを配置しておくためのものです。

### MacOS環境
本家リポジトリ参照 (brewからインストール)
→ [homebrew-sfmono-square](https://github.com/delphinus/homebrew-sfmono-square)

### Windows環境
```
git clone git@github.com:taigamorikawa/sfmono-square.git
```
もしくは、Rawダウンロードを行い、*.otfファイルをダブルクリックでフォントブックにインストール

### Linux環境
* 全てのユーザに適用
```
git clone git@github.com:taigamorikawa/sfmono-square.git
cp -p sfmono-square/*.otf /usr/share/fonts/
fc-list -v
```
* 個別ユーザに適用
```
git clone git@github.com:taigamorikawa/sfmono-square.git
mkdir -p ~/.local/share/fonts/
cp -p sfmono-square/*.otf ~/.local/share/fonts/
fc-list -v
```
* Code Serverに適用
```
git clone git@github.com:taigamorikawa/sfmono-square.git

WKB_PATH="/usr/lib/code-server/lib/vscode/out/vs/workbench/"
mv sfmono-square $WKB_PATH
cd $WKB_PATH
mv sfmono-square fonts

cp -p workbench.web.main.css workbench.web.main.css.bak
sed -i '1i@import url\("fonts\/fonts.css"\);' workbench.web.main.css
systemctl restart code-server@[username].service
```
