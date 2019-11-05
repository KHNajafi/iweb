# iWeb
Test environment for personal website/portfolio development

### Versions
The current version of the site is v2, with updates to `hugo` (version 0.57.2) and the theme `academic-hugo` (version from `2019-08-19`).  v1 has been removed with all content migrated to v2 as of `2019-08-27`.

## Site Layout and Config

For the `hugo-academic` theme, the modifications for the site are as follows:

* Menus
    * adjusting site menu to my organization in `config/_default/menus.toml`
        * deactivate unused widgets
        * rename `projects` to `feathers` (uses the same layout); create/specify new folder with the same name for path (path created in `./content/`)
* Appearance (colours, type, etc)
    * these are modified in `/config/_default/params.toml`
        * colour theme: `ocean`
        * font: `classic`
* Home
    * this is the appearance and content (order, headings, descriptions, etc) of the home page, and also configuration of all active widgets (display style, colours, filter settings, etc); on the respective `*.md` files in `content/home/` (ie, `content/home/contact.md` configures where on the homepage the contact widget will appear, the contact form settings, and heading/subheading)
* _Feathers_ 
    * these are based on the `project` widget; the configuration and layout is set in `/content/home/feathers.md`
        * edit heading (`title`) and subheading (`subtitle`)
    * they pull content from `/feathers` via `page_type = "feathers"` configuration
    * each post is within it's own subdirectory with the format:
        * create subdirectory for post with the format `content/post/#POST_SLUG#/`
        * `featured.jpg` for the image
        * `index.Rmd` for the content and all YAML (including the post's title, and image width)
