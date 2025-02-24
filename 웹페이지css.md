# css 기본 문법
셀렉터=선택자 (selector) : 태그, 클래스명, id

<img width="670" alt="Image" src="https://github.com/user-attachments/assets/fab07437-f8c7-4e2b-94da-dd66d69abc90" />

# CSS 적용방식
CSS를 HTML파일에 어떻게 적용시키냐

1. 인라인방식(태그에 직접 적용)
 <h2 style="color:red">인라인적용</h2> 

2. 내장(embedded) 방식

3. 링크 방식 - 외부의 CSS파일을 불러와서 적용
 <link rel=”stylesheet” type=”text/css” href='css 외부 파일 경로'>

4. import 방식
 @import url(css/style.css);

# 태그를 직접 선택
## 문서에 해당 태그의 디자인이 전부다 바뀜
1. 태그를 직접 선택
- 장점: 내가 선택한 부분 전부를 바꿀 수 있음
- 단점: 내가 원하는것만 바꿀수가 없음

2. 클래스(class)선택자 > .+클래스 명
2-1.태그에 클래스명을 붙인다
   <태그명 class="클래스명">content</태그명>
