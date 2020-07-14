# Bootstrap4-Grid-System

## About
Originally created by a designer and a developer at Twitter, Bootstrap has become one of the most popular front-end frameworks and open source projects in the world.

Bootstrap was created at Twitter in mid-2010 by @mdo and @fat. Prior to being an open-sourced framework, Bootstrap was known as Twitter Blueprint. A few months into development, Twitter held its first Hack Week and the project exploded as developers of all skill levels jumped in without any external guidance. It served as the style guide for internal tools development at the company for over a year before its public release, and continues to do so today.

Originally released on August 19, 2011, we’ve since had over twenty releases, including two major rewrites with v2 and v3. With Bootstrap 2, we added responsive functionality to the entire framework as an optional stylesheet. Building on that with Bootstrap 3, we rewrote the library once more to make it responsive by default with a mobile first approach.

With Bootstrap 4, we once again rewrote the project to account for two key architectural changes: a migration to Sass and the move to CSS’s flexbox. Our intention is to help in a small way to move the web development community forward by pushing for newer CSS properties, fewer dependencies, and new technologies across more modern browsers.

---

## Getting Started
Bootstrap 4 requires you to import parts of their framework into your project. There are four necessary parts if you were to run all layout, content, components, and utilities within Bootstrap. 

* Bootstrap.css
* Bootstrap.js
* jQuery
* Popper.js

However, it is flexible enough that you can only include the parts that you intend to use instead of the entire project. And these components are the only pieces that require JavaScript (at least bootstrap.js and jQuery):

* **Alerts** for dismissing
* **Buttons** for toggling states and checkbox/radio functionality
* **Carousel** for all slide behaviors, controls, and indicators
* **Collapse** for toggling visibility of content
* **Dropdowns** for displaying and positioning (also requires Popper.js)
* **Modals** for displaying, positioning, and scroll behavior
* **Navbar** for extending our Collapse plugin to implement responsive behavior
* **Tooltips** and popovers for displaying and positioning (also requires Popper.js)
* **Scrollspy** for scroll behavior and navigation updates

You are able to download the sheets and add them to your project, link to the sheets via Content Delivery Network (CDN), or use a package version.

---

## Layout
Components and options for laying out your Bootstrap project, including wrapping containers, a powerful grid system, a flexible media object, and ***responsive*** utility classes.

### Grid
Use our powerful mobile-first flexbox grid to build layouts of all shapes and sizes thanks to a twelve column system, five default responsive tiers, Sass variables and mixins, and dozens of predefined classes.

![](https://i.imgur.com/ShHuW5y.png)

Breaking it down, here’s how it works:

* **Containers** provide a means to center and horizontally pad your site’s contents. Use .container for a responsive pixel width or .container-fluid for width: 100% across all viewport and device sizes.
* **Rows** are wrappers for columns. Each column has horizontal padding (called a gutter) for controlling the space between them. This padding is then counteracted on the rows with negative margins. This way, all the content in your columns is visually aligned down the left side.
* ***In a grid layout, content must be placed within columns and only columns may be immediate children of rows.***
* Thanks to flexbox, grid columns without a specified width will automatically layout as equal width columns. For example, four instances of .col-sm will each automatically be 25% wide from the small breakpoint and up. See the auto-layout columns section for more examples.
* **Column classes** indicate the number of columns you’d like to use out of the possible 12 per row. So, if you want three equal-width columns across, you can use .col-4.
* **Column widths** are set in percentages, so they’re always fluid and sized relative to their parent element.
* Columns have horizontal padding to create the gutters between individual columns, however, you can remove the margin from rows and padding from columns with .no-gutters on the .row.
* To make the grid ***responsive***, there are ***five grid breakpoints***, one for each responsive breakpoint: all breakpoints (extra small), small, medium, large, and extra large.
* ***Grid breakpoints*** are based on minimum width media queries, meaning they apply to that one breakpoint and all those above it (e.g., .col-sm-4 applies to small, medium, large, and extra large devices, but not the first xs breakpoint).
* You can use predefined grid classes (like .col-4) or Sass mixins for more semantic markup.

Be aware of the limitations and bugs around flexbox, like the inability to use some HTML elements as flex containers.

### Grid options

While Bootstrap uses ems or rems for defining most sizes, pxs are used for grid breakpoints and container widths. This is because the viewport width is in pixels and does not change with the font size.

See how aspects of the Bootstrap grid system work across multiple devices with a handy table.

<table>
    <tr>
        <td></td>
        <td><p style="text-align: center;"><b>Extra Small</b></p><p style="text-align: center;">&lt;576px</p></td>
        <td><p style="text-align: center;"><b>Small</b></p><p style="text-align: center;">≥576px</p></td>
        <td><p style="text-align: center;"><b>Medium</b></p><p style="text-align: center;">≥768px</p></td>
        <td><p style="text-align: center;"><b>Large</b></p><p style="text-align: center;">≥992px</p></td>
        <td><p style="text-align: center;"><b>Extra Large</b></p><p style="text-align: center;">≥1200px</p></td>
    </tr>
    <tr>
        <th>Max container width</th>
        <td style="text-align: center;">None (auto)</td>
        <td style="text-align: center;">540px</td>
        <td style="text-align: center;">720px</td>
        <td style="text-align: center;">960px</td>
        <td style="text-align: center;">1140px</td>
    </tr>
    <tr>
        <th>Class prefix</th>
        <td style="text-align: center;">.col-</td>
        <td style="text-align: center;">.col-sm-</td>
        <td style="text-align: center;">.col-md-</td>
        <td style="text-align: center;">.col-lg-</td>
        <td style="text-align: center;">.col-xl-</td>
    </tr>
    <tr>
        <th>Gutter width</th>
        <td colspan=5 >12</td>
    </tr>
    <tr>
        <th>Nestable</th>
        <td colspan=5>Yes</td>
    </tr>
    <tr>
        <th>Column ordering</th>
        <td colspan=5>Yes</td>
    </tr>
</table>
