# 페이지 만들때
1. HTML 뼈대부터 만들어라
2. 요소 하나하나에 CSS적용하기

# CSS파일을 분리하는 이유
1. HTML 코드 내부에서 디자인과 관련된 요소를 제거할 수 있기 때문<br>
-> HTML코드가 정보의 전달과 웹 페이지의 구조 설계라는 본연의 기능에 집중할 수 있게 되었다.

2. 협업의 편의성
-> 웹 페이지의 기능적 측면에만 집중할 수 있다는 장점이 있다.

# css 기본 문법
셀렉터=선택자 (selector) : 태그, 클래스명, id

<img width="670" alt="Image" src="https://github.com/user-attachments/assets/fab07437-f8c7-4e2b-94da-dd66d69abc90" />

# CSS 적용방식
CSS를 HTML파일에 어떻게 적용시키냐
> 띄어쓰기는 자식루트라는 뜻

1. 인라인방식(태그에 직접 적용)
   >인라인으로 쓰는것이 우선순위가 가장 높음
예시) h2 style="color:red">인라인적용/h2>

2. style태그를통해 적용(내장(embedded) 방식<br>
예시)<p>&nbsp;head><br>
&nbsp;&nbsp;&nbsp;style>
          
&nbsp;&nbsp;&nbsp;/style><br>
&nbsp;&nbsp;/head>></p><br>
      
3. 링크 방식 - 외부의 CSS파일을 불러와서 적용<br>
 head><br>
    link rel=”stylesheet” type=”text/css” href='css 외부 파일 경로'><br>
 /head><br>

4. import 방식<br>
 @import url(css/style.css);

# 스타일 적용 우선순위
1. 인라인 선언 방식(태그안에 style)
2. 아이디 선택자(#)
3. 클래스 선택자(.)
4. 태그 선택자(p, div, a...)
5. 전체 선택자(*)

# 태그를 직접 선택
## 문서에 해당 태그의 디자인이 전부다 바뀜
1. 태그를 직접 선택
- 장점: 내가 선택한 부분 전부를 바꿀 수 있음
- 단점: 내가 원하는것만 바꿀수가 없음

2. 클래스(class)선택자 > .+클래스 명<br>
2-1. 태그에 클래스명을 붙인다<br>
   태그명 class="클래스명">content/태그명>

2-2. 클래스를 붙인 태그를 선택한다<br>
   .+클래스명{선언:선언;}

3. id선택자<br>(같은 문서안에서 겹치면 안된다.)
- css요소를 선택할때 사용
- #을써서 구분한다
> 클래스의 경우 겹쳐도 상관없지만 id의 경우 JS로 넘겨야 하기때문에 혼란을 야기할 수 있다.

4. 그룹(group)선택자
- 여러 선택자를 같이 사용할때 사용
- 쉼표(,)를 사용하여 연결하고 코드를 중복해서 작성하지 않도록 하여 코드를 간결하게 만들어준다.

5. 전체 선택자
- 별표(*)를 사용하여 모든요소를 선택한다(body)

# 스타일 적용시키기
1.스타일을 적용시킬 태그를 선택한다(선택자)
> 태그(p,h1,div,span), 클래스(.클래스), 아이디(#아이디명) <br>
2.스타일을 적용한다.(프로퍼티(property)를 잘알아야함)(뭘쓰든 결과는 같다)
> 인라인방식(태그에 직접 적용),style태그에 선언(적용하고자 하는 태그 선택해도 된다.),
> 외부스타일시트를 현재 문서에 적용(link rel="stylesheet" href="경로")<br>
> (@import url("경로"))


# CSS 속성(css 스타일은 다 속성으로 이루어져 있다.)
- 선택자{속성명 : 값; 속성명 : 값;}

> 인라인 형태 스타일 적용
> p style="속성명 : 값; 속성명 : 값;></p 
## 테두리
- border : 두께, 스타일, 색깔<br>
  1.border-width : 두께<br>
  2.border-style : 스타일<br>
  3.border-color : 색깔<br>

## 여백
- padding : 내용과 테두리 사이의 여백
- margin : 요소와 외부사이의 여백

## 폰트 : weight, style, size family 순으로 적용 해야 한다.
- font-size : 폰트 크기
- font-weight : 폰트 두께
- font-style : 기울기
- font-family : 폰트 선택

## 이미지 배경넣기
- background : url(경로)
  1. no-repeat 
  2. repeat
  3. repeat-x
  4. repeat-y

> img src="경로">(html이기때문에 레이아웃에 영향을 줄 수 밖에 없다)<br>
> css로 background url(경로)(html이아닌 요소의 배경으로 처리되서 레이아웃에 직접적인 영향을 주지 않는다)

## display : html요소가 어떻게 배치되는지 결정하는 속성
> 강제로 인라인이나 블록속성으로 바꿀 수 있다.
1. block : 한 영역을 차지하는 박스형태를 가지는 성질 (기본적으로 width값이 100%)
 - 공간을 차지하고 있기 때문에 옆에 다른 요소가 올 수 없다.
 - height, weight를 지정할 수 있다.
 - margin과 padding을 지정할 수 있다.
2. inline : width를 콘텐츠만큼 차지한다. 높이또한 콘텐츠의 크기만큼 잡힌다.

## overflow : 요소의 내용이 요소의 크기를 초과할 때, 초과된 부분을 어떻게 처리할 것인지 결정하는 속성
- visible(기본값) : 경계를 벗어나도 내용이 그대로 보임
- hidden : 넘치는 콘텐츠를 잘라내고 보이지 않게한다.
- scroll : 요소의 내용이 넘치더라도 스크롤바를 항상 표시한다.
- auto : 콘텐츠가 요소의 크기를 초과할 때만 표시한다.

# flex의 container 속성
 - justify-content : 메인 축을 기준으로 수평에서의 정렬
 - align-content : 메인 축을 기준으로 수직에서의 정렬

## 화면 정중앙 세팅
- justify-content : center;
- align-items : center;

# 미디어 쿼리
- @media(조건){조건이 맞을 때 보여줄 스타일}
>경우에 따라 모바일과 데스크탑용 디자인을 완전히 별개의 CSS파일로 관리하려고 할 때 미디어 쿼리를 적용할 수 있다
