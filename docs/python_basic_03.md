# プログラム初心者がpythonを学ぶ。またはpythonを題材にプログラムを学ぶ Part3

twitterのAPIを利用してみる。     
1.twitterの開発者アカウントを作成  
2.twitter-apiのアクセスキーを取得  
3.twitter-apiを利用  

config.py  
```
CONSUMER_KEY = "xxx"
CONSUMER_SECRET = "xxx"
ACCESS_TOKEN = "xxx-xxx"
ACCESS_TOKEN_SECRET = "xxx"
``` 

認証
``` 
import json, config
from requests_oauthlib import OAuth1Session

CK = config.CONSUMER_KEY
CS = config.CONSUMER_SECRET
AT = config.ACCESS_TOKEN
ATS = config.ACCESS_TOKEN_SECRET
twitter = OAuth1Session(CK, CS, AT, ATS)
print(twitter)
``` 

自分のツイートを取得
``` 
# 自分のツイートを取得
def get_timeline(count):
    url = "https://api.twitter.com/1.1/statuses/user_timeline.json"

    params ={'count' : count}
    res = twitter.get(url, params = params)
    print(res)
    print(res.text)
    if res.status_code == 200:
        timeline = json.loads(res.text)
        return timeline
    else:
        print("Failed: %d" % res.status_code)

tw_list = get_timeline(10)

for tw in tw_list:
    print('*******************************************')
    print(tw['user']['name']+'::'+tw['text'])
    print(tw['created_at'])
``` 

ツイートの画像を表示
``` 
import matplotlib.pyplot as plt
import urllib
import io
from PIL import Image

# ツイートの画像を表示
def show_image(tweet):
    try:
        media_list = tweet['extended_entities']['media']
        for media in media_list:
            img_url = media['media_url']
            print(f"IMAGE URL:{img_url}")

            res = urllib.request.urlopen(img_url)
            img = res.read()
            f = io.BytesIO(img)
            img = Image.open(f)

            plt.imshow(img)
            plt.show()

    except Exception as e:
        print(f"error:{e}")

tw_list = get_timeline(10)
for tweet in tw_list:
    show_image(tweet)
``` 

ツイートを検索
``` 
# ツイートを検索
def search_tweet(search_word,count):
    url = "https://api.twitter.com/1.1/search/tweets.json"
    params = {'q':search_word,
              'count':count
          }
    res = twitter.get(url, params = params)
    timeline = json.loads(res.text)
    return timeline

p=input("検索キーワードを入力してください:")

tw_list = search_tweet(p,10)
#print(tw_list)
for tweet in tw_list['statuses']:
    show_image(tweet)
``` 
