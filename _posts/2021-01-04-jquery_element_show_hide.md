---
title: "[jQuery] 객체의 show(), hide() 여부 판단하기"
layout: single
comments: true
categories:
- javascript
---

안녕하세요.

오늘은 객체의 show()와 hide() 여부를 판단하는 구문을 작성해보겠습니다!

개발을 하다보면 특정 div를 나타내거나 숨김 처리를 할 수 있는데

이에 따른 처리가 필요할 때가 있습니다.

그럴 경우, 

***.is(:visible)***

```
 console.log($("#div_area").is(:visible)); 
```

을 통해 쉽게 알 수 있습니다. 결과 값은 True 또는 False가 나오게 됩니다.

```
if ($("#div_area").is(:visible)) { // div_area가 true일 때
	console.log("True");
} else { // div_area가 false일 때
	console.log("False");
}
```

이상입니다.

감사합니다!

{% if page.comments %}
<div id="post-disqus" class="container">
{% include disqus.html %}
</div>
{% endif %}
