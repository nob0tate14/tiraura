ubuntu18.04LTSのセットアップメモ その４

ディスク容量の増加

環境：Windows10のVirtualBoxのUbuntu18.04LTS

使ってたら残り0と言われた。  
ゴミ箱は空だった。  
ダウンロードフォルダにanacondaがあったので削除した。  
シャットダウン  
仮想メディアマネージャーでディスクサイズを20Gにした。  
起動  
gpartedインストール  
sudo apt install gparted  
gparted起動  
ubuntu18.04のデフォルトインストールではswap領域はパーティションではなくファイルになっており割り当て済みのパーティションは一つだけだった
いっぱいまで広げて適用  
