# Rackspace Developer Experience UX

This is a set of LESS files that can be included in various projects to bring the “bones” of the Developer Experience look-and-feel to those projects. Notably, you'll get these cool tools to add to your project:

**An infinitely flexible, mixin-only grid system**: Rather than filling your markup with a bunch of arbitrary classes to build the basic layout of your application (ahem, Bootstrap), write semantically-appropriate classes and use mixins to apply a grid structure.

```less
.portfolio-thumbnails {
  @gutter-width: 20px;
  @grid(@gutter-width);

  .thumbnail {
    .grid-unit(1/4, @gutter-width);
  }
}
```
**Mixin-based Typography**: Open Sans and Titillium, all with carefully considered sizes and margins. Also lists, tables, preformatted text, and code snippets. Want something to be bold? `.open-sans('bold')`.

**Mixins**: Helper mixins for CSS3 features that still need vendor prefixes, like transform and transition.

## Installation

`bower install git@github.com:rackerlabs/devex-ux.git`

Then, in your LESS project:

`@include "../bower_components/devex-ux/less/ux";`

## Caveats

All this code was literally just stripped out of another project in hopes that it could be reused. As of right now it's missing a lot that you would expect to get from a UI library, and probably makes way too many assumptions about your application.
