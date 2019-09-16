---
# Change the Keyword to Search Term
# edit the product list in csv, or edits products in yml and change data.product to data.products

layout: 
keyword: New Table of Content Generator
---

<div class="main">
  <ul class="cards">
  {% for item in site.data.productz %}
    <li class="cards_item">
      <div class="card">
        <a href="{{ item.link }}" rel="nofollow"><div class="card_image"><img src="{{ item.img }}"></div></a>
        <div class="card_content">
          <a href="{{ item.link }}" rel="nofollow"><h2 class="card_title">{{ item.name }}</h2></a>
          <p class="card_text">{{ item.description }}</p>
         <a href="{{ item.link }}" rel="nofollow"><button class="btn card_btn">See Price</button></a>
        </div>
      </div>
    </li>
     {% endfor %}         
  </ul>
</div>
