<?php get_header(); ?>
			
			<div id="content" class="clearfix row">
			
				<div id="main" class="col-sm-12 clearfix homegrid" role="main">

					<?php if (have_posts()) : while (have_posts()) : the_post(); ?>
					
                    <div class="col-md-4">
                        <article id="post-<?php the_ID(); ?>" <?php $customclasses = array('clearfix','home-grid'); post_class($customclasses); ?> role="article"  >

                            <a href="<?php the_permalink() ?>" class="featured-post" style="background-image:url(<?php if( has_post_thumbnail($post_array->ID) ) {$image_arr = wp_get_attachment_image_src(get_post_thumbnail_id($post_array->ID), 'medium');echo $image_url = $image_arr[0]; }?>);"></a>
                            
                            <header>

                             <h1 class="h2"><a href="<?php the_permalink() ?>" rel="bookmark" title="<?php the_title_attribute(); ?>"><?php the_title(); ?></a></h1>

                            </header>


                            <footer>

                                <p class="meta"><?php _e("Posted", "wpbootstrap"); ?> <time datetime="<?php echo the_time('Y-m-j'); ?>" pubdate><?php echo get_the_date('F jS, Y', '','', FALSE); ?></time> <?php _e("by", "wpbootstrap"); ?> <?php the_author_posts_link(); ?> <span class="amp">&</span> <?php _e("filed under", "wpbootstrap"); ?> <?php the_category(', '); ?>.</p>
                            </footer>

                        </article>
                    </div>
					
					<?php endwhile; ?>	
					
					<?php if (function_exists('wp_bootstrap_page_navi')) { // if expirimental feature is active ?>
						
						<?php wp_bootstrap_page_navi(); // use the page navi function ?>
						
					<?php } else { // if it is disabled, display regular wp prev & next links ?>
						<nav class="wp-prev-next">
							<ul class="pager">
								<li class="previous"><?php next_posts_link(_e('&laquo; Older Entries', "wpbootstrap")) ?></li>
								<li class="next"><?php previous_posts_link(_e('Newer Entries &raquo;', "wpbootstrap")) ?></li>
							</ul>
						</nav>
					<?php } ?>		
					
					<?php else : ?>
					
					<article id="post-not-found">
					    <header>
					    	<h1><?php _e("Not Found", "wpbootstrap"); ?></h1>
					    </header>
					    <section class="post_content">
					    	<p><?php _e("Sorry, but the requested resource was not found on this site.", "wpbootstrap"); ?></p>
					    </section>
					    <footer>
					    </footer>
					</article>
					
					<?php endif; ?>
			
				</div> <!-- end #main -->
    
				<?php get_sidebar(); // sidebar 1 ?>
    
			</div> <!-- end #content -->

<?php get_footer(); ?>