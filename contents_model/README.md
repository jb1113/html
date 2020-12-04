# 콘텐츠모델

![https://developer.mozilla.org/@api/deki/files/6244/=Content_categories_venn.png](https://developer.mozilla.org/@api/deki/files/6244/=Content_categories_venn.png)

### Content Models의 7분류

1. Metadata Content
2. Flow Content
3. Sectioning Content
4. Heading Content
5. Phrasing Content
6. Embedded Content
7. Interactive Content

### 1. Metadata

'base, link, meta, noscript, script, style, title'

Metadata에는 콘텐츠의 스타일, 동작을 설정하거나 다른 문서와의 관계 등 정보를 포함하는 요소들이 포함됩니다.
메타 태그, 타이틀 태그, 스타일 태그, 링크 태그가 이에 해당하며 대부분 `<head>` 태그 내에 들어간다는 것이 특징입니다.

### 2. Flow

'a, abbr, address,map>area, article, aside,audio, b, bdo, blockquote,br, button,canvas, cite, code, datalist, del, details, dfn, div, dl, em, embed,fieldset, figure, footer, form, h1 ~ h6, header, hgroup, hr, i, iframe, img, input, ins, kbd, keygen, label, map, mark, math, menu, meter, nav, noscript, object, ol,output, p, pre, progress, q, ruby, samp, script, section, select, small, span, strong,style[scoped], sub, sup, svg, table, textarea, time, ul, var, video, wbr'

Flow에는 문서의 자연스러운 흐름에 의해 배치되는 요소들이 포함됩니다.
Metadata에 해당하는 일부 태그들만 Flow에서 제외되며 요소 대부분이 Flow에 포함됩니다.

### 3. Sectioning

'article, aside, nav, section'

Sectioning에는 문서의 구조와 관련된 요소들이 포함됩니다.
HTML5에서 새로 생긴 article, aside, nav, section 등이 포함되며 이 태그들은 문서의 구조, 아웃라인에 영향을 주게 됩니다.

### 4. Heading

'h1, h2, h3, h4, h5, h6'

Heading에는 각 section의 header를 정의하는 heading 태그가 포함됩니다.

### 5. Phrasing

`a, abbr, map>area, audio, b, bdo, br, button, canvas, cite, code, datalist, del, dfn, em, embed, i, iframe, img, input, ins, kbd, keygen, label, map, mark, math, meter, noscript, object, output, progress, q, ruby, samp, script, select, small, span, strong, sub, sup, svg, textarea, time, var, video, wbr`

Phrasing에는 문서의 텍스트 또는 텍스트를 꾸며주는 문단 내부 레벨로 사용되는 요소들이 포함됩니다.

### 6. Embedded

'audio, canvas, embed, iframe, img, math, object, svg, vedio'

Embedded에는 외부 콘텐츠를 표현하는 요소들이 포함되며 오디오나 비디오, 이미지 등 멀티미디어 관련 요소들이 이에 해당합니다.

### 7. Interactive

'a, audio[controls], button, details, embed, iframe, img[usemap], input, keygen, label, menu, object[usemap], select, textarea, video[controls]'

Interactive에는 사용자와 상호작용을 하는 요소들이 포함되며 대표적으로 form 요소들이 이에 해당합니다.

---

### 참고자료

[Content categories](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Content_categories)

[HTML5](https://www.w3.org/TR/2011/WD-html5-20110525/content-models.html)