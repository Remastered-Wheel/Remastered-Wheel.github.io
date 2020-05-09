---
layout: post
title:  "Welcome to Jekyll!"
categories: jekyll update
---
Tota la informació extreta de [jekyll].
## Objects
page.title => {{ page.title }}

## [Tags][tags]
### [highlight] code:
{% highlight ruby linenos %}
def foo
  puts 'foo'
end
{% endhighlight %}
{% highlight kotlin %}
// like kotlin
fun foo() {
  println("poteitos")
}
{% endhighlight %}

### Links
[Link to index]({% link index.md %}), if the index.md modify the path, this change correctly.
One major benefit of using the `link` or `post_url` tag is link validation. If the link doesn’t exist, Jekyll won’t build your site.

## [Filters][filter]
For example capitalize the text: "{{ "capitalized" | capitalize }}"


## Referències
- [tutorial][jekyll]
- [docs][liquid]
  - [tags]
    - [highlight]
      - [pygments][highlight-pygments]
  - [filter]

[jekyll]:    https://jekyllrb.com/docs/step-by-step/02-liquid/
[liquid]:    https://jekyllrb.com/docs/liquid/
[filter]:    https://jekyllrb.com/docs/liquid/filters/
[tags]:      https://jekyllrb.com/docs/liquid/tags/
[highlight]: https://github.com/rouge-ruby/rouge/wiki/List-of-supported-languages-and-lexers
[highlight-pygments]: https://jwarby.github.io/jekyll-pygments-themes/languages/ruby.html
