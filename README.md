<style>
    /* Basic button style */
.btn {
  /* Disply */
  display: inline-block;
  /* Box */
  padding: 0.375rem 0.75rem;
  border: 1px solid transparent;
  /* Border */
  border-radius: 0.375rem;
  /* Color */
  color: #343549;
  background-color: transparent;
  /* Transition */
  transition-duration: 350ms;
  /* Hover */
}
.btn:hover {
  filter: brightness(110%);
  cursor: pointer;
}

/* Size */
.btn-lg {
  padding: 0.5rem 1rem;
  font-size: 1.5rem;
}

.btn-sm {
  padding: 0.25rem 0.5rem;
  font-size: 0.8rem;
}

/* Button background color */
.btn-primary {
  background-color: #626ED4;
  color: white;
}

/* Outline button */
.btn-outline-primary {
  border-color: #626ED4;
  color: #626ED4;
}
.btn-outline-primary:hover {
  background-color: #626ED4;
  color: white;
}

/* Button background color */
.btn-secondary {
  background-color: #575c62;
  color: white;
}

/* Outline button */
.btn-outline-secondary {
  border-color: #575c62;
  color: #575c62;
}
.btn-outline-secondary:hover {
  background-color: #575c62;
  color: white;
}

/* Button background color */
.btn-success {
  background-color: #2AA39A;
  color: white;
}

/* Outline button */
.btn-outline-success {
  border-color: #2AA39A;
  color: #2AA39A;
}
.btn-outline-success:hover {
  background-color: #2AA39A;
  color: white;
}

/* Button background color */
.btn-danger {
  background-color: #EC4561;
  color: white;
}

/* Outline button */
.btn-outline-danger {
  border-color: #EC4561;
  color: #EC4561;
}
.btn-outline-danger:hover {
  background-color: #EC4561;
  color: white;
}

/* Button background color */
.btn-warning {
  background-color: #F8B425;
  color: white;
}

/* Outline button */
.btn-outline-warning {
  border-color: #F8B425;
  color: #F8B425;
}
.btn-outline-warning:hover {
  background-color: #F8B425;
  color: white;
}

/* Button background color */
.btn-info {
  background-color: #38A5F8;
  color: white;
}

/* Outline button */
.btn-outline-info {
  border-color: #38A5F8;
  color: #38A5F8;
}
.btn-outline-info:hover {
  background-color: #38A5F8;
  color: white;
}

/* Button background color */
.btn-light {
  background-color: #f8f8fa;
  color: white;
}

/* Outline button */
.btn-outline-light {
  border-color: #f8f8fa;
  color: #f8f8fa;
}
.btn-outline-light:hover {
  background-color: #f8f8fa;
  color: white;
}

/* Button background color */
.btn-dark {
  background-color: #343549;
  color: white;
}

/* Outline button */
.btn-outline-dark {
  border-color: #343549;
  color: #343549;
}
.btn-outline-dark:hover {
  background-color: #343549;
  color: white;
}
</style>

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
## Component

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

<button class="btn btn-primary">Cart</button>

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