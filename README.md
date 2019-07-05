# NPM 설치

```javascript
npm install --save express morgan body-parser
```

`express`
웹 서버에서 필요한 대부분 기능이 이미 구현되어 있는 웹 프레임 워크

`morgan`
로깅 미들웨어 - 상세하게 로깅 된다.

`body-parser`
JSON 형태 데이터 파싱

# Nodemon 설치

```javascript
npm install -g nodemon
```

명령어에 서버 시작하고 코드가 수정이 되었을 때
node main.js 를 수동으로 재시작을 해줘야 했다.
수정되어도 자동으로 재시작해주는 nodemon <br>

(-g) : 글로벌로 설치하면 터미널에서 직접 실행 할 수 있다.

예제 확인 = `npm repo nodemon`


# cmd 실행

Nodemon 설치하지 않았을 때 실행 **node main.js**
Nodemon 설치 했을 때 실행 **nodemon main.js**

<br>


### main.js
```javascript
app.use('/', express.static('public'));

app.get('/', function(req,res){
  res.send('Hello World');
});
```

**먼저 작성한 코드가 우선권을 갖는다.**

HTML, 이미지, CSS, JavaScript 이런 파일들을
브라우저에서 접근할 수 있도록 제공해주는 것

`app.use('/', express.static('public'));` <br>

Express 에 내장된 static 이라는 미들웨어를 사용하면 된다.

첫번째 파라미터 '/' 경로를 들어왔을 때 	
public 디렉토리에 접근할 수 있게 해줘라고 설정하는 것이다.
