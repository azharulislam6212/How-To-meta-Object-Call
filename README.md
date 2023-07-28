# How-To-meta-Object-Call

{% assign accordionItems = product.metafields.custom.info.value %}
    {% if accordionItems != blank %}

     
       
      <div class="accordion">
        {% for accordion in accordionItems %}
          <div class="accordion__item">
            <div class="accordion__title">
              <span>{{accordion.title  | metafield_tag}}</span>
              <img src="{{'expand.svg' | asset_url}}" alt="">
              </div>
            <div class="accordion__text">{{accordion.text | metafield_tag}}</div>

              {{accordion.clients_image | metafield_tag}}
          </div>
        {% endfor %}
      </div>
    {% endif %}
