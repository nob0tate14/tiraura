VirtualBoxのUbuntu18.04LTSをちょっとだけ使いやすくしたメモ

ワイドディスプレイでWindows10でVirtualBoxでUbuntuでEclipseだと  
タスクバーとかステータスバーとかタイトルバーとかなんちゃらバー的なもので高さが足りない。  
Windowsのタスクバーを横にしたが、いまいちだったので隠れるようにした。
VirtualBoxのメニューバーとステータスバーも非表示  
表示する場合は[右ctrl]+[home]  

VMを起動するたびにウインドウサイズが微妙なのでちょうどよいサイズを登録した。  
xrandr  
cvt 1400 1050  
sudo xrandr --newmode 上のコマンドの結果  

省電力のためにWindowsもUbuntuもダークテーマにした。  
ubuntuソフトウェアからgnome tweak toolをインストールして、暗い感じにする  
Eclipseも外観の設定でダークテーマにする(とりあえず標準版)  
若干見づらくなるので色の設定を微調整  
ツールバーのボタンを右縦に配置した  

デフォルトのviがしょぼかったのでvimをインストール  
sudo apt install vim  

ロック時間の調整  
設定＞電源＞画面オフにするまでの時間  
設定＞プライバシー＞画面オフ後にロックするまでの時間  
