# Flask를 이용하여 정적페이지 만들기
> Flask 프레임워크를 이해하기.
>> 관련 링크 : https://medium.com/@feedbotstar/python-flask-%ED%94%84%EB%A0%88%EC%9E%84%EC%9B%8C%ED%81%AC-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0-41c7c6e97d08

## keyword

### 1. virtualenv

- 시스템 독립적인 파이썬 개발환경을 만드는 도구.
- virtualenv로 프로젝트용 샌드박스를 생성하고 개발환경을 실행.
``` terminal
> pip3 install virtualenv
> virtualenv flaskapp
> cd flaskapp
> source bin/activate

# 그 다음 안전하게 Flask 설치
(flaskapp) > pip3 install flask
```

### 2. Jinja
- Python 웹 프레임워크인 Flask에 내장되어 있는 Template 엔진.
- LINK : https://jinja.palletsprojects.com/en/2.11.x/
- 참고 사이트 : https://velog.io/@decody/-Flask-Template%EC%97%90-Jinja2-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0
```python
# 변수나 표현식
{{ ... }} 

# if나 for같은 제어문
{% ... %}

# 주석
{# ... #}

```

## Flask 실행

#### 1. 실행방법 1
- 파일이름 `app.py` 로 설정
- 해당파일이 있는 root에서 `flask run` 실행

#### 2. 실행방법 2
- FLASK_APP 환경 변수 이용
- {실행파일}.py 파일이 있는 root에서 터미널 실행
```
> export FLASK_APP=hello.py
> flask run
```

#### 3. 실행방법 3
```python
# 실행되는 .py 파일 하단에 추가 
if __name__ == '__main__':
     app.run(debug=True)
```
- run 으로 실행 또는 `python {해당파일이름}.py` 명령어로 실행


