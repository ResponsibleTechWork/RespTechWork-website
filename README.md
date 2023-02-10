# About

The website introduces the ResponsibleTech.Work framework and is open to [community contributions](https://ResponsibleTech.Work/contribute/).

# Dev stack

The website was created in [Jekyll](https://jekyllrb.com/), a static website generator, and is hosted on [GitHub](https://github.com/ResponsibleTechWork/RespTechWork-website)

The design is based on the [Libris theme](https://github.com/stackbit-themes/libris-jekyll) by [Stackbit](https://www.stackbit.com/). The theme's SASS files are stored in the `_sass/imports` folder.

## Getting started on macOS

To get a local copy up and running follow these simple steps.

### Prerequisites

  Jeykyll requires Ruby 2.5 or above. Ruby 3 and above does not include webrick; this dependency will be included when you run bundle install (see below).
  ```sh
  brew install ruby
  ```  
  Install jekyll
  ```sh
  gem install jekyll bundler
  ```

### Running the website locally

  Clone the repo
  ```sh
  git clone https://github.com/ResponsibleTechWork/RespTechWork-website.git
  ```
  Make sure all dependencies in your Gemfile are available to your application
  ```sh  
  bundle install
  ```
  Build the site and serve locally with or without live reload
  ```sh
  bundle exec jekyll serve
  bundle exec jekyll serve --livereload
  ```

If you run into any problems, Jekyll documentation has all the information you need to set up your machine, and build and run a Jekyll site: https://jekyllrb.com/docs/.
  
# Content file structure

## The framework

- **The Pledges**: the 7 core pledges of the framework. Source files are stored in the `/responsible-pledges` folder, implemented with the theme's docs layout. Open to suggestions for text improvements.
- **Methodologies**: advice on how to adapt existing methodologies within tech companies.Source files are stored in the `/methodologies` folder, implemented with the theme's docs layout. Open to suggestions for text improvements as well as new methodologies.
- **Tools**: updating existing tools used in different tech roles to encourage day to day action. Source files are stored in the `/_tools` folder, implemented as a Jekyll collection. Open to suggestions for improvements as well as new tools that follow the [requirements](https://ResponsibleTech.Work/about/#tools). To add a new tool, add a new Markdown file with a description and assign one of the existing categories.

## Additional content

- **Resources**: lists of links to additional resources, organized by topic. Source files are stored in the `/resources` folder, implemented with the theme's docs layout. Open to suggestions for text improvements as well as new links. 
- **Blog**: posting news related to the framework and the website. Source files are stored in the `/_posts` folder, implemented as a Jekyll collection. Maintained and updated by the core team.
- **Library**: pages related to the Responsible Tech Library. Source files are stored in the `/library` folder, implemented with a modified theme's docs layout -- look for `_library` files in the `_layouts`. On these pages, the main menu was removed and the footer simplified because these pages were designed to be displayed within the Responsible Tech Library to provide guidance to visitors in the Library.

## Additional pages

Additional static pages (**About**, **Contribute**) are stored in the `/pages` folder.

## Images

When adding images, use the appropriate content folder within the `/assets/img` folder. SVG and WebP are the preferred image file formats to keep the size of the website and its carbon footprint low. Images should only be used when they help people understand the written text better and include descriptive alt text for improved accessibility.

## Settings

General Jekyll settings are stored in the `_config.yml` file, additional variables are defined in the `/_data/_config.json` file. 

# License information

## Libris theme

The modified Libris theme is subject to [Stackbit's License Agreement](https://github.com/stackbit-themes/libris-jekyll/blob/master/LICENSE.md).

## Website content

[![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

The content of the website is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa] unless indicated otherwise.

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-2C82C9.svg