# `breakpoints`

Simple code snippet to make working with media queries easier and more enjoyable. Comes in handy in projects that use SCSS

## Usage

You can import this snippet wherever you want - in your main file containing all of your styles or you could create a file like _breakpoints.scss and paste it here. It's totally up to you!

```scss
// _breakpoints.scss

@mixin breakpoint($breakpoint) {
  $breakpoints: (
    "sm": "576px",
    "md": "768px",
    "lg": "992px",
    "xl": "1200px",
  );

  @media screen and (min-width: #{map-get($breakpoints, $breakpoint)}) {
    @content;
  }
}
```

Then you can use it like so:

```scss
@import "breakpoints";

...
@include breakpoint("md") {
  // Your styling for "md" breakpoint goes here
}
...
```


