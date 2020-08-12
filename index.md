---
layout: home
---

Writer and researcher. I used to work in marketing.

---


<div><h2>Articles</h2>
   {% for post in site.posts %}
       {% assign currentDate = post.date | date: "%Y" %}
       {% if currentDate != myDate %}
           {% unless forloop.first %}</ul>{% endunless %}
    <ul style="list-style: none; padding-left: 0px;">
           {% assign myDate = currentDate %}
       {% endif %}
 <li><a href="{{ post.url }}">{{ post.title }}</a></li>
       {% if forloop.last %}</ul>{% endif %}
{% endfor %}

</div>
