# HenStyle

This is a simple CSS framework biuld with Sass.

## Compile

Use the following command to compile the Sass files.

```sh
npm run sass ./scss/henstyle.scss -o ./test/henstyle.css
```

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