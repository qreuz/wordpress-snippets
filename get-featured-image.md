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
 * @TITLE       Get Featured Image in WordPress
 * @VERSION     1.0
 * @DESCRIPTION A collection of commands to retrieve the featured image of a post in WordPress.
 * @LINK        https://hungryflamingo.com/snippets/get-featured-image-in-wordpress
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
```