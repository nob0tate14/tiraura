VirtualBoxのubuntu18.04LTSにEclipseとPython開発環境をセットアップしたメモ

sudo apt install openjdk-8-jdk  

Eclipseダウンロード  
pleiadesからプラグインダウンロード

Eclipse解凍  
Eclipse起動確認して一旦終了  
プラグイン解凍してEclipseのフォルダに入れる  
eclipse.ini修正  

EclipseをDockに登録できるようにする  
/usr/share/applicationsにeclipse.desktopを作成  

eclipse -cleanで起動  


python確認  
python3 -V  
Python 3.6.6  

pip確認  
which pip3  
なければインストール  
sudo apt install python3-pip  
確認  
python3 -m pip -V  
pip 9.0.1 from /usr/lib/python3/dist-packages (python 3.6)  
which pip3  
/usr/bin/pip3  

Eclipse上でpydevをインストール  
Pythonインタープリター追加  
