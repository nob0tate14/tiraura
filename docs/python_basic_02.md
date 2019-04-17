# プログラム初心者がpythonを学ぶ。またはpythonを題材にプログラムを学ぶ Part2
``` 
#例題１
import urllib.request
import urllib.parse
import json

def debug_print(p):
    pass
    print(p)

debug_print("0.----------")

p=input()
debug_print(f"入力は{p}です")
debug_print("1.----------")

ep=urllib.parse.quote(p)
debug_print(ep)
debug_print("3.----------")

base_url="http://ci.nii.ac.jp/books/opensearch/search?format=json&"
comp_url=f"{base_url}q={ep}"
debug_print(comp_url)
debug_print("4.----------")

req=urllib.request.Request(comp_url)
res=urllib.request.urlopen(req)

debug_print(res)
debug_print("5.----------")

res_cont=res.read().decode("utf8")
debug_print(res_cont)
debug_print("6.----------")

j_cont=json.loads(res_cont)

debug_print(j_cont)
debug_print("7.----------")

itms=j_cont["@graph"][0]["items"]
for itm in itms:
    try:
        print(f"書名：{itm['title']}　出版：{itm['dc:publisher']}")
    except Exception as e:
        print(e)

debug_print("8.----------")
``` 
``` 
#例題２
#http://weather.livedoor.com/forecast/rss/primary_area.xml
import urllib.request
import urllib.parse
import json

def debug_print(p):
    pass
    #print(p)

def get_area(p):
    dict_area ={"1":"016010","2":"130010","3":"230010"}
    ret=dict_area[p]
    return ret

print("札幌：１")
print("東京：２")
print("名古屋：３")

p=input("エリアを入力してください")
debug_print(f"入力は{p}です")
area=get_area(p)

ep=urllib.parse.quote(area)
base_url=f"http://weather.livedoor.com/forecast/webservice/json/v1?"
comp_url=f"{base_url}city={ep}"

req=urllib.request.Request(comp_url)
res=urllib.request.urlopen(req)

res_cont=res.read().decode("utf8")
j_cont=json.loads(res_cont)

print("----------")
print(f'{j_cont["title"]}')
print(f'{j_cont["forecasts"][0]["dateLabel"]}の天気：{j_cont["forecasts"][0]["telop"]}')
print(f'{j_cont["forecasts"][1]["dateLabel"]}の天気：{j_cont["forecasts"][1]["telop"]}')
print(f'説明：{j_cont["description"]["text"]}')
``` 
