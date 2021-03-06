# HTML 태그

- 개요

    HTML 버전이 업그레이드 되면서 태그가 새로 추가되기도 하고 삭제되기도 합니다.
    현재 태그의 개수는 대략 130여 개 정도입니다.

    관련 통계 사이트를 보면 실제로 대다수의 웹 페이지는 대략 25개 정도의 서로 다른 태그가 사용된다고 합니다.
    ([https://www.advancedwebranking.com/html/#overview](https://www.advancedwebranking.com/html/#overview))

    ---

    ### 참고자료

    [HTML elements reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

    [HTML Reference](https://www.w3schools.com/tags/default.asp)

    [HTML5 Element Index](http://html5doctor.com/element-index/)

- 제목과 단락 요소

    ### 제목 태그

    제목(heading) 태그는 문서 내의 제목을 표현할 때 사용하는 태그입니다.
    태그 이름은 heading을 줄여서 h로 쓰며, 제목의 레벨에 따라서 `<h1>` ~ `<h6>`까지 있습니다.
    보통 `<h1>`은 해당 페이지를 대표하는 큰 제목으로 주로 사용되며, 숫자가 올라갈수록 조금 더 낮은 수준의 소제목을 나타내게 됩니다.
    하지만 현재 웹 페이지의 내용은 제목과 본문 식의 문서 형태보다는 주로 이미지나 그림처럼 시각적인 형태로 표현되고 있어서 제목 태그를 `<h6>`까지 쓰는 경우는 거의 없습니다.

    ```html
    <h1>역사</h1>
    <h2>개발</h2>
    1980년, 유럽 입자 물리 연구소(CERN)의 계약자였었던 물리학자 팀 버너스리가 HTML의 원형인 인콰이어를 제안하였다.
    ... 이하 생략
    <h2>최초 규격</h2>
    HTML 최초의 일반 공개 설명은 1991년 말에 버너스리가 처음으로 인터넷에서 문서를 "HTML 태그"(HTML tag)로 부르면서 시작되었다.
    ... 이하 생략
    ```

    예시 글에서는 역사가 가장 큰 제목이기 때문에 `<h1>`를 사용했고, 개발과 최초 규격에는 그보다 아래 단계인 `<h2>`를 사용했습니다.

    제목 태그를 사용하면, 일반 텍스트보다 더 강조되는 스타일이 적용되는데 이는 브라우저가 기본적으로 제목 태그에 제공하는 스타일입니다.
    제목이라는 의미에 맞게 기본적으로 좀 더 굵고 크게 표현이 됩니다.

    ### 단락 태그

    단락(paragraph) 태그는 paragraph를 줄여서 p로 씁니다.
    제목 태그에 이어 본문에 해당하는 내용을 단락 태그를 이용해 작성해보겠습니다.

    ```html
    <h1>역사</h1>
    <h2>개발</h2>
    <p>
    	1980년, 유럽 입자 물리 연구소(CERN)의 계약자였었던 물리학자 팀 버너스리가 HTML의 원형인 인콰이어를 제안하였다.
    	... 이하 생략
    </p>
    <h2>최초 규격</h2>
    <p>
    	HTML 최초의 일반 공개 설명은 1991년 말에 버너스리가 처음으로 인터넷에서 문서를 "HTML 태그"(HTML tag)로 부르면서 시작되었다.
    	... 이하 생략
    </p>
    ```

    화면에는 별다른 변화는 없지만, 이전보다 훨씬 의미에 맞게 잘 짜진 마크업 구조라고 볼 수 있습니다.

    ### 개행

    단락 태그 `<p>`를 사용해서 단락으로 구분하면 자연스럽게 개행이 됩니다.
    그럼 `<p>` 태그 내부에서 임의로 개행을 하려면 어떻게 해야 할까요?
    HTML 문법 중 공백 시간에 배운 대로, html은 두 칸 이상의 공백 및 개행을 무시하기 때문에 실제 코드창에서 개행을 하더라도 화면에 나타나지는 않습니다.
    따라서 개행을 위해 쓰이는 태그가 바로 `<br>` 태그입니다. (linebreak를 줄여서 br이라고 합니다.)
    `<br>` 태그는 닫기 태그와 내용이 존재하지 않는 빈 태그(empty tag)입니다.
    개행하고자 하는 곳에서 `<br>` 태그를 선언하면 개행이 됩니다.
    이처럼 `<p>` 태그를 이용하면 태그 자체에서 자연스럽게 개행이 되지만, `<p>` 태그 내부에서 강제로 개행을 하기 위해서는 `<br>` 태그를 이용해야 합니다.

    ---

    ### 참고자료

    [- : The HTML Section Heading elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements)

    [: The Paragraph element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p)

    [: The Line Break element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br)

- 텍스트를 꾸며주는 요소

    ### 텍스트 표현 태그

    웹 표준화가 대두하면서 웹 문서의 구조와 표현을 분리하였습니다.
    그 과정에서 많은 표현용 태그들이 사라졌고, 지금은 표현용 태그가 얼마 남지 않았습니다.
    그 중 `<b>`, `<i>`, `<u>`, `<s>`에 대해 살펴보도록 하겠습니다.

    - `<b>` : bold 태그는 글자를 굵게 표현하는 태그입니다.
    - `<i>` : 이전에는 italic 태그로 글자를 기울여서 표현하는 태그였으나,
    HTML5 버전에서는 `<i>` 태그가 단순 표현용 태그에서 의미를 가지는 태그로 변경 되었습니다. 특정 이유(기술적인 용어, 외국어 문구, 소설속 인물의 생각 등)로 다른 글자와 구분하기 위해 사용됩니다.
    - `<u>` : underline 태그는 글자의 밑줄을 표현하는 태그입니다.
    - `<s>` : strike 태그는 글자의 중간선을 표현하는 태그입니다. (예전에 존재했던 strike 태그와는 다른 태그로, strike 태그는 폐기되어 더는 사용할 수 없습니다.)

    위 태그들은 의미가 없는 표현용 태그이기 때문에 사용하실 때는 각별히 주의를 하셔야 합니다.

    ```html
    <p>
    	<b>Lorem</b> <i>ipsum</i> dolor sit amet<br>
    	<u>Lorem</u> <s>ipsum</s> dolor sit amet
    </p>
    ```

    ---

    ### 참고자료

    [HTML elements reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element#Inline_text_semantics)

- 시멘틱 마크업

    ### 시멘틱 마크업(semantic markup)이란?

    시멘틱 마크업은 종종 POSH(Plain Old Semantic HTML)라고도 불리는데, 단어 그대로 평범하고 오래된 의미론적인 HTML이라는 뜻입니다.
    시멘틱은 즉, 기계(컴퓨터, 브라우저)가 잘 이해할 수 있도록 하는 것을 뜻합니다.
    애초에 프로그래밍 언어는 사람과 기계와의 정해진 약속이며 HTML 역시 마찬가지입니다.
    시멘틱 마크업은 적절한 HTML 요소를 올바르게 사용하는 것에서 시작합니다.

    ### 시멘틱 마크업 하기

    그럼 어떻게 하면 브라우저가 코드를 잘 이해할 수 있을까요?
    간단합니다. 정해진 약속을 잘 지키면 됩니다.
    구체적으로 설명하자면 마크업 할 때는 의미에 맞는 태그, 요소를 사용하는 것이고
    문서를 표현할 때는 구조화를 잘 해주는 것입니다.
    정해진 약속대로 코드를 작성하게 되면 결국 기계뿐 아니라 사람도 이해하기 쉬운 코드가 됩니다.

    ```html
    <b>굵은</b> vs <strong>중요한</strong>
    <i>기울어진</i> vs <em>강조하는</em>
    <u>밑줄친</u> vs <ins>새롭게 추가된</ins>
    <s>중간선이 있는</s> vs <del>삭제된</del>
    ```

    위 코드를 작성해서 화면을 보면 각각의 요소가 같은 모습으로 표현되나 그 의미가 같지는 않습니다.
    `<b>`는 의미 없이 단순히 텍스트를 굵게 표현하는 태그지만, `<strong>`은 중요하다는 의미를 지닙니다.
    `<strong>`은 중요하다는 의미에 맞춰 브라우저에 의해 굵은 스타일로 표현된 것입니다.
    따라서 중요하다는 의미를 포함할 때는 `<b>`가 아닌 `<strong>`을 사용하는 것이 적절하고 시멘틱한 마크업입니다.

    이외에 `<i>`는 단순히 기울어진 글자를 표현하지만, `<em>`은 글자의 특정 부분을 강조하는 의미를 지닙니다.
    `<u>`와 `<s>`는 단순히 글자에 선을 그은 것이고, `<ins>`와 `<del>`은 내용이 새롭게 추가되거나 삭제가 되었다는 의미를 지닙니다.

    ### HTML5 시멘틱 요소

    HTML5에서 새로 생긴 Semantic 요소들입니다.

    - `<article>`
    - `<aside>`
    - `<figcaption>`
    - `<figure>`
    - `<footer>`
    - `<header>`
    - `<main>`
    - `<mark>`
    - `<nav>`
    - `<section>`
    - `<time>`

    ---

    ### 참고자료

    [Semantics](https://developer.mozilla.org/ko/docs/Glossary/Semantics)

    [HTML Semantic Elements](https://www.w3schools.com/htmL/html5_semantic_elements.asp)

- 앵커 요소

    ### 앵커(anchor) 태그

    HTML에서 HT(Hyper Text)는 링크를 의미하는 것으로, 링크는 클릭하기만 하면 다른 페이지로 쉽게 이동을 할 수 있습니다.
    앵커 태그는 이런 링크를 생성합니다.
    앵커 태그를 이용해 다른 페이지로 이동하거나 현재 페이지 내에서 특정 위치로 초점을 이동시킬 수 있습니다.
    HTML의 가장 큰 특징이 되는 태그이며, 그만큼 중요하고 자주 사용되는 태그입니다.

    <a>(anchor 태그)는 a태그, 앵커, 링크 등 여러 이름으로 불립니다.

    ```html
    <a href="http://www.google.com/" target="_blank">구글</a>
    ```

    ### href 속성

    링크를 만들기 위해 <a> 태그는 반드시 href(hypertext reference) 속성을 가지고 있어야 합니다.
    href 속성의 값은 링크의 목적지가 되는 URL 입니다.

    ### target 속성

    target 속성은 링크된 리소스를 어디에 표시할지를 나타내는 속성입니다.
    속성값으로는 _self, _blank, _parent, _top이 있습니다.
    _self는 현재 화면에 표시한다는 의미로, target 속성이 선언되지 않으면 기본적으로 self와 같이 동작합니다.
    _blank는 새로운 창에 표시한다는 의미로 외부 페이지가 나타나게끔 하는 속성입니다.
    _parent와 _top은 프레임이라는 특정 조건에서만 동작하는 속성으로,
    최근에는 프레임을 잘 쓰지 않기 때문에 따로 다루지 않고 넘어가겠습니다.

    ### 내부링크

    <a> 태그를 통해 만들어진 링크가 꼭 외부 페이지로만 이동하는 것은 아닙니다.
    <a> 태그를 통해 페이지 내부의 특정 요소로 초점을 이동할 수도 있는데, 이를 내부 링크라고 합니다.
    내부 링크를 사용할 때는 href 속성값에 #(해시태그)를 쓰고 그 뒤에 페이지 내에서 이동하고자 하는 요소의 id 속성값을 적으면 됩니다.

    ```html
    <h1 id="overview">개요</h1>

    ... 중략

    <a href="#overview">맨위로</a>
    ```

    보통 페이지에 내용이 많아 스크롤이 길어질 경우, 빠르게 화면 최상단으로 이동하고자 할 때 내부 링크를 주로 사용합니다.
    웹페이지에서 화면 하단에 있는 'top'또는 '맨 위로 이동하기' 버튼이 이에 해당합니다.

    ---

    ### 참고자료

    [](https://developer.mozilla.org/ko/docs/Web/HTML/Element/a)

- 의미가 없는 컨테이너 요소

    ### 의미없이 요소를 묶기 위한 태그(container)

    태그 자체에 아무 의미가 없으며, 단순히 요소들을 묶기 위해 사용되는 태그입니다.
    스타일을 주거나 서버에 보내는 데이터를 담기 위한 용도로 이런 의미 없는 요소들이 사용됩니다.
    이런 의미 없는 태그의 사용 빈도는 매우 높습니다.
    그 이유는 html 태그들은 문서를 웹에 나타내기 위해 제작되어 기본적으로 문서에 최적화 되어있는 의미를 지니는데, 현재 웹의 형태는 문서 형태에서 많이 벗어났기 때문입니다.
    다행히 HTML 버전이 업그레이드 되면서 웹에 알맞은 태그들이 많이 생겼습니다.
    가장 대표적으로 많이 쓰이는 의미가 없는 태그는 `<div>`, `<span>`입니다.

    ### `<div>`태그와 `<span>`태그

    div(division) 태그는 블록 레벨 태그입니다.
    블록 레벨 요소는 기본적으로 한 줄을 생성해서 내용을 표현합니다.
    반면, span 태그는 인라인 레벨 태그입니다.
    인라인 레벨 요소들은 블록 레벨 요소의 한 줄 안에서 표현되는 요소들입니다.

    이전에 배운 `<p>` 태그는 블록 레벨 태그이며,
    그 안에서 텍스트를 꾸며주는 `<b>`, `<i>`, `<u>`, `<s>`는 모두 인라인 레벨 태그입니다.

    ```html
    <div>
    	<span>Lorem</span> ipsum dolor sit.
    </div>
    ```

    `<div>`, `<span>`은 모두 아무 의미가 없으므로 실제 브라우저도 별다른 스타일을 적용하지 않습니다.

    ---

    ### 참고자료

    [: The Content Division element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div)

    [](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/span)

- 리스트 요소

    ### 리스트를 표현하는 태그

    리스트는 일련된 항목들이 나열된 것들을 의미합니다.
    콘텐츠가 많은 포털이나 검색 엔진같은 사이트에는 분야나 항목으로 구분할 것이 많으므로 리스트가 자주 사용됩니다.

    ### `<ul>` 태그

    ul(unordered list) 태그는 순서가 없는 리스트를 표현할 때 사용합니다.

    ```html
    콩나물국 재료
    <ul>
    	<li>콩나물</li>
    	<li>파</li>
    	<li>국 간장</li>
    </ul>
    ```

    콩나물국에 들어가는 일부 재료들을 나열한 리스트입니다.
    각 재료는 나오는 순서가 바뀌어도 상관이 없으므로 순서가 없는 리스트로 표현할 수 있습니다.
    `<ul>` 태그를 선언한 후 그 아래 각각의 항목들, 재료들을 리스트라는 `<li>` 태그를 이용하여 각 항목을 나타냅니다.

    ### `<ol>` 태그

    ol(ordered list) 태그는 순서가 있는 리스트를 표현할 때 사용합니다.

    ```html
    콩나물국 레시피
    <ol>
    	<li>냄비에 국물용 멸치를 넣고 한소끔 끓여 멸치 육수를 7컵(1,400ml) 만든다.</li>
    	<li>콩나물을 넣고 뚜껑을 덮어 콩나물이 익을 때까지 끓인다.</li>
    	<li>뚜껑을 열고 대파, 마늘, 고춧가루를 넣고 끓인다.</li>
    </ol>
    ```

    콩나물국을 끓이는 순서를 나열한 리스트입니다.
    이 순서는 서로 바뀌면 안되기 때문에 순서가 있는 리스트를 사용해야 합니다.
    `<ol>` 태그를 선언한 후 그 안에서 `<li>` 태그를 사용해 각 항목을 나타냅니다.

    ### `<dl>`태그

    dl(definition/description list) 태그는 용어와 그에 대한 정의를 표현할 때 사용합니다.
    `<dl>` 태그는 앞서 배운 `<ul>`, `<ol>` 태그와는 구조가 조금 다릅니다.
    `<ul>`, `<ol>`은 항목을 단순히 나열하는 구조지만,
    `<dl>`은 용어와 설명이 하나의 세트로 항목을 이루고 하나 이상의 항목으로 리스트가 이루어지는 구조입니다.

    ```html
    <dl>
    	<dt>HTML</dt>
    	<dd>The language for building web pages</dd>
    	<dd>HTML is the standard markup language for Web pages</dd>
    	<dt>CSS</dt>
    	<dd>The language for styling web pages</dd>
    	<dt>JavaScript</dt>
    	<dd>The language for programming web pages</dd>
    </dl>
    ```

    - `<dt>` : 용어를 나타내는 태그
    - `<dd>` : 용어에 대한 정의 또는 설명을 나타내는 태그

    용어 하나에 여러 정의가 들어갈 때에는 `<dd>` 태그를 한 개 이상 쓰는 것이 가능합니다.

    ---

    ### 참고자료

    [: The Unordered List element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul)

    [: The Ordered List element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol)

    [: The Description List element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dl)

- 이미지 요소

    ### 이미지(image) 태그

    `<img>` 태그는 문서에 이미지를 삽입하는 태그로 닫는 태그가 없는 빈 태그 입니다.

    ```html
    <img src="./images/logo.png" alt="로고">
    ```

    ### src 속성

    `<img>`의 필수 속성으로 이미지의 경로를 나타내는 속성입니다.
    반드시 들어가야 하는 필수 속성입니다.

    ### alt 속성

    이미지의 대체 텍스트를 나타내는 속성입니다.
    대체 텍스트는 이미지를 대체하는 글을 뜻하며 웹 접근성 측면에서 중요한 속성입니다.
    src 속성과 더불어 반드시 들어가야 하는 속성입니다.

    ### width / height 속성

    이미지의 가로/세로 크기를 나타내는 속성입니다.
    값의 단위는 필요하지 않으며 값을 입력하면 자동으로 픽셀 단위로 계산됩니다.
    width/height는 선택적인 속성이지만 이미지의 크기가 고정적이라면 width/height 속성을 선언하는 것이 성능적인 측면에서 좋습니다.
    width/height 속성이 없으면 이미지는 원본 크기대로 노출되며,
    둘 중 하나만 선언하면 나머지 한 속성은 선언한 속성의 크기에 맞춰 자동으로 비율에 맞게 변경됩니다.
    반면 두 속성 모두 선언하면 이미지는 비율과 무관하게 선언한 크기대로 변경됩니다.

    ### 상대경로와 절대경로

    src 속성에는 이미지의 경로가 들어가며 이미지의 상대경로와 절대경로가 있습니다.
    상대경로는 현재 웹 페이지를 기준으로 상대적으로 이미지의 위치를 나타내는 경로이고,
    절대경로는 실제 그 이미지가 위치한 곳의 전체 경로입니다.

    ```html
    <!-- 상대경로 -->
    <img src="./images/logo.png" alt="로고">

    <!-- 절대경로 -->
    <img src="/Users/jb1113/BoostCourse/html/images/logo.png" alt="로고">
    <img src="http://placehold.it/500x250" alt="dummy">
    ```

    상대 경로에서의 './'는 페이지가 있는 현재 폴더를 나타냅니다.
    상위 폴더는 '../'로 표현합니다.

    ### 이미지 파일 포맷 형식

    - .gif : 제한적인 색을 사용하고 용량이 적으며 투명 이미지와 애니메이션 이미지를 지원하는 형식
    - .jpg : 사진이나 일반적인 그림에 쓰이며 높은 압축률과 자연스러운 색상 표현을 지원하는 형식 (투명을 지원하지 않습니다.)
    - .png : 이미지 손실이 적으며 투명과 반투명을 모두 지원하는 형식

    ---

    ### 참고자료

    [: 이미지 삽입 요소](https://developer.mozilla.org/ko/docs/Web/HTML/Element/img)

- 테이블 요소

    ### 테이블(table) 태그

    `<table>` 태그는 이름에서 느껴지는 바와 같이 데이터를 표로 나타낼 때 사용되는 태그입니다.
    복잡한 데이터들을 기술할 때 표를 많이 사용합니다.

    ### 표의 구성 요소

    표는 셀(내용이 들어가는 하나의 칸)로 이루어져 있습니다.
    표의 행(가로 방향)을 row, 열(세로 방향)을 column이라고 합니다.

    - `<table>` : 표를 나타내는 태그
    - `<tr>` : 행을 나타내는 태그
    - `<th>` : 제목 셀을 나타내는 태그
    - `<td>` : 셀을 나타내는 태그

    하나의 `<table>`은 하나 이상의 `<tr>`로 이루어져 있으며,
    `<tr>`은 셀을 나타내는 `<th>`, `<td>`를 자식으로 가지게 됩니다.
    표를 구성할 때는 위에서 밑으로, 좌측에서 우측으로 작성하면 됩니다.

    ```html
    <table>
    	<tr>
    		<td>1</td>
    		<td>2</td>
    		<td>3</td>
    		<td>4</td>
    	</tr>
    	<tr>
    		<td>5</td>
    		<td>6</td>
    		<td>7</td>
    		<td>8</td>
    	</tr>
    	<tr>
    		<td>9</td>
    		<td>10</td>
    		<td>11</td>
    		<td>12</td>
    	</tr>
    	<tr>
    		<td>13</td>
    		<td>14</td>
    		<td>15</td>
    		<td>16</td>
    	</tr>
    </table>
    ```

    위는 1부터 16을 표현한 4행 4열의 표를 나타내는 코드입니다.
    브라우저 화면을 확인해보면 테두리가 없어 표가 어색해 보일 수 있습니다.
    브라우저에서 제공하는 테이블의 기본 스타일에는 테두리가 없기 때문입니다.
    확인을 위해 아래의 CSS 코드를 `<head>` 태그 안에 입력하면 테두리가 나타나는 것을 확인할 수 있습니다.

    ```html
    <head>
    	<style>
    		th, td {border: 1px solid;}
    	</style>
    </head>
    ```

    ### 표의 구조와 관련된 태그

    표가 복잡해지면 표를 해석해서 음성으로 전달해야 하는 스크린 리더기와 같은 보조 기기를 통해서는 표의 내용을 이해하는 것이 더욱 어려워질 것입니다.
    따라서 표를 구조적으로 파악하기 위해 도움이 되는 태그를 사용해야 합니다.

    - `<caption>` : 표의 제목을 나타내는 태그
    - `<thead>` : 제목 행을 그룹화하는 태그
    - `<tbody>` : 본문 행을 그룹화하는 태그
    - `<tfoot>` : 바닥 행을 그룹화하는 태그

    ```html
    <table>
    	<caption>Monthly Savings</caption>
    	<thead>
    		<tr>
    			<th>Month</th>
    			<th>Savings</th>
    		</tr>
    	</thead>
    	<tbody>
    		<tr>
    			<td>January</td>
    			<td>$100</td>
    		</tr>
    		<tr>
    			<td>February</td>
    			<td>$80</td>
    		</tr>
    	</tbody>
    	<tfoot>
    		<tr>
    			<td>Sum</td>
    			<td>$180</td>
    		</tr>
    	</tfoot>
    </table>
    ```

    `<tfoot>`은 `<thead>` 다음에 있지만 실제 화면에서는 표의 맨 아래에 위치하게 된다는 점을 주의해야 합니다.

    * HTML 버전에 따라  `<tfoot>`의 위치가 변경되었습니다.

    - HTML4 : `<tfoot>` 위치가 `<tbody>` 전에 위치합니다. 이유는 데이터의 양이 (`<tbody>`) 잠재적으로 매우 클수도 있기 때문에 그 전에 `<tfoot>`을 렌더해야 했기 때문입니다.
    - HTML5 : `<tfoot>`의 위치가 `<tbody>` 앞에 와도 되고, 뒤에 와도 상관없습니다.
    - HTML5.1 ~ 현재(5.2) : `<tfoot>`이 `<tbody>` 뒤에 위치해야 합니다. `<tfoot>`의 위치가 `<tbody>` 앞에 나올 경우 웹 접근성의 키보드의 초점 이동 순서 항목에 문제가 있기 때문에 변경되었습니다.

    ### 셀 병합

    테이블 관련 속성으로 셀을 병합하는 속성이 있습니다.
    셀을 가로 방향으로 병합할 건지 아니면 세로 방향으로 병합할 건지에 따라서 colspan, rowspan 속성을 사용합니다.
    속성 값에는 병합할 셀의 개수를 적어주시면 됩니다.

    - colspan : 셀을 가로 방향으로 병합
    - rowspan : 셀을 세로 방향으로 병합

    ```html
    <table>
    	<caption>Monthly Savings</caption>
    	<thead>
    		<tr><th>Month</th><th>Savings</th></tr>
    	</thead>
    	<tbody>
    		<tr>
    			<td>January</td>
    			<td>%100</td>
    		</tr>
    		<tr>
    			<td>February</td>
    			<td rowspan="2">$80</td>
    		</tr>
    		<tr>
    			<td>March</td>
    		</tr>
    	</tbody>
    	<tfoot>
    		<tr>
    			<td colspan="2">Sum</td>
    		</tr>
    	</tfoot>
    </table>
    ```

    ---

    ### 참고자료

    [: The Table element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table)

    [https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td#attr-colspan](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td#attr-colspan)

    [https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td#attr-rowspan](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td#attr-rowspan)

- 폼 요소

    웹 사이트에는 사용자의 입력을 요구하는 때도 있습니다.
    예를 들어 사용자로부터 텍스트를 입력받거나 아니면 선택을 하게끔 하는 경우가 이에 해당합니다.
    사용자로부터 데이터를 받아야 하는 경우 사용되는 요소들을 폼 요소라고 합니다.

    ### 폼(form) 태그

    `<form>` 태그는 서버에 데이터를 전달하기 위한 요소이며 `<input>`은 대표적인 폼 요소입니다.
    `<input>`은 내용이 없는 빈 요소이며 type 속성을 통해 여러 종류의 입력 양식으로 나타나게 됩니다.

    ### `<input>` 태그

    ### type="text"

    ```html
    <input type="text" placeholder="아이디">
    ```

    주로 아이디, 비밀번호, 이름, 주소, 전화번호 등 단순한 텍스트를 입력할 때 사용합니다.
    type="text"에는 placeholder 속성이 존재합니다.
    placeholder 속성은 사용자가 입력하기 전 미리 화면에 노출하는 값으로 입력하는 값의 양식을 표현할 수 있습니다.

    ### type="password"

    ```html
    <input type="password">
    ```

    암호와 같이 공개할 수 없는 내용을 입력할 때 사용합니다.
    화면에는 type="text'와 같게 나타나지만 실제로 입력할 때 값을 노출하지 않습니다.

    ### type="radio"

    ```html
    <input type="radio" name="gender" checked> 남자
    <input type="radio" name="gender"> 여자
    ```

    라디오 버튼을 만들 때 사용합니다.
    라디오 버튼은 중복 선택이 불가능하며 하나의 항목만을 선택해야 합니다.

    ### type="checkbox"

    ```html
    <input type="checkbox" name="hobby"> 음악감상
    <input type="checkbox" name="hobby" checked> 운동
    <input type="checkbox" name="hobby"> 요리
    ```

    체크박스를 만들 때 사용합니다.
    체크박스는 중복 선택이 가능합니다.

    ### name, checked 속성

    라디오 버튼과 체크박스에는 checked, name 속성이 존재합니다.
    name 속성은 라디오 버튼과 체크박스를 그룹화 시켜주는 속성입니다.
    checked 속성은 값이 별도로 존재하지 않는 boolean 속성입니다.
    boolean 속성은 true/false 둘 중 하나의 값을 가지며 속성이 존재하면 true,
    속성이 존재하지 않으면 false를 가집니다.

    ### type="file"

    ```html
    <input type="file">
    ```

    파일을 서버로 전송할 때 사용합니다.
    브라우저에 따라 표현되는 형태는 조금씩 다르지만 모두 같은 역할을 합니다.

    ### type="submit", "reset", "button", "image"

    ```html
    <form action="./receive.html">
    	message : <input type="text" name="message"><br>
    	<input type="submit" value="전송">
    	<input type="reset" value="취소">
    	<input type="button" value="등록">
    	<input type="image" src="./images/login_button" alt="로그인" width="100" height="50">
    </form>
    ```

    submit, reset, button, image 타입은 모두 클릭 가능한 버튼을 만듭니다.

    - submit : form에 입력된 값을 서버로 전송합니다.
    - reset : form에 입력된 값을 초기화 합니다.
    - button : 아무 기능이 없는 버튼을 생성합니다.
    - image : 이미지를 삽입할 수 있는 버튼을 생성합니다. (submit과 동일한 동작을 합니다.)

    이미지 버튼은 이미지 관련 속성인 src, alt 속성이 반드시 필요하며 submit 버튼과 동일하게 서버로 값을 전송합니다.

    ### `<SELECT>` 태그

    `<select>` 태그는 선택 목록 상자 또는 콤보박스라고도 합니다.
    몇 개의 선택지를 리스트 형태로 노출하고 그 중 하나를 선택할 수 있게 하는 태그입니다. (multiple 속성을 사용하면 다중 선택도 가능합니다.)

    ```html
    <select>
    	<option>서울</option>
    	<option selected>인천</option>
    	<option>경기</option>
    	...
    </select>
    ```

    `<select>` 내부에 `<option>`으로 각 항목을 나타냅니다.
    `<option>`의 속성으로는 selected가 있으며 이는 선택된 항목을 의미합니다.

    ### `<textarea>` 태그

    한 줄만을 입력할 수 있는 `<input type="text">`와 달리 여러 줄의 텍스트를 입력할 때 사용합니다.

    ```html
    <textarea rows="5" cols="100">
    ...
    </textarea>
    ```

    `<textarea>` 태그에는 텍스트 상자의 크기를 조절하는 rows, cols 속성이 있습니다.

    - cols : 가로 크기를 조절하는 속성 (한 줄에 들어가는 글자의 수, 수치의 의미는 평균적인 글자의 너비로 정확히 글자 수를 나타내지는 않습니다.)
    - rows : 세로 크기를 조절하는 속성 (화면에 보여지는 줄 수)

    ### `<button>` 태그

    버튼을 만들 때 사용하며 submit, reset, button 3가지의 타입이 있습니다.

    ```html
    <button type="submit">전송</button>
    <button type="reset">취소</button>
    <button type="button">등록</button>
    ```

    각 버튼은 이전에 배웠던 input 태그의 submit, reset, button과 모두 같은 기능을 가진 버튼입니다.
    다만, 빈 태그가 아니며 내용을 안에 직접 넣을 수 있으므로 좀 더 자유로운 스타일 표현이 가능합니다.

    ### `<label>` 태그

    `<label>` 태그는 form 요소의 이름과 form 요소를 명시적으로 연결시켜주기 위해 사용합니다.
    모든 form 요소에 사용할 수 있습니다.

    ```html
    <label for="name">닉네임</label>
    <input type="text" id="name"><br>
    <label for="password">비밀번호</label>
    <input type="password" id="password"><br>
    성별
    <label for="male">남자</label>
    <input type="radio" id="male" name="gender" checked>
    <label for="female">여자</label>
    <input type="radio" id="female" name="gender">
    ```

    form 요소의 id 속성값과 `<label>` 태그의 for 속성값을 같게 적어주어야 합니다.
    `<label>`을 사용하면 이를 클릭했을 경우 해당 form 요소를 클릭한 것처럼 동작합니다.
    또한, 스크린 리더기를 통해 듣게 되면 해당 form 요소에 접근 시 `<label>`을 함께 읽어주게 됩니다.
    `<label>`은 사용성, 접근성적인 측면으로 중요한 역할을 하므로 반드시 써주는 것이 좋습니다.

    ### `<fieldset>`, `<legend>` 태그

    `<fieldset>`, `<legend>` 태그는 form 요소를 구조화 하기 위해 필요한 태그입니다.

    - `<fieldset>` : 여러 개의 폼 요소를 그룹화하여 구조적으로 만들기 위해 사용
    - `<legend>` : 폼 요소의 제목으로 <fieldset> 요소 내부에 작성

    `<fieldset>`은 보통 form의 성격에 따라 구분합니다.
    `<legend>`는 `<fieldset>`의 자식으로 반드시 최상단에 위치해야 합니다.

    ```html
    <fieldset>
    	<legend>기본 정보</legend>
    	아이디, 비밀번호, 성별 폼 요소
    	...
    </fieldset>
    <fieldset>
    	<legend>부가 정보</legend>
    	취미, 지역, 프로필 사진, 지역, 자기소개 폼 요소
    	...
    </fieldset>
    ```

    ### `<form>` 태그

    `<form>` 태그는 form 요소들을 감싸는 태그로 데이터를 묶어서 실제 서버로 전송해주는 역할을 하는 태그입니다.
    만약 `<fieldset>`으로 구조화되어 있다면 `<fieldset>`도 함께 감싸는 역할을 합니다.

    ```html
    <form action="./receive" method="post">
    	<fieldset>
    		<legend>기본 정보</legend>
    		...
    	</fieldset>
    	<fieldset>
    		<legend>부가 정보</legend>
    		...
    	</fieldset>
    </form>
    ```

    `<form>` 태그에는 대표적인 2가지 속성이 있습니다.

    - action : 데이터를 처리하기 위한 서버의 주소
    - method : 데이터를 전송하는 방식

    method 속성값에는 GET/POST 2가지 방식이 존재합니다.
    GET 방식은 데이터가 전송될 때 주소창에 파라미터 형태로 붙어 데이터가 노출됩니다.
    반면, POST 방식은 데이터가 전송될 때 데이터가 노출되지 않습니다.

    ---

    ### 전체 코드

    ```html
    <!DOCTYPE html>
    <html lang="ko">
    	<head>
    		<meta charset="UTF-8">
    		<title>form</title>
    	</head>
    	<body>
    		<form action="./receive" method="post">
    			<h1>Form 관련 요소</h1>
    			<fieldset>
    				<legend>기본 정보</legend>
    					<label for="name">아이디: </label>
    					<input type="text" id="name" placeholder="영문 아이디를 입력해주세요"><br>
    					<label for="password">비밀번호: </label>
    					<input type="password" id="password"><br>
    					성별: 
    					<label for="male">남자</label>
    					<input type="radio" id="male" name="gender" checked>
    					<label for="female">여자</label>
    					<input type="radio" id="female" name="gender"><br>
    			</fieldset>
    			<fieldset>
    				<legend>부가 정보</legend>
    					취미: 
    					<label for="music">음악감상</label>
    					<input type="checkbox" id="music" name="hobby">
    					<label for="exercise">운동</label>
    					<input type="checkbox" id="exercise" name="hobby" checked>
    					<label for="cooking">요리</label>
    					<input type="checkbox" id="cooking" name="hobby"><br>
    					...
    			</fieldset>
    			<button type="submit">전송</button>
    			<button type="reset">취소</button>
    		</form>
    	</body>
    </html>
    ```

    ---

    ### 참고자료

    [](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)

    [: The Input (Form Input) element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)