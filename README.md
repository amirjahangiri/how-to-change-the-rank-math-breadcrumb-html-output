# how-to-change-the-rank-math-breadcrumb-html-output
how to change the rank math breadcrumb html output

<pre>
// Write By Amirj.
// www.example.com/wp-content/theme/Theme-name/functions.php
// Open Functions.php in root template 

add_filter( 'rank_math/frontend/breadcrumb/html', function( $html, $crumbs, $class ) {
    $html = str_replace('<span class="last">'.get_the_title().'</span>', '<a href="'.get_the_permalink().'">'.get_the_title().'</a>', $html);
    return $html;
}, 10, 3);

</pre>
