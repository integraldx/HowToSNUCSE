# HTML
HTML은 웹 브라우저에서 웹 페이지를 어떻게 표시할지를 규정하는 마크업 언어로, HyperText Markup Language의 줄임말입니다.

## 간단한 튜토리얼
HTML을 이해하기 전에 아래 활동을 해 봅시다.

새로운 파일을 만들고 그 파일의 이름과 확장자를 index.html이라고 이름을 붙입시다. 그러면 이 파일의 아이콘이 자신이 기본적으로 사용하는 브라우저의 아이콘으로 바뀔 것입니다.  
이제 index.html을 편집할 건데, 더블클릭 하는 대신 [텍스트 에디터](/개발_환경/index.md)로 열어 봅시다. 우클릭 한 다음 적당한 연결 프로그램을 선택하면 됩니다.  
텍스트 에디터로 파일을 열었다면 아래 내용을 그대로 적습니다.  

```
<!DOCTYPE html>
<html>
    <head>
        <title>title example</title>
    </head>
    <body>
        <h1>h1 example</h1>
        <h3>h3 example</h3>
    </body>
</html>
```
다 적었다면 파일을 저장한 다음 닫고, index.html을 더블클릭으로 열어 봅시다. 그러면 웹 브라우저가 열리면서 아래와 같은 페이지가 나타날 것입니다.  

![image](https://user-images.githubusercontent.com/42795430/72005264-8b2ec900-3290-11ea-96db-11c0b16fd101.png)

h1 example/h3 example 대신에 다른 문자를 적고 페이지를 새로고침하면 그 문자가 그대로 표시됩니다. 이를 통해 브라우저는 **HTML 코드를 해석해서 시각적으로 표시**한다는 것을 알 수 있습니다.

## HTML과 웹 브라우저와의 관계

HTML은 웹 브라우저가 작동하는 방식과 밀접한 관련이 있습니다. 컴퓨터 간에 통신을 할 때 모든 정보는 0과 1을 기반으로 하는 문자열로 전송됩니다. 그렇다면 문자열이 어떤 과정을 거쳐 시각적인 웹 페이지로 표시되는 걸까요? 예를 들어 [www.google.com](www.google.com)에 들어가면 로고와 검색창, 로그인 버튼은 어떻게 표시되는 걸까요?  
그 해답이 바로 HTML입니다. 브라우저의 주소창에 www.google.com이라고 적어 넣으면, 브라우저는 www.google.com에 해당하는 주소에 연락을 보내 HTML 코드를 받아 옵니다. 이 HTML 코드를 해석하고 시각적으로 표시하는데, 이것이 바로 우리가 보는 웹 페이지입니다. 웹 브라우저에서 f12 버튼을 누르면 개발자 도구 창이 뜨는데, 여기서 Elements(요소) 탭을 클릭하면 볼 수 있는 HTML 코드가 바로 그러한 과정으로 받아 온 코드입니다.

## 간단한 문법

*참고: 이해를 위해 일부 단어가 부정확하게 사용되었을 수 있습니다.

HTML 문서는 element들로 이루어져 있으며, 하나의 element는 start tag에서 시작해 end tag로 종료합니다.
```
<div id='example'>content1</div>
```
위 예시의 경우, 이 전체가 하나의 HTML element이며, `<div id='example'>`은 start tag, `</div>`은 end tag, `content1`은 content라고 합니다. 
이 element는 `id`라는 attribute를 갖고, 그 attribute의 값은 `'example'`입니다.
프로그래밍 언어로 비유하자면, 위의 element는 div라는 타입의 한 객체이며 id라는 필드의 값으로 'example'을 갖는 것과 같습니다.  
하나의 element는 content로 다른 element들을 가질 수 있습니다. 예를 들어 다음과 같은 HTML 코드를 작성할 수 있습니다.
```
<div id='first>
    <div id='second'>
        Hello
    </div>
    <button id='button'>
        Click
    </button>
</div>
```
이처럼 HTML 코드는 마치 tree와 같은 구조를 가지게 됩니다. 이에 관해선 [DOM](https://en.wikipedia.org/wiki/Document_Object_Model)이라는 용어도 있지만, 여기서는 깊게 살펴보지 않겠습니다.  
웹 브라우저마다 지원하는 태그에 약간씩 차이가 있을 수 있지만 대체로 비슷한 태그를 지원하며 이들만 가지고도 웹 페이지를 만들 수 있습니다. 때문에 생소한 HTML 태그가 웹 브라우저에서 작동하지 않는다면 브라우저 호환성을 의심해 볼 수 있습니다.

## HTML과 Javascript와의 관계

HTML은 무엇을 보여 줄 지를 정의할 뿐 프로그래밍 언어가 아니기 때문에, HTML만 가지고 할 수 있는 작업은 극히 적습니다. 예를 들어, 어떤 `<button>` element를 클릭했을 때마다 `<h1>` element가 하나씩 생성되게 하는 것조차 HTML만 가지고는 할 수 없습니다. 다른 언어와 연동시켜 element를 생성해야 합니다.  
이때 주로 사용되는 언어가 JavaScript입니다. 그래서 웹 개발자들이 Javascript와 HTML을 배우는 것입니다. 이 둘을 어떻게 연동하는지는 웹 개발의 영역이므로 여기서는 설명하지 않겠습니다.

## HTML과 CSS와의 관계

HTML 파일과 함께 자주 등장하는 것이 CSS 파일입니다. 
CSS는 Cascading Style Sheet의 줄임말로, HTML 등의 마크업 언어로 작성된 문서가 실제 웹 브라우저에 표시되는 방식을 설정할 수 있습니다.  
HTML이 '어떤' element들을 보여 줄 지, 그리고 그 element들의 관계가 어떠한지를 정의한다면, css는 element들을 '어떻게' 보여 줄 지를 정합니다. 예를 들어, 위의 HTML 튜토리얼에서 `<h1>` 컴포넌트는 브라우저에서 왼쪽에 붙어 있는 것이 default입니다. CSS 파일을 사용하면 이를 중앙, 오른쪽, 혹은 특정한 자리로 옮일 수 있습니다.  
브라우저는 HTML과 CSS를 함께 해석하여 표시합니다. CSS와 HTML을 어떻게 연동시키는지, CSS의 문법은 어떠한지 또한 웹 개발의 영역이므로 여기서는 설명하지 않겠습니다.