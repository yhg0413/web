# 2.1 HTML5 기본용어 정리
    - 태그 , 요소, 속성

## 2.1.1 태그와 요소
    태그 : html 페이지에서 객체를 만들 때 사용하는 것.
    일부 태그는 태그 안에 다른 태그를 넣을 수 있음 반대도 가능
    EX > <h1></h1> <br/>
## 2.1.2 속성
    태그에 추가 정보를 부여할 때 사용
    ```<h1 title="header">Hello HTML5</h1>```
## 2.1.3 주석
    <!-- 내용 -->

# 2.2 HTML5 페이지 구조
    >>code2-1
    - <!DOCTYPE html> -> 웹 브라우저가 현재 웹페이자가 HTML5문서임을 인식하게 만들어 준다. 반드시 가장 청 번째 줄에 있어야 한다.
    
    - <html> 모든 HTML 페이지의 루트 요소이다. 모든 HTML 태그는 <html> 태그의 내부에 작성한다.
    <html lang = 'ko'> 
    lang 한국 = ko , 미국 = en , 일본 = ja, 러시아어 = ru, 중국 = zh, 독일어 = de,


    - head 태그는 body태그에서 필요한 스타일시트와 자바스크립트를 제공하는데 사용함
    1. meta     웹 페이지에 추가 정보를 전달
    2. title    웹 페이지의 제목
    3. script   웹 페이지에 스크립트를 추가
    4. link     웹 페이지에 다른 파일을 추가
    5. style    웹 페이지에 스타일시트를 추가
    6. base     웹 페이지의 기본 경로를 지정



# 2.3 글자 태그

##  2.3.1 제목 글자 태그
    <h1> ~ <h6> 크기순으로 있음

##  2.3.2 본문 글자 태그
    <p>내용</p>
    <br> 개행태그
    <hr> 수평 줄 태그

##  2.3.3 앵커 태그

- a  : 앵커 태그
  - 속성 : herf 이동하고자 하는 웹페이지를 지정

> #### 코드 2-6

```html
<!DOCTYPE html>
<html>
    <title>HTML TEXT basic Page</title>
</html>
<body>
    <a herf="http://hanbit.co.kr">Hanbit</a>
</body>
```

- a 태그에 반드시 href 속성을 입력해야한다 이동하지 않을 a 태그를 만들 때는 href 속성에 #을 준다

#### 페이지 내부 이동

- a태그를 이용하면 현재 페이지 내부에서 원하는 장소로 이동 할 수 있다. 이때는 원하는 장소에 id 속성을 부여한다

```html
<a href="#alpha">Move to Alpah</a>
```

###### id속성이 중복 될 경우에는 먼저 나오는 태그로 이동한다 하지만 웹 표준에는 어긋남



## 2.3.4 글자 형태

```
b		굵은 글자 태그
i 		기울어진 글자 태그
small	작은 글자 태그
sub		아래에 달라 붙는 글자 태그
sup		위에 달라 붙는 글자 태그
ins		밑줄 글자 태그
del 	가운데 줄이 그어진 글자 태그
```

과거에는 많이 사용했으나 요즘에는 모두 스타일시트로 처리하므로 현대에는 잘 사용하지 않음



## 2.3.5 루비 문자

```html
ruby		루비 문자 선언 태그
rt			위에 위치하는 작은 문자 태그
rp			rupy 태그를 지원할 경우 출력되지 않는 태그

<body>
    <ruby>
        <span>大韓民國</span>
        <rt>대한민국</rt>
    </ruby>
</body>
```



# 2.4 목록 태그

일반적으로 페이지를 이동할 때 사용되는 메뉴를 내비게이션 메뉴라고 부른다. 이를 만들 때 사용



## 2.4.1 기본 목록

```
ul		순서가 없는 목록 태그
ol		순서가 있는 목록 태그
li		목록 요소
```

ol은 출력시 1. 2. 3. 이렇게 숫자가 붙어 나옴

ul은 그냥 점 같은 동그라미로 리스트들이 출력 됌

## 2.4.2 정의 목록

```html
dl		정의 목록 태그
dt		정의 용어 태그
dd		정의 설명 태그

code2-15

<body>
    <dl>
        <dt>HMTL</dt>
        <dd>Mult</dd>
        <dd>Conn</dd>
        <dd>Device</dd>
        
        <dt>Milk</dt>
        <dt>Animation</dt>
        <dt>3D Transform</dt>
    </dl>
</body>

```

웹 표준에 따르면 기본 목록과 정의 목록의 사용 용도가 다르지만 실제 개발할 때는 대부분 용도 구분 없이 사용함. (하지만 최대한 요오에 맞게 사용)



# 2.5 테이블 태그

테이블 태그는 HTML 페이지에서 표를 만들 때 사용하는 태그.



## 2.4.1 테이블 태그 기본

표를 만들 때는 table 태그를 사용

code 2-16 , 17 ,18



#### 테이블 요소 태그

```
tr		표 내부의 행 태그
th		행 내부의 제목 셀 태그
td		행 내부의 일반 셀 태그
```



```html
<body>
    <table>
        
    </table>
</body>

<body>
    <table border="1">
        <tr>
            <th>Header 1</th>
            <th>Header 2</th>
        </tr>
        <tr>
        	<th>Data 1</th>
            <th>Data 1</th>
        </tr>
        <tr>
        	<th>Data 2</th>
            <th>Data 2</th>
        </tr>
    </table>
</body>
```



## 2.5.2 태이블 태그의 속성



##### table 태그의 속성

```
border		표의 테두리 두께를 지정
```

##### th태그와 td 태그 속성

```
rowspan		셀의 높이를 지정
colspan		셀의 너비를 지정 
```

code2-19

```html
<body>
    <table border="1">
        <tr>
            <th colspan="3">TableData</th>
            <th rowspan="3">TableData</th>
        </tr>
        <tr>
        	<td>Table Data</td>
            <td rowsapn="2">TableData</td>
            <td>Table Data</td>
        </tr>
        <tr>
        	<td>TableData</td>
            <td>TableData</td>
        </tr>
    </table>
</body>
```



## 2.6 이미지 태그

이미지를 생성할 때 img 태그를 사용

```
src 		이미지 경로 지정
alt 		이미지가 없을 때 나오는 글자 지정
width 		이미지 너비 지정
height		이미지 높이 지정
```

src 속성에 이미지 경로를 입력하면 이미지가 ㅡㄷㅁ

`<img src="이미지 경로.jpg" alt="이미지 없을 경우" width="300"/>`

###### placehold.it 이미지가 없을시 사용하면 입력한 사이즈의 빈 이미지값을 보여줌

```html
<body>
    <img src="http://placehold.it/300x200">
    <img src="http://placehold.it/200x150">
    <img src="http://placehold.it/100x100">
</body>
```



## 2.7 오디오 태그

HTML5에 추가된 기능으로 인터넷 익스플로러 8이하에서는 사용할 수 없다.



### 2.7.1 audio 태그

audio 태그의 속성

```
src			음악 파일의 경로지정
preload		음악을 재생하기전 모두 불러올지 지정
autoplay	음악을 자동 재생할지 지정
loop		음악을 반복할지 지정
controls	음악 재생 도구를 출력할지 지정
```



code 2-24

```html
<body>
    <audio src="오디오.mp3" controls="controls"></audio>
</body>
<body>
    <audio src="오디오.mp3" controls="controls" autoplay="autoplay"></audio>
</body>
<body>
    <audio src="오디오.mp3" controls autoplay></audio>
</body> //이와같은 표기법을 HTML5 표기법이라고 한다.
```



### 2.7.2 source 태그

웹 브라우저의 버전에 따라서 코드가 실행되지 않을 수 있다. 브라우저마다 지원하는 확장자의 형식이 다르기 때문인데 이를 맞춰줄 때 사용한다. audio 또는 video 태그 안에서 사용 가능하다.

```html
<body>
    <audio controls>
    	<source scr="오디오.mp3" type="audio/mp3"/>
        <source scr="오디오.ogg" type="audio.ogg"/>
    </audio>
</body>
```



각각의 지원되는 파일을 사용되게 함으로 써 음악또는 비디오 파일을 재생시키는데 에러가 없게한다.

 





## 2.8 비디오태그

웹에서 동영상을 볼 수 있게 해주는 태그



### 2.8.1 video 태그

웹 브라우저는 mp4형식과 webM 형식을 지원함

##### viedo 태그의 속성

```
src			비디오파일의 경로
poster		비디오 준비 중일 때의 이미지 파일 경로
preload		비디오 재생전 모두 불러올지 지정
autoplay	자동재생할지 지정
loop		반복할지 지정
controls	재생도구를 출력할지 지정
width		비디오의 너비 지정
height		비디오의 높이 지정
```

video 태그도 웹 브라우저마다 지원하는 비디오 형식이 다르므로 source 태그를 사용한다

지원하는 비디오 형식은 검색해서 찾아보자.



code2-29

```html
<body>
    <video poster="http://placehold.it/640x360"
           width="640" height="360" controls>
    	<source src="동영상.mp4" type="video/mp4"/>
        <source src="동영상.webm" type="video/webm"/>
    </video>
</body>
```

![image-20210928170017637](C:\Users\MYCOM\AppData\Roaming\Typora\typora-user-images\image-20210928170017637.png)





