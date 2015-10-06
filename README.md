# categoria_wordpress
<ul class="category_list">   
  <?php
     $args = array('child_of'=>4,'hide_empty'=>0);
     $my_categories = get_categories($args);
  ?>
  <?php foreach( $my_categories as $category ):?>
    <li><a href="<?php echo get_category_link($category->term_id);?>"><?php echo $category->name;?></a></li>
  <?php endforeach; ?>
</ul>
