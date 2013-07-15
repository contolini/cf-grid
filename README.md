# [Ghost](https://github.cfpb.gov/pages/front/ghost/grid/index.html)

A LESS-based CSS3 grid system using parametric mixins to encourage semantic HTML. Ghost has three main features:

1. Provides fixed-width gutters and fluid-width columns.
1. Works seamlessly with any combination of grid and gutter widths.
1. Keeps HTML semantic by not including presentational classes in markup.


## Semantic HTML

Instead of:

```html
<header class="row">
    <aside class="span4">
        Lorem ipsum Ut deserunt do nostrud. 
    </aside>
    <section class="span8">
        Lorem ipsum Voluptate pariatur Duis fugiat cupidatat quis pariatur.
    </section>
</header>
```

Ghost allows you to write:

```html
<header>
    <aside class="welcome-message">
        Lorem ipsum Ut deserunt do nostrud. 
    </aside>
    <section class="customer-info">
        Lorem ipsum Voluptate pariatur Duis fugiat cupidatat quis pariatur.
    </section>
</header>
```

Using LESS that looks like this:

```less
.welcome-message {
  .column(4);
}

.customer-info {
  .column(8);
}
```


## Getting Started

Grab `ghost.less` from the `dist` directory and @import it at the top of your application's LESS stylesheet.


## Documentation

More extensive documentation is coming soon, but in the meantime, the `ghost.less` file should be commented well 
enough to get you started.


## Examples

<<<<<<< Updated upstream
There is a [test runner](https://github.cfpb.gov/pages/front/ghost/grid/index.html) and an example of [Bootstrap integration](https://github.cfpb.gov/pages/front/ghost/bootstrap/index.html). These examples can be found in the archive at `dist/example.zip`. They use less.js to compile their LESS. You'll need to run a server locally to avoid cross-origin complaints. Try `python -m SimpleHTTPServer` in the example's directory.
=======
There is a [test runner](https://github.cfpb.gov/pages/contolini/ghost/grid/index.html) and an example of 
[Bootstrap integration](https://github.cfpb.gov/pages/contolini/ghost/bootstrap/index.html). These examples can be 
found in the archive at `dist/example.zip`. They use less.js to compile their LESS. You'll need to run a server 
locally to avoid cross-origin complaints. Try `python -m SimpleHTTPServer` in the example's directory.

Ghost is used by [Qui](https://github.cfpb.gov/pages/contolini/qui) 
(<a href="https://github.cfpb.gov/contolini/qui/blob/master/src/less/main.less">stylesheet</a>).


## Known Issues

* **Rounding and Rendering** – Certain browsers (most notably Safari and IE7) either (a) have poor precision when 
  rounding percentage values, (b) don't support subpixel rendering, or both.
* **Prefix/Suffix not supported in IE7** – It doesn't seem to be able to handle percentage-based padding.
>>>>>>> Stashed changes

## Contributing

Edit the files in `src` and run `grunt build` whenever you're ready to compile LESS and automagically copy appropriate source files into the `dist` dir, archiving the examples in a .zip. Running `grunt` with no options will start a server on port 8000 (for testing the [examples](https://github.cfpb.gov/contolini/ghost/tree/master/src/examples) locally) and automatically `build` whenever a source file is changed.

In lieu of a formal styleguide, take care to maintain the existing coding style.

## Release History

 * 2013-07-15   v0.5.2   Update README to be accurate. Remove a little bit of outdated stuff from ghost.less.
 * 2013-07-15   v0.5.1   Moved repo and updated documentation links accordingly.
 * 2013-07-13   v0.5.0   Total rewrite to use box-sizing and padding instead of calc(). Compile examples' LESS.
 * 2013-07-12   v0.4.2   Add proper git tag.
 * 2013-07-11   v0.4.1   Bump package.json version to aid dependency management.
 * 2013-07-01   v0.4.0   Add grunt-cfpb-internal to manage semantic versioning.

## License

Software source code written entirely by Consumer Financial Protection Bureau staff, and by contractors who are developing software on behalf of CFPB, is by default a public domain work.

Software source code previously released under an open source license and then modified by CFPB staff is considered a "joint work" (see 17 USC § 101); it is partially copyrighted, partially public domain, and as a whole is protected by the copyrights of the non-government authors and must be released according to the terms of the original open-source license.

For further details, please see: http://www.consumerfinance.gov/developers/sourcecodepolicy/

---

*This file was generated on Mon Jul 15 2013 13:43:17.*
