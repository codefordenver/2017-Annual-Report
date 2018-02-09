## 2017-Annual-Report

[![Stories Ready to Work On](https://badge.waffle.io/codefordenver/2017-Annual-Report.svg?label=ready&title=Cards%20Ready%20To%20Work%20On)](https://waffle.io/codefordenver/2017-Annual-Report)

This repo was created from https://cfd-new.herokuapp.com. Use [the Waffle board](https://waffle.io/codefordenver/2017-Annual-Report) for this repo to always know what to do next for your project!

## CSS

Uses LESS to compile CSS styles.
Sample usage in Windows command line:
lessc styles.less styles.css

## Adding a new slide for animations
1. Increment the @numberOfSlides variable in styles.less
2. Add CSS styles for the new slide. In styles.less, under .carousel, add a position rule under each of the &--background, &--midground and &--foreground files:
```CSS
&.position-[POSITION] {
	left: @width * -[POSITION-1];
}
```
Where [POSITION] is the slide number (the first slide is #1, not #0). [POSITION-1] should be the slide number -1.
3. Compile the CSS with LESS.
4. In the HTML, create a new slide under the div with a class of carousel--background. Copy and paste one of the divs with a class of slide to use as a template for a new slide. The new slide should go at the end, and should have a class of slide-[POSITION] as well as slide.
5. Repeat step 4 for both the divs with a class of carousel--midground and carousel--foreground.