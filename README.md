# HttpRequestResponse

* get(self, url, params=None, headers=None)  
* post_form(self, url, data, headers=None)  
* post_json(self, url, data, headers=None)  
请求成功，返回响应结果的json解码json_r，和响应结果r  
json_r用来内容判断  
r用来响应码判断  
例如  
```python
if r.status_code==200:
            self.assertEqual('successed', json_r['reason'], "是状态吗")
```  
一个栗子
```python
import sys
sys.path.append('..')
from tools.getResponse import HttpRequestResponse
class MyTest(unittest.TestCase):
    def test_m4(self):
            
            # get 其他详见getResponse.py
            new_get = HttpRequestResponse()
            url = 'http://localhost:12306/book_info'
            params = {
                "bookname": "接口来自moco",
                "checkstatus": "on"
            }
            get_json = new_get.get(url, params=params)
            print("get_json---", get_json)
            if r.status_code==200:
                self.assertEqual('successed', get_json['reason'], "是状态吗")

```
---
