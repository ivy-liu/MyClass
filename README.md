# HttpRequestResponse
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
            self.assertEqual('successed',get_json['reason'],"是状态吗")

```