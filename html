# 1. HTML 기초

## HTML이란?
- HyperText Markup Language
- 웹 페이지의 **구조(뼈대)** 를 정의하는 언어 (제목, 문단, 이미지, 링크 등)

## 웹과 HTML
- 서버가 HTML 문서를 만들어 브라우저에 전달
- 브라우저는 HTML을 읽고 화면의 기본 구조를 그림
- 서버 → HTML 전달 → 브라우저 → 화면 구조 생성

## 태그(Tag)
- HTML은 태그들의 조합으로 구성
- `<태그이름>` 형태로 작성, 태그마다 의미와 역할이 있음
- 대부분 여는 태그와 닫는 태그로 이루어짐
  - `<h1>제목</h1>`
  - `<p>문단 내용</p>`
- 태그 안에 다른 태그가 들어갈 수 있음 → 중첩 구조로 문서의 계층이 만들어짐

```html
<body>
    <h1>제목</h1>
    <p>내용</p>
</body>
```

---

# 2. HTML 기본 구조

```html
<!DOCTYPE html>
<html>
    <head>
        <title>My Page</title>
    </head>
    <body>
        Hello, HTML
    </body>
</html>
```

- `<!DOCTYPE html>` : 이 문서가 HTML5 문서임을 브라우저에 알리는 선언
- `<html>` : 최상위 태그 (모든 HTML 요소는 이 안에 포함)
- `<head>` : 화면에 직접 보이지 않는 설정 영역 (제목, 문자 인코딩, CSS, 메타 정보 등)
- `<title>` : 브라우저 탭에 표시되는 제목 (검색 결과 제목으로도 사용)
- `<body>` : 브라우저 화면에 실제로 보이는 내용 영역 (텍스트, 이미지, 버튼 등)
- `</body>`, `</html>` : 각각 body, html 영역의 끝

> VS Code에서 `!` + `Enter` → 기본 구조 자동 생성

## 실습 환경
- 서버 실행 : `python3.13 -m http.server`
- VS Code **Live Preview** 익스텐션 설치
  - `Ctrl + Shift + P` → `Live Preview: Show Preview(Internal)` 선택

---

# 3. HTML이 브라우저에 표시되는 과정
1. 브라우저가 서버에 HTML 요청
2. 서버가 HTML 문서 응답
3. 브라우저가 HTML을 해석(parsing)
4. 화면 구조(DOM) 생성
5. CSS 적용 → 화면 표시

## DOM (Document Object Model)
- 브라우저가 HTML 문서를 해석해서 만든 **트리 구조**
- 각 태그와 텍스트가 노드(node)가 됨
- JavaScript가 화면을 조작할 때 사용하는 대상
- HTML = 설계도, DOM = 브라우저 안의 실제 구조

```
document
└─ html
   ├─ head
   │  └─ title
   │     └─ "My Page"
   └─ body
      └─ "Hello, HTML"
```

---

# 4. 기본 태그

| 태그 | 설명 |
|---|---|
| `<p>` | 문단 (줄바꿈 단위) |
| `<h1>` ~ `<h6>` | 제목 (숫자가 작을수록 큰 제목) |
| `<hr>` | 가로 구분선 (닫는 태그 없음) |
| `<ul>` + `<li>` | 순서 없는 목록 (점) |
| `<ol>` + `<li>` | 순서 있는 목록 (숫자) |
| `<img>` | 이미지 (닫는 태그 없음) |
| `<a>` | 링크 |
| `<div>` | 의미 없는 묶음 (영역 나누기) |

```html
<h1>One</h1>
<p>Hello, World!</p>
<hr>
<ul>
    <li>foo</li>
    <li>bar</li>
</ul>
```

## table 태그
- `<table>` : 표 전체
- `<thead>` : 머리글 영역 / `<tbody>` : 본문 영역
- `<tr>` : 행 / `<th>` : 제목 칸 / `<td>` : 데이터 칸

```html
<table border="1">
    <thead>
        <tr>
            <th>이름</th>
            <th>나이</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>alex</td>
            <td>20</td>
        </tr>
    </tbody>
</table>
```

---

# 5. HTML 속성(Attribute)
- 태그에 추가 정보나 동작을 지정
- 기본 형태 : `<태그이름 속성="값">`
- 여는 태그에만 작성 / 태그마다 쓸 수 있는 속성이 다름 / 여러 속성 같이 사용 가능

```html
<a href="https://google.com">Google</a>
<img src="pizza.jpeg" alt="pizza">
<p class="text">문단</p>
```

- `href` : 이동할 주소
- `src` : 이미지 파일 경로
- `alt` : 이미지가 안 보일 때 나오는 설명

## id 속성
- 한 페이지에서 **유일한** 식별자 (하나의 요소에만 사용)
- 특정 요소 하나를 정확히 지정해야 할 때 사용

```html
<div id="header"></div>     <!-- O -->
<p id="header"></p>         <!-- X : 같은 id 중복 사용 -->
```

## class 속성
- 공통된 특징을 가진 요소들을 묶는 속성
- 여러 요소에 같은 이름으로 **반복 사용 가능**
- class를 기준으로 CSS 스타일을 적용

```html
<p class="text">Hello</p>
<p class="text">World</p>
```

---

# 6. form 태그
- 사용자 입력을 받아 서버로 보내는 태그
- `action` : 데이터를 보낼 주소
- `method` : 보내는 방식 (`get` / `post`)

```html
<!-- GET -->
<form action="https://google.com/search" method="get">
    <input type="search" placeholder="Search..." name="q" autofocus autocomplete="off">
    <button>입력</button>
</form>

<!-- POST -->
<form action="https://httpbin.org/post" method="post">
    <input type="text" placeholder="Username" name="username">
    <button>전송</button>
</form>
```

- `name` : 서버로 보낼 때 데이터 이름
- `placeholder` : 입력칸에 미리 보이는 안내 문구
- `autofocus` : 페이지 열리면 바로 커서 위치
- `autocomplete="off"` : 자동완성 끄기

## 회원가입 화면 예시
```html
<form>
    <label for="email">Email</label>
    <input id="email" type="email" required placeholder="example@email.com">
    <br>
    <label for="phone">Phone</label>
    <input id="phone" type="text" required placeholder="010-1234-5678"
           pattern="010-[0-9]{4}-[0-9]{4}"
           title="010-1234-5678 형식으로 입력하세요">
    <br>
    <button type="submit">Submit</button>
</form>
```

- `<label for="id">` : input의 id와 연결 (label 클릭 시 해당 입력칸 선택)
- `required` : 필수 입력
- `pattern` : 정규식으로 입력 형식 검사
- `title` : 형식이 틀렸을 때 보여줄 안내

## regex (정규식)
- 문자열의 형식을 검사·검색·치환하기 위한 규칙

| 기호 | 의미 | 기호 | 의미 |
|---|---|---|---|
| `.` | 아무 문자 1개 | `[]` | 문자 집합 |
| `*` | 0번 이상 | `0-9` | 0부터 9까지 |
| `+` | 1번 이상 | `\d` | 숫자 |
| `?` | 0 또는 1 | `^` | 시작 |
| `{n}` | n번 반복 | `$` | 끝 |

> `010-[0-9]{4}-[0-9]{4}` → 010- 뒤에 숫자 4개, - 뒤에 숫자 4개

---

# 7. Semantic HTML
- 태그 자체에 **의미**를 담아, 코드가 무엇을 뜻하는지 드러내는 작성 방식
- `div` : 의미 없음, 단순한 묶음
- `p` : 문단
- `header` : 상단 영역 / `main` : 핵심 콘텐츠 / `footer` : 하단 정보

```html
<header>Dong-hyeon Shin</header>
<main>Backend Engineer in Seoul</main>
<footer>Copyright &#169; Dong-hyeon Shin</footer>
```
