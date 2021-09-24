```php
<?php
/**
 *
 *  ██████╗ ██████╗ ███████╗██╗   ██╗███████╗
 * ██╔═══██╗██╔══██╗██╔════╝██║   ██║╚══███╔╝
 * ██║   ██║██████╔╝█████╗  ██║   ██║  ███╔╝
 * ██║▄▄ ██║██╔══██╗██╔══╝  ██║   ██║ ███╔╝
 * ╚██████╔╝██║  ██║███████╗╚██████╔╝███████╗
 *  ╚══▀▀═╝ ╚═╝  ╚═╝╚══════╝ ╚═════╝ ╚══════╝
 *
 * QREUZ SNIPPET FOR WORDPRESS
 * This file is part of a collection of snippets to be used on your WordPress website.
 * !! Do not put this file in your WordPress installation !!
 *
 * Copy/paste the code below and add it to the functions.php of your child theme.
 * Don't know what a child theme is? Read this post: https://qreuz.com/
 *
 * COPY AND PASTE EVERYTHING BELOW THIS LINE TO YOUR FUNCTIONS.PHP */

/**
 * QREUZ SNIPPET FOR WORDPRESS
 *
 * @TITLE       Get Featured Image in WordPress
 * @VERSION     1.0
 * @DESCRIPTION A collection of commands to retrieve the featured image of a post in WordPress.
 * @LINK        https://qreuz.com/snippets/get-featured-image-in-wordpress
 * @AUTHOR      Qreuz GmbH <hello@qreuz.com>
 * @LICENSE     GNU GPL v3 https://www.gnu.org/licenses/gpl-3.0
 */

// Return the featured image as an <img> tag.
// https://developer.wordpress.org/reference/functions/get_the_post_thumbnail/
get_the_post_thumbnail();

// Return the featured image with specified size 'large' as an <img> tag.
get_the_post_thumbnail( get_the_ID(), 'large' );

// Return the image URL.
// https://developer.wordpress.org/reference/functions/get_the_post_thumbnail_url/
get_the_post_thumbnail_url();

// Return the featured image URL with specified size 'large'.
get_the_post_thumbnail_url( get_the_ID(), 'large' );