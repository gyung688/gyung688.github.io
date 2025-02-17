---
layout: post
title: Introduction
excerpt_separator:  
---

<p class="message">
좋은 개발자란 사용자에게 열려있는 개발자라고 생각합니다.
사용자의 환경을 깊이 이해하고 어떻게 하면 사용자에게 더 편하게 다가오는지 생각해얀하고 생각합니다.
그것이 서버에 직접 구축을 하는 방법이든 새로운 기술을 써야한다든 말이죠.

이런 개발자가 되려면 마라톤을 해야한다고 생각합니다.
천천히 계속 끊임없이 달리다보면 그에 다다르지 않을까요.

저는 욕심 많습니다.
일도 잘하면서 기술 블로그도 쓰고, 토이 프로젝트도 하며 실력을 늘리고싶습니다.
또 분석/설계부터 구현까지 모두를 어울러 잘하는 전문 엔지니어가 되고싶습니다.

점점 성장하는 저의 모습을 아래 기술 블로그와 깃허브에서 확인해보세요.

gitHub : https://github.com/gyung688/
blog : gyung688.github.io/blog/


마라토너 개발자
코더가 아닌 개발자가 되자.
가독성이 리팩토링하기 좋은 코드를 짜자.
사용자 입장에서 생각하자.
상황에 맞게 유연한 사고를 갖자. 
현실 세계를 코드로 표현하는 법을 연습하자.(추상화 -> 구현)
하나의 서비스가 기획되고 배포될 때 까지의 과정을 
질문의 방식은 '이것을 하고 싶고, 이런 문제가 생겼고, 이것을 시도해봤다.'

</p>

Hydeout updates the original [Hyde](https://github.com/poole/hyde)
theme for [Jekyll](http://jekyllrb.com) 3.x and 4.x and adds new functionality.

### Keep It Simple

In keeping with the original Hyde theme, Hydeout aims to keep the overall
design lightweight and plugin-free. JavaScript is currently limited only
to Disqus and Google Analytics (and is only loaded if you provide configuration
variables).

Hydeout makes heavy use of Flexbox in its CSS. If Flexbox is not available,
the CSS degrades into a single column layout.

### Customization

Hydeout replaces Hyde's class-based theming with the use
of the following SASS variables:

```scss
$sidebar-bg-color: #202020 !default;
$sidebar-fg-color: white !default;
$sidebar-sticky: true !default;
$layout-reverse: false !default;
$link-color: #268bd2 !default;
```

To override these variables, create your own `assets/css/main.scss` file.
Define your own variables, then import in Hydeout's SCSS, like so:

```
---
# Jekyll needs front matter for SCSS files
---

$sidebar-bg-color: #ac4142;
$link-color: #ac4142;
$sidebar-sticky: false;
@import "hydeout";
```

See the [_variables](https://github.com/fongandrew/hydeout/blob/master/_sass/hydeout/_variables.scss) file for other variables
you can override.

You can also insert custom head tags (e.g. to load your own stylesheets) by
defining your own `_includes/custom-head.html` or insert tags at the end
of the body (e.g. for custom JS) by defining your own
`_includes/custom-foot.html`.

### New Features

* Hydeout also adds a new tags page (accessible in the sidebar) and a new
  "category" layout for dedicated category pages.

* Category pages are automatically added to the sidebar. All other pages
  must have `sidebar_link: true` in their front matter to show up in
  the sidebar.

* A simple redirect-to-Google search is available. If you want to use
  Google Custom Search or Algolia or something with more involved,
  override the `search.html`.

* Disqus integration is ready out of the box. Just add the following to
  your config file:

  ```yaml
  disqus:
    shortname: my-disqus-shortname
  ```

  If you don't want Disqus or want to use something else, override
  `comments.html`.

* For Google Analytics support, define a `google_analytics` variable with
  your property ID in your config file.

There's also a bunch of minor tweaks and adjustments throughout the
theme. Hope this works for you!
