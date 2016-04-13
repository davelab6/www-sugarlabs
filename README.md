# Sugar Labs Website Source Files

This website is made with Jekyll, Bootstrap, some plugins and jQuery.

[Live preview: sugarlabs.github.io/www-sugarlabs](//sugarlabs.github.io/www-sugarlabs)

## How To Contribute

If you wish to contribute to this website, you are very welcome to! Here are a few ways you can do so:

1. Report an issue for someone else to resolve, by clicking the ‘Issues’ button at the top of [this page](http://github.com/sugarlabs/www-sugarlabs), in the main navigation bar.

2. Contribute a change directly, by forking it on GitHub and editing the plain text files, then send a pull request. (If that sounds unfamiliar, learn how with GitHub’s excellent [interactive introduction](https://try.github.io))

3. Discuss general topics on the ["Its An Education Project" email discussion list](https://lists.sugarlabs.org/archive/iaep/) 

## License

The site's contents are licensed under the [Creative Commons Attribution-NonCommercial 4.0 Unported License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

## How This Site Is Made

This site is made with the [Jekyll](http://jekyllrb.com/docs/home/) content management system, and hosted on [GitHub pages](http://pages.github.com).

To learn more about GitHub, check out their [excellent help pages](https://help.github.com).

#### Directory Layout

- `_layouts/*.html`: HTML template files
- `_includes/*.html`: snippets of HTML that are included in pages and templates
- `assets/`: CSS, JS and image files
- `_config.yml`: configuration for Jekyll (generally, ignore this file)
- `press/`: the site’s press relations contents, in US English and Spanish
- `en-US/`: the site’s main contents, in US English
- `en-US/images/precompressed/`: original, pre-compressed content images

#### File Formats

Each page is in Markdown format, with a `.md` file extension. 
If a markdown file starts with the following lines, it will be converted by Jekyll into corresponding `.html` files:

- published: if the page should not be published, set this to `false`
- layout: `default` is the default
- category: the category the page belongs in
- weight: an integer value starts from 1 that effects the ordering of the page in the sidebar and homepage lists
- title: the page title, used in the title tag and h1 of the page

Example:

    ---
    published: true
    layout: default
    category: Workflow
    weight: 3
    title: Page Title
    ---

#### Weight list

Weight lists are used to help contributors determine and document the weight of all pages. Please follow the following rules:

1. Please update the according list if any chapter/page is added or removed.
2. If the new chapter is in between existing chapters, Just add a weight between existing weights.
3. If the new chapter is after any exising chapters, Add the weight number by 3.
4. If no more full numbers can be add between the exising weights, start using decimals.
5. Only edit the weight list for your chapter's language.

Example:

| Weight | Page                                       |
|-------:|:-------------------------------------------|
| 0      | Index                                      |
| 1      | Introduction                               |
| 3      | Contact                                    |


#### How to build the site

For GNU+Linux, ensure that ruby-dev is installed on your system. 
For Ubuntu 14.04:

    sudo apt-get install ruby-dev;

Install Jekyll, with `gem`:

    sudo gem install jekyll;

To see the site as it will appear after processing by Jekyll and review your edits live in a browser layout, run:

    jekyll serve --watch

Now browse [http://localhost:4000/](http://localhost:4000/)

#### How to compress images with Grunt

Put all the raw images inside `en-US/images/precompressed/`

Make sure npm is already installed in your computer, then install all the dependencies with:

    npm install

Once the installations are done, you can go ahead to minify all the images with this Grunt command:

    grunt

Wait for Grunt to notify you, and all the compressed images will be inside `en-US/images/`
