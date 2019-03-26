# [LASA 2019](https://lasa2019.com)

## About
Developed by [Griffin Davis](https://griffindvs.com) and [Cameron Kleiman](https://camk.co) for the [LASA](http://lasahighschool.org) Class of 2019.

This site is built with [Jekyll](https://jekyllrb.com/), [Bootstrap](http://getbootstrap.com/), and [Sass](https://sass-lang.com/). It is hosted on [Google Firebase](https://firebase.google.com/).

All pages, with the exception of `404.html`, run off of the `default.html` layout, as found in the `_layouts` folder. This layout includes components from the `_includes` folder. In order to modify the navbar, the corresponding component can be edited in `_includes/navbar.html`. This will update all pages once the site is build with Jekyll. All pages can be found in the `_pages` collection, but these files are compiled into the main `_site` directory due to their permalink settings. All static assets, including compiled CSS, images, files, and Javascript, can be found in the `assets` folder.

## Building the Site
1. Install a [Ruby Development Environment](https://jekyllrb.com/docs/installation/)
2. Navigate to the `public` directory in a terminal
3. Install Jekyll and bundler gems
   - Run `gem install jekyll bundler` in a terminal
4. Change to the site directory
5. Install all dependencies via the `Gemfile`
   - Run `bundle install`
6. Serve the site to see changes during development
   - Run `bundle exec jekyll serve`
   - The site will be live at [http://localhost:4000/](http://localhost:4000/)
7. Build the site for deployment
   - Run `bundle exec jekyll build`
   - This will compile all Sass files into `assets/css/main.css`
   - The built site can be found in the `_site` folder
   
## Creating a New Page
1. Create a `.html` file in the `_pages` folder
2. Use the following front matter so that Jekyll will use it in the build
    ```
    ---
    layout: default
    title: <Page Title>
    ---
    ```
3. All asset links are done from the root directory: `/assets/<folder>/<filename>`
    
## Modifying the Stylesheets
- Modify the corresponding `.scss` files in the `_sass` folder of the unbuilt site
- New classes can be added to `_global.scss`
