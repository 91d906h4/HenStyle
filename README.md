
# HenStyle

This is a simple CSS framework biuld with Sass.

## Compile

Use the following command to compile the Sass files.

```sh
npm run sass ./scss/henstyle.scss -o ./test/henstyle.css
```

## Basic

### Colors

There are 8 colors in HenStyle.css.

- ![#626ED4](https://via.placeholder.com/15/626ED4/000000?text=+) `Primary`
- ![#575c62](https://via.placeholder.com/15/575c62/000000?text=+) `Secondary`
- ![#2AA39A](https://via.placeholder.com/15/2AA39A/000000?text=+) `Success`
- ![#EC4561](https://via.placeholder.com/15/EC4561/000000?text=+) `Danger`
- ![#F8B425](https://via.placeholder.com/15/F8B425/000000?text=+) `Warning`
- ![#38A5F8](https://via.placeholder.com/15/38A5F8/000000?text=+) `Info`
- ![#f8f8fa](https://via.placeholder.com/15/f8f8fa/000000?text=+) `Light`
- ![#343549](https://via.placeholder.com/15/343549/000000?text=+) `Dark`

---

### Containers

Use `.container` class to build the container.

#### Setting

|                    | Extra small<br /><576px | Small<br />≥576px | Mediums<br />≥768px | Large<br />≥992px | X-Large<br />≥1200px | XX-Large<br />≥1400px |
| ------------------ | ----------------------- | ----------------- | ------------------- | ----------------- | -------------------- | --------------------- |
| `.container-sm`    | 100%                    | 540px             | 720px               | 920px             | 1140px               | 1320px                |
| `.container-md`    | 100%                    | 100%              | 720px               | 920px             | 1140px               | 1320px                |
| `.container-lg`    | 100%                    | 100%              | 100%                | 920px             | 1140px               | 1320px                |
| `.container-xl`    | 100%                    | 100%              | 100%                | 100%              | 1140px               | 1320px                |
| `.container-xxl`   | 100%                    | 100%              | 100%                | 100%              | 100%                 | 1320px                |
| `.container-fluid` | 100%                    | 100%              | 100%                | 100%              | 100%                 | 100%                  |

#### Example

```html
<div class="container container-sm">100% wide until small breakpoint.</div>
<div class="container container-lg">100% wide until large breakpoint.</div>
<div class="container container-xxl">100% wide until extra extra breakpoint.</div>
```

---

### Grid System

Use `.row` and `.col` class to build the grid system.

Use `.row-{number}` to specify how many number of rows will be in the elemetnt. The range of `number` is from 1 to 12 (`.row` is same as `.row-12`).

Use `.col-{number}` to specify how many columns will this element takes. Then range of `number` is also from 1 to 12 (`.col` is same as `.col-1`).

#### Example

Now we are going to build a grid with 6 rows and 3 elements with 1 columns, 2 columns and 3 columns, respectively.

```html
<div class="row-6">
    <div class="col">
        Take 1 col.
    </div>
    <div class="col-2">
        Take 2 col.
    </div>
    <div class="col-3">
        Take 3 col.
    </div>
</div>
```

## Component

### Badge

Use class `.badge` to build a badge.

This class should be used with tag `<span></span`.

#### Color

Use `.badge-{color}` to specify the color of the badge.

Default color is `secondary`.

#### Example

```html
<button class="btn btn-primary">Cart <span class="badge badge-dnager">0</span></button>
```

---

### Button

Use class `.btn` to build a button.

#### Color

Use `.btn-{color}` to specify the color of the button.

Use `.btn-outline-{color}` to build a outline button with color `color`.

#### Size

Use `.btn-lg` or `.btn-sm` to change the size of button.

#### Example

If you want to build a large blue button with outline style, you can use the following code.

```html
<button class="btn btn-outline-info btn-lg">Large Blue Button</button>
```

---

### Alert

Use class `.alert` to build a alert.

#### Color

Use `.alert-{color}` to specify the color of alert.

#### Example

```html
<div class="alert alert-danger">Danger!</div>
```

---

### Card

Use class `.card` to build a card.

You should use `.card` with `.card-body`, and the `.card-title` and `.card-text` inside.

If you want to add a header or footer, just use `.card-header` and `.card-footer`.

#### Color

Use `.card-{color}` to specify the color of the card.

#### Example

```html
<div class="card">
    <div class="card-header">Header</div>
    <img src="https://picsum.photos/286/180" />
    <div class="card-body" style="width: 286px;">
        <h5 class="card-title">Title</h5>
        <div class="card-text">This is a demo card with header, footer, title, text and even an image inside.</div>
        <button class="btn btn-primary">GO!</button>
    </div>
    <div class="card-header">Footer</div>
</div>
```

---

### Navbar

Use class `.navbar` to build a navbar.

You can use `.navbar` with `.container` together.

If you want to add a brand, just use `.navbar-brad`.

## Example

```html
<div class="navbar">
    <div class="container container-fluid">
        <a class="navbar-brand">My Navbar</a>
    </div>
</div>
```

## Utilities

### Background Color

Use class `.bg-{color}` and `.bg-light-{colot}` to specify the background colors.

#### Example

A 200x200 box with border and light blue background.

```html
<div class="border bg-light-info" style="height: 200px; width: 200px;">Box</div>
```

---

### Border

Use class `.border` to show the border around.

You can also use `top`, `right`, `bottom`, or `left` to specify which side will show the border.

If you want to disable the border, use `.border-none` to disable the border, or use `.border-top-none`, `.border-bottom-none`.

#### Example

A box without top border.

```html
<div class="border border-top-none" style="height: 200px; width: 200px;">Box</div>
```

---

### Display

Use class `.d-{value}` to set the display of elements.

#### Values

The following are the legal values.

- `none`
- `inline`
- `inline-block`
- `block`
- `grid`
- `inline-grid`
- `table`
- `table-cell`
- `table-row`
- `flex`
- `inline-flex`

#### Example

```html
<div class="d-flex">Flex</div>
```

---

### Opacity

Use class `.opacity-{value}` to specify the opacities of elements.

#### Values

The legal values are `25`, `50`, `75`, and `100`.

#### Example

```html
<div class="opacity-25">...</div>
<div class="opacity-50">...</div>
<div class="opacity-75">...</div>
<div class="opacity-100">...</div>
```

---

### Overflow

Use class `.overflow-{value}` to specify the behavior of elements when overflow occurs.

You can also use `.overflow-x-{value}` and `.overflow-y-{value}`.

#### Values

The legal values are `auto`, `hidden`, `visible`, and `scroll`.

#### Example

```html
<div class="overflow-auto">...</div>
<div class="overflow-hidden">...</div>
<div class="overflow-visible">...</div>
<div class="overflow-scroll">...</div>

<div class="overflow-x-auto">...</div>
<div class="overflow-x-hidden">...</div>
<div class="overflow-x-visible">...</div>
<div class="overflow-x-scroll">...</div>

<div class="overflow-y-auto">...</div>
<div class="overflow-y-hidden">...</div>
<div class="overflow-y-visible">...</div>
<div class="overflow-y-scroll">...</div>
```

---

### Position

Use class `.position-{value}` to specify the position of elemetns.

#### Values

The legal values are `static`, `relative`, `absolute`, `fixed`, and `sticky`.

#### Example

```html
<div class="position-static">...</div>
<div class="position-relative">...</div>
<div class="position-absolute">...</div>
<div class="position-fixed">...</div>
<div class="position-sticky">...</div>
```

---

### Width & Height

Use class `.w-{value}` and `.h-{value}` to specify the width and height of elements.

#### Valeus

The legal values are `25`, `50`, `75`, `100`, and `auto`.

#### Example

```html
<div class="w-25">Width 25%</div>
<div class="w-50">Width 50%</div>
<div class="w-75">Width 75%</div>
<div class="w-100">Width 100%</div>
<div class="w-auto">Width auto</div>

<div class="h-25">Height 25%</div>
<div class="h-50">Height50%</div>
<div class="h-75">Height 75%</div>
<div class="h-100">Height 100%</div>
<div class="h-auto">Height auto</div>
```

---

### Text

#### Aligen

Use class `.text-{value}` to specify the text-align of elements.

The value can be `start`, `center`, or `end`.

#### Word Break

Use class `.text-break` or `.text-break-none` to specify if the word should be break.

#### Text Case

Use class `.text-upper`, `.text-lower` or `.text-capitalize` to specify the text case of elemetns.

#### Decoration

Use class `.text-decoration-{value}` to specify the decoration of elements.

The value can be `none`, `underline`, or `line-through`.

---

### Visibility

Use class `.visible` or `.invisible` to specify whether the element can be seen or not.

---

# Z-Index

Use class `.z-{value}` to specify the z-index of elemetns.

#### Values

The value can be `n1` (-1), `0`, `1`, `2`, or `3`.