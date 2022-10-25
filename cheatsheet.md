# Tailwind CSS Cheat Sheet

## Responsive Design ([Tailwind Docs](https://tailwindcss.com/docs/responsive-design))

At the heart of Tailwind is the concept of Mobile first design.  Roughly translated that means that all utilities that aren't prefixed will apply to all of the breakpoints.  Tailwind has a number of pre configured breakpoints.

<kbd>sm</kbd>  Equates to a minimum width of 640px creating a media statement @media (min-width: 640px)<br>
<kbd>md</kbd>  Equates to a minimum width of 768px creating a media statement @media (min-width: 768px)<br>
<kbd>lg</kbd>  Equates to a minimum width of 1024px creating a media statement @media (min-width: 1024px)<br>
<kbd>xl</kbd>  Equates to a minimum width of 1280px creating a media statement @media (min-width: 1280px)<br>
<kbd>2xl</kbd>  Equates to a minimum width of 1536px creating a media statement @media (min-width: 1536px)

To add a utility but only have it take effect at certain breakpoinys all that need br done is to prefix the utility with the breakpoint followed by a colon.

```html
<!-- Width of 16 by default, 32 on medium screens, and 48 on large screens -->
<img class="w-16 md:w-32 lg:w-48" src="...">
```



## Spacing  

Spacing can be applied to 

Top <kbd> t </kbd>  :  Bottom <kbd> b </kbd> : Left <kbd> l </kbd> : Right <kbd> r </kbd>  : Top and Bottom <kbd> y  </kbd> : Left and Right <kbd> x </kbd>

### Padding ([Tailwind Docs](https://tailwindcss.com/docs/padding))

The basic syntax is <kbd> p </kbd>  followed by the number of Pixels.  It can be applied specificall with the use of the spacing modifioers ie;  <kbd> pt-4 </kbd> to produce a top padding of 4 pixels.

### Margin  ([Tailwind Docs](https://tailwindcss.com/docs/margin))

Margin follows the same principles as padding but using <kbd> m </kbd> instead.

### Space Between  ([Tailwind Docs](https://tailwindcss.com/docs/space))

The space class provides a way to create space between child elements ie; <kbd> space-x-0.5 </kbd>  will add a margin to the left of all child elements 0f 0.125 rem (2px).


## Sizing

We have basic width and height sizing

### Width

Width <kbd> w </kbd>  ([Tailwind Docs](https://tailwindcss.com/docs/width)) :  Min-Width <kbd> min-w </kbd>  ([Tailwind Docs](https://tailwindcss.com/docs/min-width)) : Max-Width  <kbd> max-w </kbd>  ([Tailwind Docs](https://tailwindcss.com/docs/max-width)).

### Height

Height <kbd> h </kbd>  ([Tailwind Docs](https://tailwindcss.com/docs/height)) :  Min-Height <kbd> min-h </kbd>  ([Tailwind Docs](https://tailwindcss.com/docs/min-height)) : Max-Height  <kbd> max-h </kbd>  ([Tailwind Docs](https://tailwindcss.com/docs/max-height)).


## Borders

Basic syntax is <kbd> border </kbd> to which can be added colour, width or style.  In addition you can configure radius <kbd> rounded </kbd>, divide  <kbd> divide </kbd>, outline <kbd> outline </kbd> and ring <kbd> ring </kbd>.  Check the [Tailwind Docs](https://tailwindcss.com/docs/border-radius) for more specific details.


## Backgrounds

Basic syntax is <kbd> bg </kbd>. Check the [Tailwind Docs](https://tailwindcss.com/docs/background-attachment) for more info.


## Colours

Tailwind CSS has a vast number of pre-defined colours across a wide range of shades.  However it is perfectly possible to add to these should you so wish.  See the [Tailwind Docs](https://tailwindcss.com/docs/customizing-colors) for more information.  The following resource is also very useful for creating new colours and shades [Tailwind Colour Generator](https://tailwind.simeongriggs.dev/blue/3B82F6).


## Flex and Grid

As you might by now be expecting we have basic syntax for Flex <kbd> flex </kbd>, Grid <kbd> grid </kbd> and Gap <kbd> gap </kbd>.

As you would expect there are a vast number of things that you can do with these.  For more informantion check the [Tailwind Docs](https://tailwindcss.com/docs/flex-basis).


## Typeography

<kbd> font </kbd> and  <kbd> text </kbd> are the basic utility classes for use with typeography.  Check out the documentation for more information. [Tailwind Docs](https://tailwindcss.com/docs/font-family)