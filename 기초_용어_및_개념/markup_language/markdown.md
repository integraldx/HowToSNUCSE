# 마크다운(markdown)

마크다운은 간단한 형태의 마크업 언어입니다. 다른 마크업 언어에 비해 읽고 쓰기 쉬워 다양한 웹 사이트에서 지원합니다. 마크다운 파일은 확장자로 .md를 사용합니다.

## 사용

마크다운 형식으로 문서를 작성한 다음 마크다운 변환기를 통해 PDF나 HTML 등으로 변환시킬 수 있습니다. vscode로 `.md` 확장자를 갖는 마크다운 파일을 편집하고 있을 땐 우측 상단에 `측면에서 미리 보기 열기` 버튼을 눌러 현재 마크다운 파일이 어떻게 변환될 지 미리 볼 수 있습니다. 또는 [온라인 프로그램](https://dillinger.io/)을 사용하여 작성, 미리보기, 변환까지 한 번에 할 수 있습니다. github에서는 마크다운 형식으로 문서를 작성하면 자동으로 변환시켜 줍니다. 마크다운의 변환에는 정해진 표준이 없으므로 어떤 변환기를 사용하느냐에 따라 스타일에 차이가 있을 수 있습니다. 다만 최근에는 [표준 비슷한 것](https://commonmark.org/)이 개발되고 있습니다.

## github과 마크다운

github에서는 마크다운을 자주 사용합니다. 지금 보고 있는 페이지도 마크다운으로 작성한 것입니다. issue나 comment 등을 마크다운 형식으로 작성할 수 있습니다. 또한 어떤 폴더에 들어갔을 때 README.md라고 이름을 붙인 마크다운 파일이 있으면 자동으로 열어서 보여 줍니다.

## 문법
마크다운은 간단한 문법만 알아도 문서를 상당히 깔끔하게 작성할 수 있습니다. 때문에 기본적인 문법은 숙지해 두는 것을 추천합니다.  
마크다운 문법을 정리한 페이지는 많이 있기 때문에, 이곳에는 전부 설명하지 않고 기본이 되는 문법만 일부 설명하겠습니다. 다른 문법도 알아보고 싶다면 `마크다운 사용법` 같은 키워드를 구글에 검색해 보세요.

### ○ 제목
줄 앞에 #을 하나 이상 이어 붙이면 제목처럼 변환됩니다. #의 개수가 많아질수록 하위 항목의 제목이 됩니다.

#### 마크다운
```
# 서울특별시
## 관악구
### 관악로 1
#### 301동
##### 314호
###### 컴퓨터공학부 학생과방
```

#### 변환 결과
# 서울특별시
## 관악구
### 관악로 1
#### 301동
##### 314호
###### 컴퓨터공학부 학생과방

### ○ 개행
마크다운에서 개행문자(enter) 하나만으로는 개행이 되지 않습니다. 개행 문자 뒤에 스페이스바 두 개를 입력하거나 중간에 빈 줄을 입력해야 합니다.

#### 마크다운
```
줄1(<- 공백 없음)
줄2  (<- 공백 2개)
줄3

줄4
```

#### 변환 결과
줄1
줄2  
줄3

줄4

### ○ 항목
`*` 또는 `+` 또는 `-`를 사용하여 항목의 리스트를 작성할 수 있습니다. 하위 항목은 `SPACE`나 `TAB`을 입력해 들여쓰기하면 작성할 수 있습니다.

#### 마크다운
```
* 항목 1
* 항목 2
  + 항목 2-1
    - 항목 2-1-1
    - 항목 2-1-2
  + 항목 2-2
* 항목 3
  - 항목 3-1
```

#### 변환 결과
* 항목 1
* 항목 2
  + 항목 2-1
    - 항목 2-1-1
    - 항목 2-1-2
  + 항목 2-2
* 항목 3
  - 항목 3-1

### ○ 수평선
`-` 또는 `*` 또는 `_`을 3개 이상 작성할 경우 수평선이 그려집니다. 단, `-`을 사용할 경우 바로 윗 줄을 2단계 제목으로 만드는 것과 같은 문법이기 때문에 이전 줄은 비워 두어야 합니다.

#### 마크다운
```
위쪽 내용
(빈 줄)
---
아래쪽 내용
```

#### 변환 결과
위쪽 내용

---
아래쪽 내용

### ○ 문자 효과
기울임, 볼드, 취소선을 지원합니다. 밑줄은 지원되지 않습니다.

#### 마크다운

```
_기울임1_ , *기울임2*  
__볼드1__ **볼드2**  
~~취소선~~  
___기울임+볼드1___  
***기울임+볼드2***  
**_복합적_ ~~사용~~**  
```

#### 변환 결과

_기울임1_ , *기울임2*  
__볼드1__ **볼드2**  
~~취소선~~  
___기울임+볼드1___  
***기울임+볼드2***  
**_복합적_ ~~사용~~**  
