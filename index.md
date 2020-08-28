---
layout: default
---

# mkgll's blog

<section id="blog">
   {% for post in site.posts %}
       {% assign currentDate = post.date | date: "%Y" %}
       {% if currentDate != myDate %}
           {% unless forloop.first %}</ul>{% endunless %}
    <ul style="list-style: none; padding-left: 0px;">
           {% assign myDate = currentDate %}
       {% endif %}
 <li><a href="{{ post.url }}">{{ post.title }}</a> <time datetime="{{post.date}}"> {{ post.date | date: "%m/%d/%Y" }} </time></li>
       {% if forloop.last %}</ul>{% endif %}
{% endfor %}

</section>
