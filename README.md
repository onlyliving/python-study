# Flask Study




## Python Web Framework Type
- 플라스크(Flask)
- 장고(django)

## Flask VS Django
#### 1. 플라스크
    * 특징 : 입문이나 학습, 프로토타입 서버에 적합하다.
    * 이유
        * micro web framework. 즉, 정말 필요한 것만, 최소한으로 제공
        * 나머지 필요한 것은 추가적으로 설치해야 함.(extension)
        * 서비스를 제공하게 된다면, 추가적으로 설치하는 라이브러리에서 문제가 생길 여지가 있다.
        
#### 2. 장고
    * 특징 : 웹 서비스 구축에 적합하다.
    * 이유
        * 장고를 설치하게 되면, 모든 것이 제공된다. (따로 설치할 필요가 없다.)
        * 장고의 단점으로는 웹서버가 어떻게 동작되는지 알 방법이 없기 때문에, 입문/학습용으로 좋지 않다.
        


## Flask
* Python의 마이크로 웹 프레임워크.
* 다양한 웹 엔진과 붙여서 쓸 수 있고, 가볍기도 해서 Django와 같이 쓰는 경우도 있다. 코드도 비교적 단순하고, 특히 API 서버를 만들기에 매우 편리하다. (관련된 확장 기능들이 많기 때문)

```python
from flask import Flask
app = Flask(__name__)

@app.route("/")
def hello_world():
 return "Hello, World!"

@app.route('/user/<userName>') # URL뒤에 <>을 이용해 가변 경로를 적는다
def hello_user(userName):
    return 'Hello, %s'%(userName)

if __name__ == "__main__":
    app.run()
```

### Flask 사용처
- Pinterset : API에 쓰임
- reddit

### Flask 설치 방법
```
pip install -U Flask
```
정확한 설치 방법 : https://pypi.org/project/Flask/

### Flask 문서
https://flask.palletsprojects.com/en/1.1.x/

## 참조 사이트
- 나무위키 : https://namu.wiki/w/Flask
