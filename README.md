# minssg

minimum static site generator.

- imports
- layouts
- dev server w/ hot reloading

## Getting started

```bash
bun add minssg
```

### Folder structure

```
src
├── public
│   ├── index.html
│   ├── posts.html
├── templates
│   ├── header.html
│   ├── footer.html
│   ├── base-layout.html
```

### Basic Templates

```html
<!DOCTYPE html>
<html lang="en">
    <!-- @import './header.html' -->
 <body>
    <h1>Hello, World!</h1>
    <!-- @import './footer.html' -->
 </body>
</html>
```

### Layouts

in `templates/base-layout.html`
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <!-- @import './head.html' -->
    <title>{{ title }}</title>
  </head>
  <body>
    <main>
      <a href="/">Home</a>
      <!-- @slot -->
    </main>
    <!-- @import './footer.html' -->
  </body>
</html>
```

in `public/index.html`

```html
<!-- @layout './base-layout.html' { "title": "Home" } -->
 <h1>Hello, World!</h1>
```

### Dev Server w/ hot reloading

```bash
bunx minssg serve
```

### Build

```bash
bunx minssg build
```