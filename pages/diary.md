---
layout: page
title: 心情日记本
titlebar: diary
subtitle: <span class="mega-octicon octicon-organization"></span>&nbsp;&nbsp; 给生活抹点颜色
menu: cartoon
css: ['blog-page.css']
permalink: /diary
---

<div class="row">
    <div class="col-md-12">
        <ul id="posts-list">
            {% for post in site.posts %}
                {% if post.category=='diary' %}
                <li class="posts-list-item">
                    <div class="posts-content">
                        <span class="posts-list-meta">{{ post.date | date: "%Y-%m-%d" }}</span>
                        <a class="posts-list-name bubble-float-left" href="{{ site.url }}{{ post.url }}">{{ post.title }}</a>
                        <span class='circle'></span>
                    </div>
                </li>
                {% endif %}
            {% endfor %}
        </ul>
        <!-- Pagination -->
        {% include pagination.html %}
        <!-- Comments -->
       <div class="comment">
         {% include comments.html %}
       </div>
    </div>
</div>
<script>
    $(document).ready(function(){
        $("body").tooltip({ selector: '[data-toggle=tooltip]' });
    });
</script>