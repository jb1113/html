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

    ### 참고링크

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