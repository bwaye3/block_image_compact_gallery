# *Add to the subtheme.libraries.yml*

#Image Compact Gallery <br />
image-compact-gallery: <br />
version: "1.0.x" <br />
css: <br />
theme: <br />
//cdnjs.cloudflare.com/ajax/libs/baguettebox.js/1.10.0/baguetteBox.min.css: {  type: external, minified: true } <br />
templates/block/custom/image-compact-gallery/css/compact-gallery.css: { } <br />
js:
//cdnjs.cloudflare.com/ajax/libs/baguettebox.js/1.11.1/baguetteBox.min.js: {type: external, minified: true,  scope: header } <br />
templates/block/custom/image_compact_gallery/js/compact-gallery.js: {}
dependencies: <br />
- core/jquery <br />

# *Add to the repositories section in the subtheme composer.json*

"repositories": [ <br />
{ <br />
"type": "vcs", <br />
"url": "https://github.gatech.edu/ICWebTeam/block_image_compact_gallery.git" <br />
}
# *Add to the requirement in the subtheme composer.json*

"require": { <br />
"drupal/paragraphs": "^1.12",<br />
"gt/image_compact_gallery": "dev-master", <br />
"mnsami/composer-custom-directory-installer": "^2.0"
},

# *Add to the installer paths in the subtheme composer.json*
"installer-paths": { <br />
"web/themes/contrib/subtheme/templates/block/custom/image_compact_gallery": [ <br />
"gt/image_compact_gallery" <br />
] <br />

# *Implements hook_page_attachments_alter(). in subtheme.theme*
function SUBTHEME_page_attachments_alter(&$page) {<br />
$page['#attached']['library'][] = 'SUBTHEME/image_compact_gallery';<br />
}
},

# *Install the Paragraphs Module*
composer require drupal/paragraphs


# **CUSTOM BLOCK  SET-UP**
![](images/set-up.png)

