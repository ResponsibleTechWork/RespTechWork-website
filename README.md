# About

The website introduces the ResponsibleTech.Work framework and is open to [community contributions](https://ResponsibleTech.Work/contribute/).

# Dev stack

The website was created in [Jekyll](https://jekyllrb.com/), a static website generator, and is hosted on [GitHub](https://github.com/ResponsibleTechWork/RespTechWork-website)

The design is based on the [Libris theme](https://github.com/stackbit-themes/libris-jekyll) by [Stackbit](https://www.stackbit.com/). The theme's SASS files are stored in the `_sass/imports` folder.

## Getting started

To get a local copy up and running follow these simple steps.

### Prerequisites

  Install or update ruby
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
  For Ruby 3.0.0 and above, add a dependency to webrick
  ```sh
  bundle add webrick
  ```
  Build the site and serve locally with or without live reload
  ```sh
  bundle exec jekyll serve
  bundle exec jekyll serve --livereload
  ```

If you run into any problems, Jekyll documentation has all the information you need to set up your machine, and build and run a Jekyll site: https://jekyllrb.com/docs/.

## Contributing

Please follow these steps to make changes to the website. There is a detailed example below.

1. Select a Trello ticket assigned to you, and move it from **TODO** to **Doing**.
2. Check you are in the main branch and make a git pull to get the latest project changes from the remote server.
3. Create a new branch and make your changes. This will typically be for new content.
4. Check your changes locally.
5. When you've finished, commit changes to your branch.
6. Create a pull request from your branch to main, adding clear comments and assigning it to a reviewer where possible.
7. Once the ticket has been moved to **Done**, delete the local and remote versions of your branch.

## Adding new content example

### Making changes in a new local branch

  Branch naming convention
  `<typeOfChange>_<short-title>`
  e.g. feature_tag-generator

  In this example, the name is content_new-blog-post

  Create and checkout a new branch locally
  ```sh
  git checkout -b content_new-blog-post
  ```

  Check you are on the new branch.

  ```sh
  git branch
  ```

  Edit files and add content to the local branch. Commit your changes, and push them to the remote server.

  ```sh 
  git add .
  git commit -m 'content_new-blog-post added'
  git push --set-upstream origin content_new-blog-post
  ```

  #### Creating a pull request

  The pull request can be made on GitHub. To create a pull request from the command line use the CLI tool - https://github.com/cli/cli.
  
  The CLI tool requires you to set up authentication.

  ```sh
  brew install gh
  gh auth login
  ```

  You are now ready to create a pull request from the command line. There are currently 3 possible reviewers: ialja, rewildchris, and danhartley.

  ```sh
  gh pr create --title "New content_new-blog-post" --body "Content ready to review" --reviewer ialja
  ```

  For additional commands and flags see: https://cli.github.com/manual/gh_issue_create

  Once a pull request has been created, it can be linked to its Trello ticket.

  #### Updating the Trello ticket

  Under POWER-UPS in the Trello ticket click GitHub and follow the instructions to 'Attach Pull Request'.

  Move the Trello ticket you want reviewed from **Doing** to **In Review**.

  #### Reviewing a pull request

  If you accept a pull request, and the branch has been successfully merged with main, move the relevant Trello ticket from **In Review** to **Done**.

  #### Tidying up

  Once a pull request has been accepted its branch should be deleted, either by the reviewer on GitHub or by the developer locally:
  First checkout the master branch, pull to check the branch has been merged, then delete the branch both locally and, if necessary, remotely. Use git branch to verify the branch has been deleted locally.

  ```sh
  git checkout master
  git pull
  git branch -d content_new-blog-post
  git push origin --delete content_new-blog-post
  git branch
  ```
  
# Content file structure

## The framework

- **The Pledges**: the 7 core pledges of the framework. Source files are stored in the `/responsible-pledges` folder, implemented with the theme's docs layout. Open to suggestions for text improvements.
- **Methodologies**: advice on how to adapt existing methodologies within tech companies.Source files are stored in the `/methodologies` folder, implemented with the theme's docs layout. Open to suggestions for text improvements as well as new methodologies.
- **Tools**: updating existing tools used in different tech roles to encourage day to day action. Source files are stored in the `/_tools` folder, implemented as a Jekyll collection. Open to suggestions for improvements as well as new tools that follow the [requirements](https://ResponsibleTech.Work/about/#tools). To add a new tool, add a new Markdown file with a description and assign one of the existing categories.

## Additional content

- **Resources**: lists of links to additional resources, organized by topic. Source files are stored in the `/resources` folder, implemented with the theme's docs layout. Open to suggestions for text improvements as well as new links. 
- **Blog**: posting news related to the framework and the website. Source files are stored in the `/_posts` folder, implemented as a Jekyll collection. Maintained and updated by the core team.

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