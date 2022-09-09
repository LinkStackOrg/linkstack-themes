## Contribute
### Contribute by making your own custom themes. Read more about this by clicking the link below.



1. [Fork the template repository](#1) -> [github.com/JulianPrieber/llc-default](https://github.com/JulianPrieber/llc-default)
2. [Edit the CSS](#2)
3. [Draft a new release with a version tag](#3)
4. [Open a new pull request or issue on this repository](#4)

<br>

### Theme V2 update:
<details>
    <summary>Read more...</summary>

Theme V2 is the update to the theme system that allows theme-makers to make use of long awaited features.

**These features include:**
- Ability to disable custom styled buttons created by the button editor.
- Ability to open links in the same tab
- Ability to use custom code such as Blade, PHP, HTML, JS and CSS
- Ability to use custom assets and files such as CSS, JS or image files
- Ability to add custom icons
- Ability to make use of other file types for the custom icons instead of being limited to SVGs

</details>


#### File tree:
<pre>
.
└── your-theme/
    ├── animations.css
    ├── brands.css
    ├── config.php
    ├── preview.png
    ├── readme.md
    ├── share.button.css
    ├── skeleton-auto.css
    └── extra/
        ├── custom-body-end.blade.php
        ├── custom-body.blade.php
        └── custom-head.blade.php
			├── custom-assets/
			└── custom-icons/
</pre>

<br>

<a name="1"></a>
## 1. Fork the template repository
Make a fork of this [template repository](https://github.com/JulianPrieber/llc-default). Here you can find the theme files for the default theme.

<br>

<a name="2"></a>
## 2. Edit the Code

**Note:** Before committing your new theme to this theme repository, edit the readme.md to fit your created theme. Make sure to include all additional assets used to create your custom CSS.

Make sure to include a preview image of your theme. This preview image should show both dark and light mode, if applicable. You may add custom text or descriptions to this image, just make it an adequate representation of your theme. Please keep this image in a `16:9` aspect ratio and don't scale it higher than `1920x1080p`. Make sure to use a PNG as the file type.

### 2.1 Edit the CSS

Customize the files to fit your idea.

Default theme uses `prefers-color-scheme` to switch between dark and light mode. You can either keep this format and adjust the colors to your liking, or set one color theme for both modes.

(for CSS only themes this is the only step you'll need.)

<br>

### 2.2 Edit the config

The theme config allows you to configure how LittleLink Custom should treat your theme.
All settings are explained with comments in the config file.

If you edited your buttons in the previous your theme may not be compatible with custom buttons created by the Button Editor.
You can disable the use of custom buttons in the config.

If you want to use custom code like HTML, JavaScript or custom icons in your theme you can enable this here as well.

<br>

### 2.3 Adding custom code

The new theme system allows you to inject custom code at three places on your page: in the head, body and at the end of the body tag.

You can add your custom code with 3 individual files in the "extra" folder with the files:

<pre>
custom-body-end.blade.php
custom-body.blade.php
custom-head.blade.php
</pre>

Here you can write your code in the following languages: Blade, PHP, HTML, JS and CSS.

Further instructions are provided in the individual files as comments.

<br>

### 2.4 Adding custom assets

The theme system gives you the option to add custom assets to your page.

You will have to declare these additions in the file custom-head.blade.php (others work too if required).

Custom assets are stored in the 'custom-assets' directory found inside the 'extra' folder.
Custom assets can be any file you would like to use in your theme.
For example: JS, CSS or image files.

You can load these custom assets with a built-in function, 'themeAsset()'.
Add the file you want to add to your 'custom-assets' folder, and include the name with the file extension in the function.


For this the file and custom code have to be enabled in the config.php

<details>
<pre>

Down below, you can find a few examples using this function:

<link rel="stylesheet" href="{{themeAsset('your.css')}}">
<script src="{{themeAsset('your.js')}}"></script>
<style>body{background-image: url({{themeAsset('your.png')}});}</style>

</pre>
</details>

<br>

### 2.5 Add custom icons

You can download all the icons used for the buttons from [here](https://download-directory.github.io/?url=https%3A%2F%2Fgithub.com%2FJulianPrieber%2Flittlelink-custom%2Ftree%2Fmain%2Flittlelink%2Ficons).

For custom icons to apply you have to enable them in the config first.

Include your edited icons in the "custom-icons" folder while keeping the original file names.

You can use other file types like PNG, JPG, etc. by defining a custom file extension in the config.

<br>

<a name="3"></a>
## 3. Draft a new release with a version tag
Create a new release for your theme in your forked repository. The download URL for that release will later be used to download the font. Create a new tag for your new release. Your first tag should always be v1.0.

**Note:** Please keep the final release file below 2 Megabyte to insure maximum compatibility. For this, it is recommended to compress any images used. This can easily be done online on a site like [tinypng.com](https://tinypng.com/).

<br>

<a name="4"></a>
## 4. Open a new pull request or issue on this repository
Once you followed all these steps, you may [open a pull request or issue](https://github.com/JulianPrieber/llc-themes) on this repository to get included in the official theme list.

<br>

### [For any questions and easier communications, make sure to join our discord community](https://discord.littlelink-custom.com)
