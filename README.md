# product-tabss

<div class="cgt-desc">
<div id="write-revieww" class="page-width">
 <ul class="tabs clearfix">
 <li><a href="#tab-1" class="active">Description</a></li>
 <li><a href="#tab-2">Reviews</a></li>
 </ul>
 </div>
 <div class="cgt-content">
   <div class="page-width">
 <div id="tab-1" class="tab active">
  {{product.description}}
 </div>
 <div id="tab-2" class="tab">
 <div id="shopify-product-reviews" data-id="{{product.id}}">{{ product.metafields.spr.reviews }}</div>
 </div>
   </div>
 </div>
 </div>
     
 <script>
 $(document).ready(function() {
 $('ul.tabs').each(function(){
 var active, content, links = $(this).find('a');
 active = links.first().addClass('active');
 content = $(active.attr('href'));
 links.not(':first').each(function () {
 $($(this).attr('href')).hide();
 });
 $(this).find('a').click(function(e){
 active.removeClass('active');
 content.hide();
 active = $(this);
 content = $($(this).attr('href'));
 active.addClass('active');
 content.show();
 return false;
 });
 });
 });
 </script>


