"<tr>"
row는 가로를 의미하지만 
 " <td>내용</td>"
 "<td>번호</td>"
  이게 가로로 써짐
  한줄구성
"</tr>"

rowspan : row span이란 뜻으로 셀(세로줄)을 합치는 개수를 지정
출처: https://aboooks.tistory.com/59 [지구별 안내서:티스토리]
col은 반대겟지?




인풋태그
< input type="text" id="title" name="title">
1. id 속성 (id="title")
document.all.id.value
id.value
document.getElementById("폼 id").value
id 속성은 page 안에서 중복으로 사용할 수 없으며, 주로 JavaScript에서 다루기 위해 지정한다.

name 속성으로도 JavaScript를 통해 속성이나 값을 변경할 수 있는데, 중복 값을 가질 수 있어 id 속성의 값으로 주로 접근한다.

document.getElementById(id)를 통해서 해당 엘리먼트 Object를 가져올 수 있다.

id 속성으로 설정된 값은 @RequestMapping에 지정한 Server단 (클래스 or 메소드)의 파라미터로 넘어가지 않기 때문에, Server단에서 접근이 불가능하다.

2. name 속성 (name="title")
document.폼 객체명.폼 원소명.value
document.getElementsByName("name")
name 속성은 page 영역에서 중복되어 사용이 가능하며, action에 해당하는 페이지에 전달할 수 있는 파라미터로 사용한다.

GET/POST 방식으로 값을 전달하고 싶은 tag에 사용한다. 예를 들어 Form 객체(input, radio, checkbox, ...)에서 전송되는 파라미터의 Key 값으로 사용한다.

태그의 name 값이 키(Key)로 해서 값(Value)가 전송된다.
즉, request에 값이 전달될 때 Map과 마찬가지로 Key와 Value 쌍의 형식으로 데이터가 저장된다.

Server단에서 request.getParameter(parameterName) 으로 값을 가져온다.

정리하자면,

name 속성은 스크립트단에서 id 속성은 Server단에서 주로 사용된다.
id 속성으로 지정된 값은 server단에서 HttpServletRequest 파라미터로 전달받을 수 있다.
전달받은 파라미터는 Map과 마찬가지로 Key-Value 형식으로 이루어져 있다.
