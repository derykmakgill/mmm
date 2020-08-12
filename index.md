---
layout: home
---

<section id="blog">
   {% for post in site.posts %}
       {% assign currentDate = post.date | date: "%Y" %}
       {% if currentDate != myDate %}
           {% unless forloop.first %}</ul>{% endunless %}
    <ul style="list-style: none; padding-left: 0px;">
           {% assign myDate = currentDate %}
       {% endif %}
 <li><time datetime="{{post.date}}"> {{ page.date | date_to_long_string }} </time> <a href="{{ post.url }}">{{ post.title }}</a></li>
       {% if forloop.last %}</ul>{% endif %}
{% endfor %}

</section>
