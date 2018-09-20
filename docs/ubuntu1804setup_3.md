ubuntu18.04LTSのセットアップメモ その３

jupyter-notebook等を試すためにvmを用意して諸々をインストールしたメモ

環境：Windows10のVirtualBoxのUbuntu18.04LTS

virtualboxの仮想マシンの設定  
　チップセットをICH9  
　準仮想化インターフェースをKVM→デフォルトに戻した  
　ビデオメモリを256  
　3Dアクセラレーションを有効→クソ重くなったので外した  

以前インストールした際のISOをまた使う  
最小インストール  
GuestAdditionsをインストール  
ソフトウェアの更新の設定を変えて必要なものを更新  

設定＞電源＞画面オフにするまでの時間  
設定＞プライバシー＞画面オフ後にロックするまでの時間  

sudo apt update  
anacondaのサイトからanacondaのshをダウンロード  
shに実行権限つけて実行  
インストール後にconda activateしたら  
.bashrcになんか追記しろと言われるので追記する  
conda activateするとconda環境になる  
anaconda-navigatorでanacondaの画面が起動  
終わったらconda deactivateでconda環境抜ける  


