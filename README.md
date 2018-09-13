# Base CSS Setup

Basic CSS setup for future projects incorporating Skeleton CSS and employing Inverted Triangle CSS approach.


### The Grid

There is a basic grid included that uses flexbox as its layout mechanism. Using CSS Grid is ideal on a project by project basis but this grid should work for proprtyping or production layouts.

#### The basics

Creating a basic grid:

```html
<div class="grid">
  <div class="grid__cell">
    ...
  </div>
</div>
```

Flexbox properties allow `.grid__cell` elements to share space evenly within a `.grid`. So three `divs` will form three columns of equal widths.

##### Columns / Cells

A grid is 12 columns by default. Total columns can be adjusted by changing the `$total-columns` variable in the `_vars.scss` partial . Each cell is identified with a `.grid__cell` class.

##### Cell modifiers

Any individual cell can be made to extend to full available width by using the `grid__cell--fill` class. Using this class will cause the cell to take up all available space left by its siblings or all available space if no siblings exist..

##### Gutters

Adding gutters to columns can be done on the grid parent element by adding the `.grid--gutters` class. 

```html
<div class="grid grid--gutters">
  <div class="grid__cell">
    ...
  </div>
  <div class="grid__cell">
    ...
  </div>
  <div class="grid__cell">
    ...
  </div>
</div>
```

Gutter spacing is provided by the `$gutter-spacing` variable in the `_vars.scss` partial . Default is set to 1.5rem.

##### Alignment

Aligning columns inside a grid is acheived with the alignment modifier classes added to the parent `.grid` element:

`.grid--top`: aligns all child elements at top.
`.grid&--middle`: aligns child elements at top.
`.grid&--bottom`: aligns child elements at bottom.
`.grid&--stretch`: stretches child elements to same height.
`.grid&--baseline`: aligns child elements at baseline.
`.grid&--left`: aligns child elements to the left.
`.grid&--center`: centers child elements.
`.grid&--right`: aligns child elements to the right.
`.grid&--between`: spaces child elements across parents distributing empty space between children.
`.grid&--around`: spaces child elements distributing empty space on either side of all children.

##### Small grid

Adding the `.grid--small` to a grid parent retains grid from mobile up. Without the `.grid--small` class, the grid columns cease at `$phablet-up` breakpoint (550px).

##### Grid dictates columns

You can have a grid dictate the number of equal-width columns by adding a class of `.grid--of-X` where `X` is the number of columns you want. The following will allow for  6 columns of equal widths in relation to the parent width. If you add more than six cells, the left over cells will be  pushed down to the next 'row' **and will retain the same width as all other cells**.

```html
<div class="grid grid--of-6">
	...
<div>
```

##### Columns create grids








TODO: Documentation