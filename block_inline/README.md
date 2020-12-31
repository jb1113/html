# 블록 & 인라인

### 블록 레벨 요소

`<div>`, `<h1>`~`<h6>`, `<p>`, `<ul>`, `<li>`, `<table>`, ...

부모 요소의 가로 영역에 맞게 꽉 채워져 표현되는 요소입니다.
양옆으로 다른 요소가 배치되지 않게 박스를 생성하므로 박스의 위아래로 줄 바꿈이 생기게 됩니다.
블록 레벨 요소는 일반적으로 모든 요소(블록, 인라인 레벨 등)를 포함할 수 있습니다.

### 인라인 레벨 요소

`<span>`, `<a>`, `<i>`, `<img>`, `<em>`, `<strong>`, ...

하나의 라인 안에서 자신의 내용만큼의 박스를 만드는 요소입니다.
라인의 흐름을 끊지 않고 요소 앞 뒤로도 줄 바꿈이 되지 않아 다른 인라인 요소들이 자리할 수 있습니다.
인라인 레벨 요소는 블록 레벨 요소의 자식으로 분류되기 때문에 자손으로 블록 레벨 요소를 가질 수 없습니다.
즉, 인라인 레벨 요소는 블록 레벨 요소를 포함할 수 없습니다.

다만, HTML5 버전에서 생겨난 한가지 예외 경우가 있는데 `<a>`는 인라인 레벨 요소지만 자손으로 블록 레벨 요소를 가질 수 있습니다.

---

### 참고자료

[Block-level elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements)

[Inline elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements)