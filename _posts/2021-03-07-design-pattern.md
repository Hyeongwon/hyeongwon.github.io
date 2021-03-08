---
layout: post
title:  "디자인 패턴은 왜 쓸까?"
date:   2021-03-07 16:00:59
author: 변형원
categories: design-pattern
cover:  "/assets/instacode.png"
---

## 디자인 패턴은 왜 쓸까? 꼭 써야 하는가?

<a href="/assets/7c3b3f0852a76.jpeg" data-lightbox="falcon9-large" data-title="Check out the Falcon 9 from SpaceX">
  <img src="/assets/7c3b3f0852a76.jpeg" title="Check out the Falcon 9 from SpaceX">
</a>

디자인 패턴이랑은 상관은 없지만,

간단하게 짤 수 있는 부분도 꼭 어렵게 짜는 사람이있다.

물론 (갑자기 * x 100개로 변경이 되면?) 같은 상황이 발생하면 왼쪽이 더 보기 좋긴하겠다.

그런데 모든 부분을 왼쪽 마냥 짜는게 좋은가?

직관적인게 가장 좋은 코드가 아닌가 하는 생각이 든다.

### 그럼 왜 쓰지?

사실 혼자 작업 하고, 혼자 유지보수 하면 자기 눈에 익숙한게 젤 좋다고 생각한다.

그런데 혼자 작업하는 경우 드물다.

그리고 기획은 수시로 바뀐다. (이건 원래 그렇다)

또 내가 작업한걸 꼭 내가 수정하지도 않는다.

이런 여러 이유를 보면 범용적이고 가독성이 높은 코드는 실무에서 꼭 필요하다고 생각한다.

그래서 패턴을 쓰지 않나 생각한다.

물론 이게 무조건적인 대안은 아니라곤 생각하지만...

### 디자인 패턴은 무엇인가?

gof 의 디자인 패턴에서 보면

여담이지만, gof 사람 이름이 아니라 (gang of four) 에릭 감마, 존 블리시데스, 리차드 헬름, 랄프 존슨 4명 이라서 gof 라고한다.

영미권에서 4인방을 저런식으로 표현하는구나. 잡 지식이 늘었다.




### Code Snippets

You can use [highlight.js][highlight] to add syntax highlight code snippets:

Use the [Liquid][liquid] `{% raw %}{% highlight <language> %}{% endraw %}` tag to add syntax highlighting to code snippets.

For instance, this template...
{% highlight html %}
{% raw %}{% highlight javascript %}    
function demo(string, times) {    
  for (var i = 0; i < times; i++) {    
    console.log(string);    
  }    
}    
demo("hello, world!", 10);
{% endhighlight %}{% endraw %}
{% endhighlight %}

...will come out looking like this:

{% highlight javascript %}
function demo(string, times) {
  for (var i = 0; i < times; i++) {
    console.log(string);
  }
}
demo("hello, world!", 10);
{% endhighlight %}

Syntax highlighting is done using [highlight.js][highlight]. You can change the active theme in [head.html](https://github.com/bencentra/centrarium/blob/2dcd73d09e104c3798202b0e14c1db9fa6e77bc7/_includes/head.html#L15).

### Blockquotes

> "Blockquotes will be indented, italicized, and given a subdued light gray font. These are good for side comments not directly related to your content, or long quotations from external sources." - Some Smart Guy

### Images

Lightbox has been enabled for images. To create the link that'll launch the lightbox, add <code>data-lightbox</code> and <code>data-title</code> attributes to an <code>&lt;a&gt;</code> tag around your <code>&lt;img&gt;</code> tag. The result is:

<a href="//bencentra.com/assets/images/falcon9_large.jpg" data-lightbox="falcon9-large" data-title="Check out the Falcon 9 from SpaceX">
  <img src="//bencentra.com/assets/images/falcon9_small.jpg" title="Check out the Falcon 9 from SpaceX">
</a>

For more information, check out the [Lightbox][lightbox] website.

### Tooltips

With Tippy.js, you can add tooltips to your text with a little bit of HTML and JavaScript. First, create the tooltip trigger: `<span class="tooltip" id="someId">trigger</span>`. Then in a `<script>` tag at the bottom of your page, add some code to initialize the tooltip when the document is ready: `window.tooltips.push(['#someId', { content: "Content" }])`

See the [Tippy.js docs](https://atomiks.github.io/tippyjs/) for additional configuration that you can provide for your tooltips.

You can also use a Liquid `include` to import tooltip text or HTML from an external file: 

```
window.tooltips.push(['#someOtherId', { content: "{% raw %}{% include tooltips/example.html %}{% endraw %}" }])
```

To modify the styles for tooltip triggers, find the `.tooltip` class in `_layout.scss`.

Here's an <span class="tooltip" id="someId">example tooltip</span>, and <span class="tooltip" id="someOtherId">here's another</span>.

<br/>
{% include page_divider.html %}

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
[highlight]:   https://highlightjs.org/
[lightbox]:    http://lokeshdhakar.com/projects/lightbox2/
[jekyll-archive]: https://github.com/jekyll/jekyll-archives
[liquid]: https://github.com/Shopify/liquid/wiki/Liquid-for-Designers

<script>
window.tooltips = window.tooltips || []
window.tooltips.push(['#someId', { content: "This is the text of the tooltip!" }])
window.tooltips.push(['#someOtherId', { content: "{% include tooltips/example.html %}", placement: "right" }])
</script>
