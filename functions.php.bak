<?php

function get_images_from_media_library() {
    $args = array(
        'post_type' => 'attachment',
        'post_mime_type' =>'image',
        'post_status' => 'inherit',
        'posts_per_page' => 1,
        'orderby' => 'rand'
    );
    $query_images = new WP_Query( $args );
    $images = array();
    foreach ( $query_images->posts as $image) {
        $images[]= $image->guid;
    }
    return $images;
}

function display_images_from_media_library() {

    $imgs = get_images_from_media_library();
    $html = '';

    foreach($imgs as $img) {

        $html .= '' . $img . '';

    }

    $html .= '';

    return $html;

}

function my_theme_add_editor_styles() {
    $font_url = str_replace( ',', '%2C', '//fonts.googleapis.com/css?family=Roboto+Slab:400,700|Fjalla+One' );
    add_editor_style( $font_url );
    add_editor_style( 'editor-style.css' );
}
add_action( 'after_setup_theme', 'my_theme_add_editor_styles' );
add_action( 'admin_init', 'my_theme_add_editor_styles' );

?>