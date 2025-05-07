# Emmet Snippets Documentation

This document organizes a collection of Emmet snippets for use in WordPress, Elementor, JavaScript, jQuery, and PHP development. Snippets are categorized by their primary use case, with Elementor snippets prefixed with 'E', WordPress snippets with 'W', JavaScript/jQuery with 'J', and PHP with 'P'. Each snippet includes a prefix, description, and usage details to streamline development workflows.

## Elementor Snippets (E)

Elementor snippets are designed for creating and styling widgets in Elementor, including controls (e.g., text, color, repeater), sections, and responsive settings. These snippets start with the prefix 'E'.

| Prefix                 | Description                              | Usage                                                                 |
|------------------------|------------------------------------------|----------------------------------------------------------------------|
| econtentstart         | Starts a content section in Elementor widget | Initialize a content section for adding controls like text or media.  |
| estylecontent         | Starts a style section in Elementor widget | Initialize a style section for adding styling controls like color or typography. |
| etext                 | Adds a text control for titles           | Use to add a title field in a widget, editable in the Elementor panel. |
| etextsubtitle         | Adds a text control for subtitles        | Use for subtitle fields in widgets, supports translation.            |
| etextsubheading       | Adds a text control for subheadings      | Use for subheading fields in widgets, supports full-width input.     |
| etextheading          | Adds a text control for headings         | Use for heading fields in widgets, ideal for section titles.         |
| etextheadingtitle     | Adds a textarea for heading titles       | Use for longer heading titles, supports multi-line input.           |
| etextbutton           | Adds button text and link controls       | Use to add customizable buttons with text and URL in widgets.        |
| enumber               | Adds a number control with min/max/step  | Use for numeric inputs like price or quantity in widgets.            |
| etextarea             | Adds a textarea control for descriptions | Use for multi-line text inputs like descriptions or notes.          |
| ewisi                 | Adds a WYSIWYG editor control            | Use for rich text editing in widgets, supports HTML formatting.      |
| eselect               | Adds a dropdown select control           | Use for style or option selection in widgets (e.g., style_one, style_two). |
| ecolor                | Adds a color picker control              | Use to style elements like text or backgrounds with color selection. |
| efontfamily           | Adds a font family control               | Use to customize font families for text elements in widgets.         |
| etime                 | Adds a date-time picker control          | Use for date or time inputs in widgets, like event scheduling.       |
| erepeater             | Adds a repeater control for lists        | Use for dynamic lists of items (e.g., testimonials, services) in widgets. |
| etabs                 | Adds tabs for normal/hover states        | Use to organize styling controls for different states (normal, hover). |
| eslider               | Adds a slider control for sizes          | Use for responsive size controls (e.g., icon size, width) in widgets. |
| emargin               | Adds margin control with dimensions      | Use to adjust spacing around elements in widgets.                   |
| epadding              | Adds padding control with dimensions     | Use to adjust internal spacing of elements in widgets.              |
| elink                 | Adds a URL control for links             | Use for adding clickable links in widgets, supports external/nofollow. |
| eimage                | Adds an image upload control             | Use for adding images to widgets, integrates with media library.    |
| eicon%image           | Adds an icon picker control              | Use for selecting icons (e.g., Font Awesome) in widgets.            |
| eboxshadow            | Adds a box shadow control                | Use to apply shadow effects to elements in widgets.                 |
| etypography           | Adds typography control                  | Use to customize font size, weight, and style for text elements.    |
| eborder               | Adds a border color control              | Use to style borders of elements in widgets.                        |
| eopacity              | Adds an opacity slider control           | Use to adjust transparency of elements in widgets.                  |
| ebackground           | Adds background control (classic/gradient/video) | Use to style backgrounds of elements in widgets.                  |
| econdition            | Adds a condition for control visibility  | Use to show/hide controls based on other settings (e.g., style).    |
| ecsstext              | Adds a custom CSS textarea control       | Use to allow custom CSS input for styling widget elements.          |
| ethree                | Adds typography, color, and margin controls | Use for styling text elements with typography, color, and spacing. |
| esvgicontogetherstyle | Adds SVG/icon color and size controls    | Use for styling SVG or icon elements in widgets.                    |
| eattr                 | Outputs escaped attribute for translation | Use to safely output translatable attributes in widget templates.   |
| ehr                   | Adds a divider control                   | Use to visually separate controls in the Elementor panel.           |
| eheading              | Adds a heading control for sections      | Use to label sections or groups of controls in the Elementor panel. |
| ealignment            | Adds text alignment control              | Use to align text or elements (left, center, right, justify) in widgets. |
| ebradius              | Adds border radius control               | Use to round corners of elements in widgets.                        |
| econditions           | Adds multiple conditions for visibility   | Use to control visibility of controls based on multiple settings.   |
| efour                 | Adds typography, color, margin, padding  | Use for comprehensive text styling in widgets.                      |
| esettings             | Outputs escaped settings value           | Use to safely display widget settings in templates.                 |
| eswitch               | Adds a switcher control (show/hide)      | Use for toggleable options in widgets (e.g., show navigation).      |
| wpkses                | Outputs settings with wp_kses sanitization | Use to safely output HTML content from settings in widget templates. |
| eeschtml              | Outputs escaped HTML settings value      | Use to safely display settings as HTML in widget templates.         |
| eicondirect           | Renders an icon from settings            | Use to display selected icons in widget templates.                  |
| eimagethree           | Adds image height, width, border radius  | Use to style images with responsive dimensions and rounded corners. |
| enav                  | Adds navigation color and hover styles   | Use for styling navigation arrows in sliders or carousels.          |
| etwo                  | Adds typography and color controls       | Use for basic text styling in widgets.                              |
| essubtitle            | Styles subtitle with typography, color, spacing | Use to style subtitle elements in widgets.                     |
| estitle               | Styles title with typography, color, spacing | Use to style title elements in widgets.                         |
| esdescription         | Styles description with typography, color, spacing | Use to style description text in widgets.                  |
| essubheading          | Styles subheading with typography, color, spacing | Use to style subheading elements in widgets.                |
| esheading             | Styles heading with typography, color, spacing | Use to style heading elements in widgets.                    |
| esheadingtitle        | Styles heading title with typography, color, spacing | Use to style heading title elements in widgets.         |
| esname                | Styles name with typography, color, spacing | Use to style name fields in widgets (e.g., team member names).   |
| esplace               | Styles place with typography, color, spacing | Use to style location or place fields in widgets.              |
| esdesignation         | Styles designation with typography, color, spacing | Use to style job titles or roles in widgets.             |
| esdate                | Styles date with typography, color, spacing | Use to style date fields in widgets (e.g., event dates).         |
| escard                | Styles card with background and padding  | Use to style card containers in widgets.                           |
| eshow                 | Conditionally displays settings value    | Use to conditionally output settings in widget templates.           |

### Example: Elementor Text Control
```php
$this->add_control(
    'title',
    [
        'label' => esc_html__( 'Title', 'plugin-name' ),
        'type' => \Elementor\Controls_Manager::TEXT,
        'default' => esc_html__( 'Default title', 'plugin-name' ),
        'label_block' => true,
    ]
);
```
**Usage**: Adds a text input field for a widget title, displayed as a full-width block in the Elementor panel.

## WordPress Snippets (W)

WordPress snippets are designed for WordPress-specific functionality, such as post loops, theme functions, and ACF integration. These snippets start with 'W' or relate to WordPress plugins like ACF.

| Prefix                     | Description                                | Usage                                                                 |
|----------------------------|--------------------------------------------|----------------------------------------------------------------------|
| wp_title_function         | Outputs post/page title                    | Use in templates to display the title of the current post or page.   |
| wp_content_function       | Outputs post/page content                  | Use in templates to display the content of the current post or page. |
| wp_post_thumbnail_function | Outputs featured image URL                 | Use to display the URL of a post’s featured image in templates.      |
| wp_post_if_function       | Standard WordPress loop                    | Use for iterating through posts in templates with a full loop structure. |
| wp_ewwpost_if_function    | Simplified WordPress loop                  | Use for a concise post loop in templates.                           |
| wp_ewwsspost_if_function  | Duplicate simplified loop (same as above)  | Same as `wp_ewwpost_if_function` (consider merging or removing).    |
| wp_ewwsspssost_if_function | Basic WordPress conditional check          | Use for simple post existence checks in templates.                  |
| location                  | Outputs theme directory URI                | Use to reference theme assets (e.g., images, CSS) in templates.     |
| acf_if                    | Conditional ACF field output               | Use to display ACF field values conditionally in templates.         |
| acf_foreach               | Loops through ACF repeater field           | Use to iterate through ACF repeater fields in templates.            |
| pluginhead                | Plugin header comment                     | Use as the header for custom WordPress plugins.                    |
| pactivedeactive           | Plugin activation/deactivation hooks       | Use to define actions on plugin activation/deactivation.            |

### Example: WordPress Loop
```php
<?php if ( have_posts() ) : ?>
    <?php while ( have_posts() ) : the_post(); ?>
        <!-- do stuff ... -->
    <?php endwhile; ?>
<?php endif; ?>
```
**Usage**: Implements the standard WordPress loop to display post content in templates.

## JavaScript/jQuery Snippets (J)

JavaScript and jQuery snippets are designed for DOM manipulation, event handling, and animations. These snippets start with 'J' for jQuery or describe JavaScript functionality.

| Prefix                 | Description                                | Usage                                                                 |
|------------------------|--------------------------------------------|----------------------------------------------------------------------|
| documentstyle         | Changes element style (color)              | Use to dynamically change an element’s CSS color via JavaScript.     |
| documentid            | Sets element innerHTML                     | Use to update the content of an element by ID.                      |
| documentclass         | Sets innerHTML for first element by class  | Use to update content of the first element with a specific class.   |
| documentsrc           | Changes image source                       | Use to dynamically update an image’s `src` attribute.               |
| dc                    | Writes content to document                 | Use for direct document output (less common, use with caution).     |
| documentquery         | Sets style via querySelector               | Use to apply styles to elements selected by CSS selectors.          |
| eventlistener         | Adds a click event listener                | Use to attach click events to elements with a callback function.    |
| log                   | Logs to console                            | Use for debugging by logging values to the browser console.         |
| jqready               | jQuery document ready event                | Use to run code when the DOM is fully loaded with jQuery.           |
| jqclick               | jQuery click event handler                 | Use to attach click events to elements with jQuery.                 |
| jqslideup             | jQuery slideUp animation                   | Use to animate an element sliding up (hiding it).                   |
| jqslidedown           | jQuery slideDown animation                 | Use to animate an element sliding down (showing it).                |
| jqslidetoggle         | jQuery slideToggle animation               | Use to toggle an element’s visibility with a slide animation.       |
| jqanimatetoggle       | jQuery animate height toggle               | Use to animate an element’s height for show/hide effects.           |
| jqcss                 | Applies CSS styles with jQuery             | Use to dynamically style elements with multiple CSS properties.     |
| jqcssadd              | Adds CSS classes with jQuery               | Use to add classes to elements for styling or behavior.             |
| jqremovecss           | Removes CSS classes with jQuery            | Use to remove classes from elements.                               |
| jqtogglecss           | Toggles CSS classes with jQuery            | Use to toggle classes on elements for dynamic styling.              |
| jqappend              | Appends content with jQuery                | Use to add content to the end of an element.                       |
| jqprepand             | Prepends content with jQuery               | Use to add content to the start of an element.                     |
| jqremove              | Removes elements with jQuery               | Use to remove elements matching a selector.                        |
| jqanimate             | Custom jQuery animation                    | Use for custom animations (e.g., position, opacity, size).         |
| terneryjs             | JavaScript ternary operator                | Use for concise conditional assignments.                           |
| switchjs              | JavaScript switch statement                | Use for multi-case conditional logic.                              |
| breakifjs             | JavaScript loop with break                 | Use to exit a loop based on a condition.                           |
| arrowjs               | JavaScript arrow function                  | Use for concise function definitions.                              |
| setjs                 | JavaScript Set object                      | Use to manage unique values and iterate through them.               |
| mapjs                 | JavaScript Map object                      | Use for key-value pair storage and retrieval.                      |

### Example: jQuery Click Event
```javascript
$("#loginButton").click(function(){
    
});
```
**Usage**: Attaches a click event handler to an element with ID `loginButton` using jQuery.

## PHP Snippets (P)

PHP snippets cover general PHP functionality, including arrays, loops, string manipulation, and WordPress-specific PHP utilities. These snippets start with 'P' or describe PHP functionality.

| Prefix                       | Description                                | Usage                                                                 |
|------------------------------|--------------------------------------------|----------------------------------------------------------------------|
| foreach                     | PHP foreach loop                           | Use to iterate through arrays or objects.                           |
| associativearray            | PHP associative array                      | Use to define key-value pair arrays.                               |
| multidimentionalarray       | PHP multidimensional array                 | Use for nested arrays (e.g., data tables).                          |
| strpositioncheck            | Checks string position                     | Use to find the position of a substring in a string.               |
| strreplace                  | Replaces string content                    | Use to replace occurrences of a substring in a string.             |
| array                       | Defines a simple PHP array                 | Use for basic indexed arrays.                                      |
| minvalue                    | Finds minimum value                        | Use to get the smallest value from a set of numbers.               |
| maxvalue                    | Finds maximum value                        | Use to get the largest value from a set of numbers.                |
| e                           | PHP echo statement                         | Use to output content (incomplete, consider expanding).            |
| abs                         | PHP absolute value                         | Use to get the absolute value of a number.                         |
| root                        | PHP square root                            | Use to calculate the square root of a number.                      |
| round                       | PHP round number                           | Use to round a floating-point number.                              |
| randomfunc                  | PHP random number                          | Use to generate a random number.                                   |
| definearray                 | Defines a constant array                   | Use to create a constant array with predefined values.             |
| ifphp                       | PHP if condition                           | Use for conditional logic in PHP scripts.                          |
| elsephp                     | PHP else condition                         | Use to define alternative logic in conditionals.                   |
| elseifphp                   | PHP elseif condition                       | Use for additional conditional checks.                             |
| switchphp                   | PHP switch statement                       | Use for multi-case conditional logic in PHP.                       |
| whilephp                    | PHP while loop                             | Use for looping while a condition is true.                         |
| dowhilephp                  | PHP do-while loop                          | Use for looping at least once before checking a condition.         |
| forphp                      | PHP for loop                               | Use for iterating a specific number of times.                      |
| sortfullfunction            | Sorts array and iterates                   | Use to sort and display array elements.                            |
| rsortfullfunction           | Reverse sorts array and iterates           | Use to sort array in descending order and display.                 |
| asort                       | Sorts associative array by value           | Use to sort key-value pairs by value.                              |
| ksortfull                   | Sorts associative array by key             | Use to sort key-value pairs by key.                                |
| array_change_key_case_function | Changes array key case                   | Use to convert array keys to upper or lower case.                  |
| ternaryphp                  | PHP ternary operator                       | Use for concise conditional assignments in PHP.                    |
| nullcoalescingPHP           | PHP null coalescing operator               | Use to provide default values for undefined variables.             |
| restparameterPHP            | PHP rest parameter function                | Use to handle variable number of function arguments.               |
| strtoarrayPHP               | Converts string to array                   | Use to split a string into an array by delimiter.                  |
| arraytostringPHP            | Converts array to string                   | Use to join array elements into a string.                          |
| inarrayPHP                  | Checks if value exists in array            | Use to verify presence of a value in an array.                     |
| arraysearchPHP              | Searches array for value                   | Use to find the key of a value in an array.                        |
| keyexistsPHP                | Checks if key exists in array              | Use to verify presence of a key in an array.                       |
| arraywalkPHP                | Applies callback to array elements         | Use to process each array element with a custom function.           |
| arrayreducePHP              | Reduces array to single value              | Use to combine array elements into a single value (e.g., sum).     |
| arraylistPHP                | Assigns array values to variables          | Use to extract array elements into individual variables.           |
| arrayrangePHP               | Creates array with range of values         | Use to generate an array of sequential numbers.                    |
| arraypushPHP                | Adds elements to array end                 | Use to append elements to an array.                                |
| arrayshifthPHP              | Removes and returns first array element    | Use to shift the first element off an array.                       |
| arrayslicehPHP              | Extracts a portion of an array             | Use to get a subset of an array.                                   |
| arrayunshiftPHP             | Adds elements to array start               | Use to prepend elements to an array.                               |
| arraysplicePHP              | Replaces array portion with new elements   | Use to modify an array by replacing a section.                     |
| arraymapPHP                 | Applies callback to array elements         | Use to transform array elements with a function.                   |
| arrayfilterPHP              | Filters array elements                     | Use to filter array elements based on a condition.                 |
| arrayintersectPHP           | Finds common elements in arrays            | Use to get intersecting elements of multiple arrays.               |
| arraydifftPHP               | Finds differing elements in arrays         | Use to get elements unique to one array compared to another.       |
| arraypopPHP                 | Removes and returns last array element     | Use to pop the last element off an array.                          |
| arrayrandomPHP              | Selects random array elements              | Use to pick random elements from an array.                         |
| arrayshufflePHP             | Shuffles array elements                    | Use to randomize the order of array elements.                      |
| arraysortPHP                | Sorts array with multisort                 | Use to sort multiple arrays or multidimensional arrays.            |
| arraysumPHP                 | Sums array elements                        | Use to calculate the sum of numeric array elements.                |
| arraycompactPHP             | Creates array from variables               | Use to create an array from variable names and values.             |
| arraycurrentPHP             | Gets current array element                 | Use to access the first or current element of an array.            |
| strsubstrPHP                | Extracts substring                         | Use to get a portion of a string.                                  |
| strexplode                  | Splits string into array                   | Use to split a string by a delimiter with optional limits.         |
| strjoin                     | Joins array into string                    | Use to combine array elements into a string (alias for implode).   |
| strimplode                  | Joins array into string                    | Use to combine array elements into a string with a delimiter.      |
| strsplit                    | Splits string into array of characters     | Use to convert a string into an array of individual characters.    |
| strwordcount                | Counts words in string                     | Use to count the number of words in a string.                      |
| strtok                      | Tokenizes string                           | Use to split a string into tokens based on a delimiter.            |
| strpos                      | Finds last position of substring           | Use to find the last occurrence of a substring in a string.        |
| headerPHP                   | Sets HTTP header for redirection           | Use to redirect to another URL in PHP.                             |
| moveuploadedfilePHP         | Moves uploaded file                        | Use to handle file uploads by moving files to a destination.       |
| setcookiesPHP               | Sets a cookie                              | Use to create a browser cookie with expiration and path.           |
| br                          | Outputs newline in PHP                     | Use to add a line break in output (e.g., for CLI or plain text).   |
| define                      | Defines a constant                        | Use to create a constant value in PHP.                             |
| func                        | Defines a JavaScript function              | Use to create a named function (misplaced in PHP category).        |

### Example: PHP Foreach Loop
```php
foreach ($variable as $key => $value) {
    
}
```
**Usage**: Iterates through an array or object, accessing keys and values for processing.

## Miscellaneous Snippets

| Prefix          | Description                                | Usage                                                                 |
|-----------------|--------------------------------------------|----------------------------------------------------------------------|
| iteration-foreach | JavaScript forEach loop                   | Use to iterate through arrays in JavaScript.                        |
| comment         | Multi-line comment block                  | Use to add documentation or comments in PHP/JavaScript code.        |
| elseifdirectphp | WordPress elseif for ACF field            | Use in templates to check ACF fields conditionally.                 |
| elsedirectphp   | WordPress else statement                  | Use in templates for alternative logic in conditionals.             |
| foreachdirect   | WordPress foreach for settings            | Use to loop through Elementor settings arrays in templates.         |
| foreachsimple   | Simple PHP foreach loop                   | Use for basic array iteration in WordPress templates.               |
| labelblock      | Elementor label_block setting             | Use to make text controls full-width in Elementor widgets.          |
| ee              | Outputs esc_html function                 | Use to escape HTML output in WordPress templates.                   |
| emptyphp        | Conditional check for empty settings      | Use to conditionally display content if settings are not empty.     |
| translate       | Outputs translatable text                 | Use to output translatable strings in WordPress templates.          |
| isset           | Checks if theme option is set             | Use to conditionally display content based on theme options.        |
| ddd             | Placeholder/invalid snippet               | Likely a typo or test; consider removing or clarifying purpose.     |

### Notes
- **Duplicates**: The snippet `wp_ewwsspost_if_function` is identical to `wp_ewwpost_if_function`. Consider removing or renaming to avoid redundancy.
- **Misplaced Snippets**: The `func` snippet (JavaScript function) is categorized under PHP. It should be moved to JavaScript or clarified.
- **Incomplete Snippets**: The `ddd` snippet appears to be a placeholder or error. It should be clarified or removed.
- **Scope**: Many snippets lack a `scope` field. Adding scopes (e.g., `php`, `javascript`) would improve compatibility with editors like VS Code.

This documentation provides a comprehensive reference for using these snippets in development, with a focus on Elementor widget creation and WordPress/PHP/JavaScript utilities.