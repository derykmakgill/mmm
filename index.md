---
layout: home
---

I’m a software engineer working at the intersection of entertainment and technology. We’re talkin’ visual effects, VR / AR, and game development.

I studied computer science at the University of Waterloo and filmmaking at Vancouver Film School. At the latter I made a truly bonkers musical about a disgraced scientist who invents the spork.

On the professional side, I cofounded a startup and have worked at several others building games, middleware, cinematic tools, and web services. I'm particularly fond of Unity and Unreal Engine.

I’m also the M in comedy duo The S&M Experience. Just a couple of small town boys with big to medium sized city dreams.

Living in beautiful Vancouver, Canada.

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
