---
layout: default
---

Home

v-020

---
### dump just the 1 post
{{ post./2018/01/02/nn001 }}


---
### include 1
{% include 2018-11-11-nn011.md %}

### include 2
{% include sub1/hi.md %}

---
### site.url
{{site.url}}

### site.baseurl
{{site.baseurl}}

### list Posts
<ul class="myposts">
{% for post in site.posts %}
    <li><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a> {{ post.id }}
    <span class="postDate">{{ post.date | date: "%b %-d, %Y" }}</span>
    </li>
{% endfor %}
</ul>

### list pages
<ul class="myposts">
{% for page in site.pages %}
    <li><a href="{{ site.baseurl }}{{ page.url }}">{{ page.path}}</a>
    </li>
{% endfor %}
</ul>

### dump site.html_files
{{ site.html_files }}

### dump static
{{ site.static_files }}

