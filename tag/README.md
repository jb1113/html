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

- 제목과 단락요소

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
