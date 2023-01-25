# ACF-Flexible-Content

# Step 1 
Create a new folder directory 'template_parts/modules/' in current themes Folder (Ex: themes/twentytwentytwo).

# Step 2 

## add in front-page.php
```
<div class="site__middle">
        <div id="content" class="content" role="main" itemscope itemprop="mainContentOfPage" tabindex="-1">
            <?php while ( have_posts() ) : the_post(); ?>
                <?php while ( have_rows( 'home_page' ) ) : the_row(); ?>
                    <?php get_template_part( 'template_parts/modules/' . get_row_layout() ); ?>
                <?php endwhile; ?>
            <?php endwhile; ?>
        </div>
</div>
```
# Step 3

Create Page in 'template_parts/modules/' folder and page name need to be same as layout name(not layout label).
