---
# Change the Keyword to Search Term
# edit the product list in csv, or edits products in yml and change data.product to data.products

layout: 
keyword: New Table of Content Generator
---
<div id="`{{ page.keyword | slugify  }}`-quick-navigation"> 
    <div class="quick-nav-center-top">
        <ul id="{{ page.keyword | slugify  }}-ul">
            <a onclick="showproductlistdropdown()">Show Content<i class="arrow down"></i></a>
    </div>     
    <h3 class="regular-text">{{ page.keyword }}</h3> 
    <div id="best-product-list-div"> 
    {% for item in site.data.product %}
        <li class="list-link-{{ page.keyword | slugify  }}">
            <a class="link-{{ page.keyword | slugify  }}" href="#{{ item.name | slugify  }}-{{ item.position }}">{{ item.position }}. {{ item.name }}</a>
        </li>
        {% endfor %}         
            </div>
</ul>
