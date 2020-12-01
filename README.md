# HTML

### The language for building web pages

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

        ### 태그란?

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

        위는 태그의 가장 기본적인 예로, <h1>을 사용해 'Hello, HTML'을 출력하는 코드입니다.

        ### 요소란?

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
    - 태그의 중첩
    - 빈 태그
    - 공백
    - 주석
