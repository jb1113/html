# HTML 이해하기

- HTML 소개

    **H**yper **T**ext **M**arkup **L**anguage

    - 웹 페이지를 만드는 언어
    - Hyper Text = [Link](http://google.com)(링크)
    - Markup Language
    - 확장자로 .html 사용

    [http://google.com](http://google.com)

    ### HTML이란?

    HTML은 프로그래밍 언어로 웹 페이지를 만들 때 사용됩니다.
    웹 사이트들이 모두 HTML을 사용하여 만들어집니다.

    ### HTML의 의미와 특징

    HTML은 Hyper Text Markup Language의 줄임말 입니다.
    Hyper Text는 단순한 텍스트를 넘어서 웹 페이이지의 특정 부분과 연결할 수 있는 기능을 가진 텍스트 즉, 링크를 의미합니다.
    Markup Language는 프로그래밍 언어의 한 종류로 정보를 구조적, 계층적으로 표현 가능하다는 특징이 있습니다.
    HTML은 파일 확장자로 .html을 쓰며, 그 파일 안에 html 코드를 작성하게 됩니다.

    ### HTML의 역사

    HTML은 1990년대 영국의 물리학자 팀 버너스리가 제안하여 개발되었습니다.
    초기 개발 목적은 연구소의 연구원들이 신속하게 정보와 문서를 공유하기 위해서였습니다.
    현재의 웹은 문서의 형태는 아니지만, 정보를 공유한다는 목적은 여전히 같습니다.

    ---

    ### 참고 자료

    [HTML: Hypertext Markup Language](https://developer.mozilla.org/ko/docs/Web/HTML)

- HTML 문법
    - 태그

        ### 태그(tag)란?

        HTML은 태그들의 집합이며, 태그는 HTML에서 가장 중요하고 기본이 되는 규칙입니다.
        태그는 '무언가를 표시하기 위한 꼬리표, 이름표'라는 의미가 있으며, HTML에서도 이와 비슷한 의미로 해석됩니다.
        우리가 다양한 태그들을 이용해 코드를 작성하면, 브라우저가 이를 인식해 내용을 표현하게 됩니다.

        ### 태그를 사용하는 방법

        태그는 <, > 기호로 표현하며 <, > 기호 사이에 태그 이름이 들어갑니다.
        대부분 태그는 시작 태그와 종료 태그로 이루어지며 종료 태그는 태그 이름 앞에 '/' 기호가 붙습니다.
        시작 태그와 종료 태그 사이에 실제 화면에 나타나는 내용이 위치하게 됩니다.

        ```html
        <h1>Hello, HTML</h1>
        ```

        위는 태그의 가장 기본적인 예로, `<h1>`을 사용해 'Hello, HTML'을 출력하는 코드입니다.

        ### 요소(element)란?

        내용을 포함한 태그 전체를 요소(Element)라고 합니다.
        태그와 요소는 의미가 다르지만 많은 사람이 태그와 요소를 같은 의미로 사용하니 혼동하지 않도록 주의해야 합니다.

        ### 정리

        HTML에는 많은 종류의 태그들이 있습니다.
        태그는 각각의 의미가 있으며 이 의미에 맞게 태그를 사용해야 합니다.
        또한, 태그는 HTML뿐만 아니라 XML, SGML, XHTML 등 다양한 마크업 언어에서 모두 사용됩니다.

        ---

        ### 참고자료

        [HTML: Hypertext Markup Language](https://developer.mozilla.org/ko/docs/Web/HTML)

        [HTML 요소 참고서](https://developer.mozilla.org/ko/docs/Web/HTML/Element)

    - 속성

        ### 속성(attribute)이란?

        속성은 태그에 추가로 정보를 제공하거나 태그의 동작이나 표현을 제어할 수 있는 설정값을 의미합니다.

        ### 속성을 사용하는 방법

        속성은 이름과 값으로 이루어져 있습니다.
        시작 태그에서 태그 이름 뒤에 공백으로 구분 후 속성 이름="속성값"으로 표현합니다.
        속성값은 홑따옴표(')와 쌍따옴표(")로 감싸 표현합니다.

        ```html
        <h1 id="title">Hello, HTML</h1>
        ```

        위는 `<h1>`에 id 속성을 추가해 title 값을 선언한 코드입니다.

        ### 여러 속성을 사용하는 방법

        의미와 용도에 따라 여러 속성이 존재하며 하나의 태그에 여러 속성을 선언할 수 있습니다.
        여러 속성을 선언할 때는 공백으로 구분해서 사용합니다.

        ```html
        <h1 id="title" class="main">Hello, HTML</h1>
        ```

        위는 `<h1>`에 id와 class 2개의 속성을 선언한 코드입니다.
        속성의 선언 순서는 태그에 영향을 미치지 않으며 class를 id보다 먼저 선언해도 결과는 같습니다.

        ### 속성의 종류

        속성은 종류에 따라 모든 태그에 사용할 수 있는 글로벌 속성과 특정 태그에서만 사용할 수 있는 속성으로 구분됩니다.
        또한, 선택적으로 쓸 수 있는 속성과 특정 태그에서 필요한 필수 속성으로 구분됩니다.
        위의 예시에서 쓰인 id와 class 속성은 글로벌 속성입니다.

        ---

        ### 참고자료

        [HTML 특성 참고서](https://developer.mozilla.org/ko/docs/Web/HTML/Attributes)

        [HTML Global attributes](https://www.w3schools.com/tags/ref_standardattributes.asp)

        [HTML Attributes](https://www.w3schools.com/tags/ref_attributes.asp)

    - 태그의 중첩

        ### 태그의 중첩(nesting tags)이란?

        태그 안에 다른 태그를 선언할 수 있습니다.
        태그를 중첩해서 사용 시 중첩되는 태그는 부모 태그를 벗어나서는 안 됩니다.

        **[잘못된 태그 선언]**

        ```html
        <h1>Hello, <i>HTML</h1></i>
        ```

        `<h1>`안에서 `<i>`가 시작되었으나, `<i>`보다 부모인 `<h1>`의 종료 태그가 먼저 선언 되었습니다.
        이렇게 엇갈리게 태그를 선언하는 것은 올바르지 않습니다.

        **[올바른 태그 선언]**

        ```html
        <h1>Hello, <i>HTML</i></h1>
        ```

        `<i>`의 종료 태그를 먼저 선언해준 후 `<h1>`의 종료 태그를 선언해야 합니다.

        ### 정리

        태그 안에서는 중첩이 얼마나 되는지 어떤 태그를 쓰는지는 문제가 되지 않습니다.
        하지만 때에 따라 정해진 태그만 중첩할 수 있기도 합니다.
        태그의 구조 특성으로 인해 중첩할 수 없는 경우에 대해서는 블록 vs 인라인 부분에서 살펴보도록 하겠습니다.

        ---

        ### 참고자료

        [The W3C Markup Validation Service](http://validator.kldp.org/)

    - 빈 태그

        ### 빈 태그(empty tag)란?

        태그는 기본적으로 시작 태그와 종료 태그 2개가 1쌍으로 이루어져 있으며, 그 사이에 내용이 들어가게 됩니다.
        하지만 태그 중에는 그렇지 않은 태그가 존재하기도 합니다.
        이러한 태그를 내용이 없는 빈 태그라고 합니다.

        - `<br>`
        - `<img src="">`
        - `<input type="">`

        위는 빈 태그의 예시입니다.
        빈 태그는 내용이 없어서 종료 태그가 필요하지 않습니다.

        ### 빈 태그의 특징

        빈 태그는 내용만 비어있을 뿐 속성을 통해서 화면에 나타내거나 화면에 표시되지 않더라도 다른 용도로 사용되는 태그입니다.
        빈 태그의 대표적인 경우는 브라우저가 직접 화면에 내용을 그려줘야 하는 경우입니다.
        이런 태그는 브라우저가 내용을 대체한다고 하여 replacement 태그, 대체되는 태그라고 합니다.
        빈 태그에 대체되는 태그만 있는 것은 아니며 실제로 화면에 출력될 내용이 없어 다른 용도로 쓰이는 태그도 존재합니다.
        위 예시 코드의 `<br>`이 바로 이 경우입니다.

        ---

        ### 참고자료

        [빈 요소](https://developer.mozilla.org/ko/docs/Glossary/Empty_element)

    - 공백

        ### HTML에서의 공백(space)

        기본적으로 HTML은 두 칸 이상의 공백을 모두 무시합니다.

        ```html
        <h1>Hello, HTML</h1>
        <h1>Hello,     HTML</h1>
        <h1>
		Hello, 
		HTML
        </h1>
        ```

        HTML은 두 칸 이상의 공백과 개행을 모두 무시하기 때문에 위 세가지 모두 같은 텍스트가 화면에 나타나게 됩니다.

        ### 생각해보기

        이러한 공백처리 방식에 대해서 CSS로 제어할 수 있습니다.
        뒤에 단어 관련 속성 강의에서 다룰 속성이지만, 어떤 속성으로 공백을 제어할 수 있는지 한번 확인해 보세요.

        ---

        ### 참고 링크

        [How to Change Default Text Wrapping with HTML and CSS - Hongkiat](https://www.hongkiat.com/blog/change-default-text-wrapping-html-css/)

    - 주석
