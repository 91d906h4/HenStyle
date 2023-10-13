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
## Usage

### Containers

Use `.container` class to build the container.

#### Setting

| | Extra small<br /><576px | Small<br />≥576px | Mediums<br />≥768px | Large<br />≥992px | X-Large<br />≥1200px | XX-Large<br />≥1400px |
| -- | -- | -- | -- | -- | -- | -- |
| `.container-sm` | 100% | 540px | 720px | 920px | 1140px | 1320px |
| `.container-md` | 100% | 100% | 720px | 920px | 1140px | 1320px |
| `.container-lg` | 100% | 100% | 100% | 920px | 1140px | 1320px |
| `.container-xl` | 100% | 100% | 100% | 100% | 1140px | 1320px |
| `.container-xxl` | 100% | 100% | 100% | 100% | 100% | 1320px |
| `.container-fluid` | 100% | 100% | 100% | 100% | 100% | 100% |

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

---

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