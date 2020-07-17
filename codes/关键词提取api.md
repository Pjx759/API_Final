# 关键词提取api代码展示
## 一、使用平台
* 选择了讯飞平台的关键词提取api
```
import time
import urllib.request
import urllib.parse
import json
import hashlib
import base64
url ="http://ltpapi.xfyun.cn/v1/ke"
x_appid = "5f0d50fe"   # 使用自己的appid
api_key = "a04a3a7cf727d9027f3dd5e659d925bb"
#语言文本
TEXT="晚饭后记得还要使用一次口服液"
def main():
    body = urllib.parse.urlencode({'text': TEXT}).encode('utf-8')
    param = {"type": "dependent"}
    x_param = base64.b64encode(json.dumps(param).replace(' ', '').encode('utf-8'))
    x_time = str(int(time.time()))
    x_checksum = hashlib.md5(api_key.encode('utf-8') + str(x_time).encode('utf-8') + x_param).hexdigest()
    x_header = {'X-Appid': x_appid,
                'X-CurTime': x_time,
                'X-Param': x_param,
                'X-CheckSum': x_checksum}
    req = urllib.request.Request(url, body, x_header)
    result = urllib.request.urlopen(req)
    result = result.read()
    print(result.decode('utf-8'))
    return
if __name__ == '__main__':
    main()
```
* 提取结果
```
{"code":"0","data":{"ke":[{"score":"0.749","word":"口服液"},{"score":"0.700","word":"晚饭"},{"score":"0.602","word":"使用"},{"score":"0.559","word":"记得"},{"score":"0.557","word":"还要"}]},"desc":"success","sid":"ltp007e12bb@dxa81c1268a1d4000100"}
```

> 讯飞关键词提取可以90%提取出关键词语
* 讯飞关键词提取可以在官网找到官方使用文档进行调用操作
