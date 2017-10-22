# Week 1
## 기본 예제
```javascript
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Welcome to Vue</title>
  <script src="https://unpkg.com/vue"></script>
</head>
<body>
  <div id="simple">
    <h2>{{ message }}</h2>
  </div>

  <script>
    var model = {
      message: "첫번째 Vue.js 앱입니다."
    }

    var simple = new Vue({
      el: "#simple",
      data: model
    })
  </script>
</body>
</html>
```
- model: 모델(Model) 객체
	- 데이터를 담고있음.
- simple: Vue객체/뷰모델(ViewModel) 객체
	- el: HTML element
	- data: 모델 객체 참조.

*데이터(모델)이 변경되면 뷰모델 객체는 즉시 이를 HTML요소(뷰)에 반영시킴.*

## 기본 디렉티브
- v-text, {{ }}: innerText속성에 연결됨. 태그 문자열이 그대로 나타남.
- v-html: innerHTML속성에 연결됨. 태그 문자열을 파싱하여 화면에 나타냄.
	- &lt;script&gt;태그를 그대로 바인딩하기 때문에, script공격에 취약. 꼭 필요한 경우를 제외하고, v-text 권장
- v-bind: 요소 객체의 속성들을 바인딩(ex. v-bind:value, v-bind:src).
- v-model: 양방향 데이터 바인딩.
- v-if: 조건문의 결과가 false면 렌더링 자체를 하지 않음.
- v-show: 렌더링은 하되, 조건문의 결과에 따라 display 스타일 속성으로 화면표시여부 결정.
- v-for: 반복 렌더링.

*&lt;template&gt;태그는 렌더링 내용에는 포함되지 않고, 요소들을 그룹화 하는 용도로 사용될 수 있음.*