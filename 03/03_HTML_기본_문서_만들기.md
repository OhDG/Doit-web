# 03-1_HTML과 첫 만남

html : HyperText Markup Language : 웹 문서를 만드는 언어 : 웹 브라우저에 내용을 보여 주는 텍스트, 이미지, 영상 등의 위치를 표시하는 것

하이퍼텍스트 : 문서를 서로 연결해 주는 링크

태그 : 웹 브라우저가 어느 부분이 제목, 텍스트 또는 표인지 구별할 수 있도록 꼬리표(태그)를 붙임

# 03-2_HTML 구조 파악하기

```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8"> // 한글 인코딩
  <title>HTML 기본 문서</title>
</head>
<body>
  <h1>프런트엔드 웹 개발</h1>
  <hr>
  <p>HTML</p>
  <p>CSS</p>
  <p>자바스크립트</p>
</body>
</html>
```

<head> 태그 : 웹 문서의 정보

<meta> 태그 : 화면에 글자를 표시할 때 어떤 인코딩을 사용할지 지정하는 것. 그 외에도 웹 사이트의 키워드나 간단한 설명, 제작자 등의 정보를 지정

```html
<meta name="keywords" content="html의 구조"> // 웹 문서의 키워드
<meta name="description" content="html의 구조를 알아봅시다"> // 웹 문서의 설명
<meta name="author" content="Obi"> // 웹 문서의 소유자나 제작자
```

<title> 태그 : 제목 표시줄

---

<body> 태그 : 웹 브라우저에 보여 줄 내용

1. 인터넷이나 웹 사이트를 검색할 때 필요한 내용을 정확히 찾을 수 있다.

### 주요 시맨틱 태그

<header> : 헤더 영역

<nav> : 같은 웹 문서 안에서 다른 위치로 연결하거나 다른 웹 문서로 연결하는 링크를 만든다.

```html
<header>
      <div id="logo">
        <a href="index-footer.html">
          <h1>Dream Jeju</h1>
        </a>
      </div>
      <nav>
        <ul id="topMenu">
          <li><a href="#">단체 여행</a></li>
          <li><a href="#">맞춤 여행</a></li>
          <li><a href="#">갤러리</a></li>
          <li><a href="#">문의하기</a></li>
        </ul>
      </nav>
    </header>
```

<main> : 웹 문서마다 다르게 보여주는 내용으로 구성. 한 번만 사용할 수 있다.

<article> : 웹에서 실제로 보여 주고 싶은 내용을 넣는다. 여러 개 사용가능, 안에 <section> 태그 넣을 수도 있다.

<section> : 콘텐츠 영역을 나타냄. 몇 개의 콘텐츠를 묶는 용도로, <article> 태그는 블로그의 포스트처럼 독립된 콘텐츠로 쓴다.

단순히 스타일을 적용하려고 콘텐츠를 묶으려면 <div> 태그를 사용함.

```html
<main class="contents">
      <section id="headling">
        <h2>몸과 마음이 치유되는 섬</h2>                  
        <div class="detail"> 
          <img src="images/healing.jpg">                            
          <b><p>쉼(Healing)의 공간으로 안내합니다</p></b>          
          <p>탁 트인 바다, 시원한 바람에 몸을 맡기고 뚜벅뚜벅 오름을 오르고 올렛길을 걷다보면 온전히 나에게 집중할 수 있습니다. </p>        
        </div>        
        <div class="schedule">
          <h3>상세 일정</h3>
          <ul>
            <li>여행 기간 : 2박 3일</li>
            <li>여행 일정 : (여행 일정은 상담을 통해 결정 및 조정 가능합니다)</li>
          </ul> 
        </div>
      </section>
      <section id="activity">
        <h2>다양한 액티비티가 기다리는 섬</h2>
        <div class="detail">          
          <img src="images/activity.jpg">
          <b><p>모험과 스릴이 넘치는 레저의 천국으로 안내합니다.</p></b>          
          <p>둘러보기만 하는 여행을 하셨나요? </p>
          <p>하늘을 날며 시원한 바다를 내려다보는 패러글라이등과 투명한 물빛 속을 여행하는 스킨스쿠버... 아름다운 제주 해안도로를 씽씽 전동바이크나 전동킥보드로 달려보세요. 시원한 바다를 가까이에서 느낄 수 있는 요트 체험과 배낚시도 빼놓을 수 없겠죠?</p>
        </div>
      </section>
    </main>
```

<aside> : 사이드 바 영역

<footer> : 맨 아래쪽에 있는 푸터 영역. 사이트 제작 정보나 저작권 정보, 연락처 등을 넣음. 푸터 영역에서 다른 시맨틱 태그를 사용 가능. 

```html
<footer>    
      <section id="bottomMenu">
        <ul>
          <li><a href="#">회사 소개</a></li>
          <li><a href="#">개인정보처리방침</a></li>
          <li><a href="#">여행약관</a></li>
          <li><a href="#">사이트맵</a></li>
        </ul>
      </section>   
    </footer>  
  </div> 
</body>
</html>
```

<div> : 문서 구조를 만들 때 사용. id나 class 속성을 사용해서 문서 구조를 만들거나 스타일을 적용할 때 사용함.

```html
<header>
      <div id="logo">
        <a href="index-footer.html">
          <h1>Dream Jeju</h1>
        </a>
      </div>
      <nav>
        <ul id="topMenu">
          <li><a href="#">단체 여행</a></li>
          <li><a href="#">맞춤 여행</a></li>
          <li><a href="#">갤러리</a></li>
          <li><a href="#">문의하기</a></li>
        </ul>
      </nav>
    </header>
```
