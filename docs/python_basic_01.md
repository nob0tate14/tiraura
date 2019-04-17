# プログラム初心者がpythonを学ぶ。またはpythonを題材にプログラムを学ぶ。Part1

## Pythonとは  

特徴  
https://www.python.jp/pages/about.html  
コードの可読性  


https://ja.wikipedia.org/wiki/Python  
Ｃ言語との可読性の違い  



## pythonで何ができる  
https://ja.wikipedia.org/wiki/Python%E3%82%92%E4%BD%BF%E3%81%A3%E3%81%A6%E3%81%84%E3%82%8B%E8%A3%BD%E5%93%81%E3%81%82%E3%82%8B%E3%81%84%E3%81%AF%E3%82%BD%E3%83%95%E3%83%88%E3%82%A6%E3%82%A7%E3%82%A2%E3%81%AE%E4%B8%80%E8%A6%A7

youtube、instagram、dropbox  

用途  
データサイエンス、数値計算  
Webアプリケーション  
システム管理用スクリプト  

標準・外部ライブラリを読み込むことでいろんなことができる  
参考：標準ライブラリでできること  
https://docs.python.org/ja/3/library/index.html#library-index  


## pythonでプログラムを始めるには  

pythonの実行環境  
python2  
	2.7が最後　2020/1/1まで  
python3  
	現在は3.7  

簡単な実行  
PCにpythonをインストール  
コマンドラインからpythonを起動  
```
python -V
```
コマンドラインからの実行を試す（対話モード）  
```
python

print("test")

print(1+1)
```

コマンドラインの終了  
```
ctrl+d

exit()
```
pythonで計算してみる 
```
python
#足し算
1+1
#乗算
5**5
#円の面積
5*5*3.141592653589793
#円周率
import math
5*5*math.pi

import math
math.pi

5*5*math.pi


from math import pi

5*5*pi

p=pi

5*5*p
```

https://docs.python.org/ja/3/tutorial/introduction.html   





IDE(統合開発環境)   
eclipse   
pycharm   
visualstudio   

エディタ   
atom   

ディストリビューション   
anaconda    
 jupyter notebook anacondaに含まれているpythonの実行環境   

今回はanacondaを使用する  

virutalbox  
ubuntu18.04  
anaconda  
python3.7  
jupytrer notebook  



## python言語の基礎  
　プログラムを構成する要素  
　　リテラル  
　　変数  
　　演算子  
　　データ型  
　　式  
　　文（単純文、複合文）  
　　関数  

詳しくは  
https://docs.python.org/ja/3/reference/index.html  


■データ型  
数値  
　整数  
　ブール値（true・false）  
　実数  

シーケンス型  
　文字列  
　タプル  
　リスト  

マッピング型  
　辞書  


■式  
https://docs.python.org/ja/3/reference/expressions.html  
※比較演算以降  


■文（単純文、複合文）  




複合文をインデントで構成する  
if  

for  



■関数  
関数名  
引数  
戻り値  

