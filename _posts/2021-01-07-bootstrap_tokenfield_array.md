---
title: "[jQuery] Bootstrap Tokenfield에 2차원 배열 동적 세팅하는 법"
comments: true
layout: single
categories:
- javascript
---

안녕하세요.

혹시 부트스트랩 Tokenfield 사용하시는 분들 계신가요?

궁금하신 분들은 [bootstrap-tokenfield](https://sliptree.github.io/bootstrap-tokenfield/) 를 참고해보세요!

저는 부트스트랩 환경에서 개발중인데, 이번에 2차원 배열을 Tokenfield에

세팅해야 하는 작업이 필요해서 그 과정을 적어보려고 해요.

Tokenfield에 값을 세팅하는 법은 여러가지가 있지만, 그 중에서

```
$('#token_field').tokenfield('setTokens', ['apple','banana','tangerine']);
```

위 코드로 예를 들 수 있습니다.

그렇다면,

```
var arr_list = [["apple","banana"],["tangerine","pear"],["mango"]];
```

와 같은 이차원 배열을 여러 개의 Tokenfield에 세팅하려면 어떻게 해야할까요?

물론 이차원 배열의 값은 수시로 바뀔 수 있다고 가정합시다!

```
<div>
	<input type="text" id="token_field1" class="tokenfield">
</div>
<div>
	<input type="text" id="token_field2" class="tokenfield">
</div>
<div>
	<input type="text" id="token_field3" class="tokenfield">
</div>
															
for (var i = 0; i < arr_list.length; i++) {
    console.log("[TEST] : " + JSON.stringify(arr_list[i]) + "," + String((i + 1)));
    $('#token_field' + String((i + 1))).tokenfield('setTokens', arr_list[i]);
} // for
```

### 결과
[TEST] : ["apple","banana"], 1

[TEST] : ["tangerine","pear"], 2

[TEST] : ["mango"], 3

-

간단한 코드로 이차원 배열도 쉽게 Tokenfield에 동적으로 세팅할 수 있습니다.

오늘은 여기서 마치도록 하겠습니다!

잘못된 점은 댓글로 피드백 주시면 감사하겠습니다:)
