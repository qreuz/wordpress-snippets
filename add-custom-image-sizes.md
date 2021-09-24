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
 * @TITLE       Add Custom Image Size in WordPress
 * @VERSION     1.0
 * @DESCRIPTION A collection of commands to add additional custom image sizes in WordPress.
 * @LINK        https://qreuz.com/snippets/get-featured-image-in-wordpress
 * @AUTHOR      Qreuz GmbH <hello@qreuz.com>
 * @LICENSE     GNU GPL v3 https://www.gnu.org/licenses/gpl-3.0
 */

// Add a custom image size.
// https://developer.wordpress.org/reference/functions/add_image_size/
add_image_size( string $name, int $width, int $height, bool|array $crop = false);

// Retrieve the post thumbnail in the custom image size.
the_post_thumbnail( 'your-custom-size' );

// Retrieve an image in the custom image size. Replace 23 with the ID of your image.
wp_get_attachment_image( 23, 'your-custom-size' );

// Make the custom image size available from the WordPress backend.
/**
 * This function makes custom image sizes available from the WordPress backend.
 * You can add custom image sizes here to have them listed, e.g. for authors to select from.
 **/ 
function qreuz_snippet_custom_image_sizes( $sizes ) {
    return array_merge( $sizes, array(
        'your-custom-size' => __( 'Your Custom Size Name' ),
    ) );
}
add_filter( 'image_size_names_choose', 'qreuz_snippet_custom_image_sizes' );