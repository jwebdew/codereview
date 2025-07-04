# codereview
셀프 리뷰&피드백

#### 코드리뷰란
하나의 코드를 가지고 나 이외의 사람들과 함께 의견을 나누는 것.

#### 그렇다면 왜 코드리뷰는 왜 하는가?
1. 남들에게 코드를 보여주면서 좀 더 퀄리티 높은 코드를 작성한다.
2. 코드에 대한 책임이 코드를 짠 혼자가 아니라 우리 모두에게 있다는 문화를 만들기 위해 한다.
3. 다른 사람의 잘 만들어진 코드를 보면서 배울 기회를 얻어 주니어, 시니어 개발자의 성장
4. 이해 수준을 상향 평준화 하는 것.
5. 조기 버그 발견 가능성 상승.

# ✨ Portfolio Website

    반응형 웹사이트 제작
    기술 : HTML, CSS, JAVASCRIPT, JQUERY, swiper slide, gsap
    프로그램 : 피그마, 비주얼스튜디오코드
    링크 : 


---

## 🔍 Self Review

### 📁 1. 파일 구조 및 구성
- [x] 역할별로 디렉토리 분리 (`/css`, `/js`, `/images`)
- [x] 인라인 스타일, 스크립트 제거 → 외부 파일로 분리 완료
- [x] 파일/폴더 네이밍 일관성 유지

---

### 🧱 2. HTML 리뷰
```html
<div id="header"></div>
    
     <div id="main">
            <div id="smoother-wrapper">
               <div id="smoother-content">
```
- [ ]  의미론적 태그를 적절히 사용이 부족함 (`<article>`, `<section>`, `<header>`, `<main>`, `<nav>` 등)
- `div id="main"` 의 `div`대신 `main`태그 사용이 필요함
- [ ]  heading 태그는 순차적으로 구조화 진행 (`<h1>` `<h2>` `<h3>` ..)
- [x] 모든 이미지에 `alt` 속성 적용
- [x] 폼 요소에 `label` 연결 완료
- [ ] `<h1>`이 여러 번 사용됨 → 하나만 사용하도록 구조 변경 예정
- [ ] 링크(<a>)안에 버튼(<button>) 태그 사용  a태그만 사용 예정

---

### 🎨 3. CSS 리뷰
- [x] 중복 스타일 최소화 및 공통 클래스 추출
- [x] 반응형 웹 완성 (미디어 쿼리 사용)
- [ ] 초기값, 공통된 요소 하나의 페이지에서 모두 작성 → reset.css, common.css분리하여 정리 예정

---

### ⚙️ 4. JavaScript 리뷰
```javascript
var $main_visual = $(".main_visual .main_slider");
  var $visualList = $(".main_visual .main_slider .slide_box > div");
  var $visual_length = $visualList.length;
  var _visualNum = 0;
  var _visualIn = 0;
  var setT = 0;
  var bool = true;
  // var paging=$visualList.eq(targets);
  var idx = $(this).index();
```
- 자바스크립트와 제이쿼리 구분을 위해 변수명 앞에 $ 추가함

- [x] 메뉴 토글, 스크롤 애니메이션 등 기능 구현 완료
- [ ] 함수 네이밍 일부 추상적 (예: `handle1()`) → 의미 있는 이름으로 리팩토링 예정
- [x] 코드 모듈화 완료 (기능별 함수 분리)
```javascript
  $(".use-checkbox-top").change(function () {
    if (
      $(".use-checkbox-top:checked").length === $(".use-checkbox-top").length
    ) {
      btnSubmitTop.addClass("active");
    } else {
      btnSubmitTop.removeClass("active");
    }
  });
  $(".use-checkbox-bottom").change(function () {
    if (
      $(".use-checkbox-bottom:checked").length ===
      $(".use-checkbox-bottom").length
    ) {
      btnSubmitBottom.addClass("active");
    } else {
      btnSubmitBottom.removeClass("active");
    }
  });
```
- $(".use-checkbox-bottom").change(function ()... on('change', function(){ 을 이용하여 동적으로 처리되도록 변경
- 반복되는 선택자를 변수로 지정하여 요소의 효율을 높여주는게 좋음.  $(".use-checkbox-bottom")

---

### 🎯 5. UX/UI 측면
- [x] 인터랙션 요소에 호버 및 포커스 스타일 제공
- [x] 모바일 환경에서 메뉴가 터치로 작동함
- [ ] 디자인 시각적 계층 구조 명확함

<img src="https://github.com/user-attachments/assets/3934e497-461f-4bd4-9e6b-bc286d2ebf24" style="width: 500px;"/>

- [ ] PPL과 영상 보러갈 수 있도록 링크 추가

---

## 🛠️ 개선 계획 (To-Do)
- [ ] `<h1>` 태그 구조 개선
- [ ] JavaScript 함수명 정비
- [ ] 로딩 애니메이션 추가
- [ ] 불필요한 font파일 제거

---

## ✅ 참고 도구
- [W3C HTML Validator](https://validator.w3.org/)
- [Lighthouse Performance Check (Chrome DevTools)](https://developer.chrome.com/docs/lighthouse/overview/)
- [Wave Accessibility Checker](https://wave.webaim.org/)



 

