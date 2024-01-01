```php
<?php
/**
 *
 * ooooo   ooooo                                                         
 * `888'   `888'                                                         
 *  888     888  oooo  oooo  ooo. .oo.    .oooooooo oooo d8b oooo    ooo 
 *  888ooooo888  `888  `888  `888P"Y88b  888' `88b  `888""8P  `88.  .8'  
 *  888     888   888   888   888   888  888   888   888       `88..8'   
 *  888     888   888   888   888   888  `88bod8P'   888        `888'    
 * o888o   o888o  `V88V"V8P' o888o o888o `8oooooo.  d888b        .8'     
 *                                       d"     YD           .o..P'      
 *                                       "Y88888P'           `Y8P'   
 * oooooooooooo oooo                              o8o                                   
 *  `888'     `8 `888                              `"'                                   
 *  888          888   .oooo.   ooo. .oo.  .oo.   oooo  ooo. .oo.    .oooooooo  .ooooo.  
 *  888oooo8     888  `P  )88b  `888P"Y88bP"Y88b  `888  `888P"Y88b  888' `88b  d88' `88b 
 *  888    "     888   .oP"888   888   888   888   888   888   888  888   888  888   888 
 *  888          888  d8(  888   888   888   888   888   888   888  `88bod8P'  888   888 
 *  o888o        o888o `Y888""8o o888o o888o o888o o888o o888o o888o `8oooooo.  `Y8bod8P' 
 *                                                                  d"     YD            
 *                                                                 "Y88888P'            
 *
 * HUNGRY FLAMINGO SNIPPET FOR WORDPRESS
 * This file is part of a collection of snippets to be used on your WordPress website.
 * !! Do not put this file in your WordPress installation !!
 *
 * Copy/paste the code below and add it to the functions.php of your child theme.
 * Don't know what a child theme is? Read this post: https://hungryflamingo.com
 *
 * COPY AND PASTE EVERYTHING BELOW THIS LINE TO YOUR FUNCTIONS.PHP */

/**
 * HUNGRY FLAMINGO SNIPPET FOR WORDPRESS
 *
 * @TITLE       Add Custom Image Size in WordPress
 * @VERSION     1.0
 * @DESCRIPTION A collection of commands to add additional custom image sizes in WordPress.
 * @LINK        https://hungryflamingo.com/snippets/add-custom-image-sizes-to-wordpress/
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
function hf_snippet_custom_image_sizes( $sizes ) {
    return array_merge( $sizes, array(
        'your-custom-size' => __( 'Your Custom Size Name' ),
    ) );
}
add_filter( 'image_size_names_choose', 'hf_snippet_custom_image_sizes' );
```