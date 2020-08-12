---
layout: home
---

I’m a software engineer working at the intersection of entertainment and technology. We’re talkin’ visual effects, VR / AR, and game development.

<p><strong>New:</strong> {% for post in site.posts limit:1 %}
  <a href="{{ post.url }}">
            {{ post.title }}
          </a>
{% endfor %}</p>

---

<section class="archive-post-list">
  <h2>Articles</h2>
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

</section>
