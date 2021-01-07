---
title: "[GitHub] Jekyll 블로그에 Disqus 댓글 연동하는 법"
comments: true
categories:
- etc
---

안녕하세요.

오늘은 Jekyll 블로그에 Disqus 연동하는 법을 알아보도록 할게요.

저도 처음 블로그를 제작할 때 타 개발자님의 설명을 보면서 따라했는데,

그 과정에서 Disqus가 연동이 안되는 오류가 생겨 직접 해결한 후기를

작성해보려고 합니다!

### 1. Disqus 홈페이지 가입  : [https://disqus.com/](https://disqus.com/)

![Disqus_1](/assets/images/Disqus_1.PNG)

우선 Disqus 홈페이지에 접속해 회원가입을 진행합니다.

그 후, **GET STARTED** 버튼을 클릭합니다!

![Disqus_2](/assets/images/Disqus_2.PNG)

개인 블로그 설치를 위해 **I want to install Disqus on my site** 클릭

![Disqus_3](/assets/images/Disqus_3.PNG)

**Website Name** 을 적어줍니다.

*_config.yml*  파일을 수정할 때 필요하니 기억해두기로 합시다!

![Disqus_4](/assets/images/Disqus_4.PNG)

**Jekyll** 클릭!

### 2. Disqus 연동

![Disqus_5](/assets/images/Disqus_5.PNG)

**Universal Embed Code** 를 클릭해 줍니다.

![Disqus_6](/assets/images/Disqus_6.PNG)

오른쪽 상단에 있는 **Copy** 버튼을 통해 코드 복사!

![Disqus_7](/assets/images/Disqus_7.PNG)

*_includes* 폴더에 disqus.html 파일을 생성해 코드를 붙여넣기 해줍니다.

![Disqus_8](/assets/images/Disqus_8.PNG)

*_config.yml* 에 provider는 "disqus"로,

shortname은 조금 전 작성한 **Website Name**으로!

### 3. Jekyll 블로그에 Disqus 댓글 기능 추가

저는 localhost:4000/admin/ 에서 포스트를 작성하고 있는데요.

![Disqus_9](/assets/images/Disqus_9.PNG)

포스트 하단에 위 코드를 붙여넣기 하면 끝!

댓글 기능이 추가된 것을 보실 수 있습니다.

혹시 잘못된 점이 있을 시, 댓글을 통해 알려주시면 감사하겠습니다:) 


{% if page.comments %}
<div id="post-disqus" class="container">
{% include disqus.html %}
</div>
{% endif %}
