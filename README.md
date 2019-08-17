# HttpRequestResponse
```python
# get
new_get = HttpRequestResponse()
url = 'http://localhost:12306/book_info'
params = {
    "bookname": "接口来自moco",
    "checkstatus": "on"
}
get_json = new_get.get(url, params=params)
print("get_json---", get_json)

# post_form
newForm = HttpRequestResponse()
url = "http://localhost:12306/login1"
headers = {
    "Content-Type": "application/x-www-form-urlencoded"
}
data = {
    "username": "xiaoming",
    "pwd": "123456"
}
form_json=newForm.post_form(url,data=data,headers=headers)
print("form_json---",form_json)

#post_json
newJson = HttpRequestResponse()
url = "http://localhost:12306/login2"
headers = {
    "Content-Type": "application/json"
}
data = {
    "username": "xiaoqiang",
    "pwd": "123456"
}
json_json=newJson.post_json(url,data,headers)
print("json_json---",json_json)

```