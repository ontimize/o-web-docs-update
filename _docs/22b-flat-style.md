---
title: "Flat design"
permalink: /customize/flatdesign/
excerpt: ""
---

{% include base_path %}
{% include toc %}

## What is `flat design`?
Flat design is a user interface design style that **uses simple, two-dimensional elements and bright colors**. It avoids the excessive use of gradients, textures, and drop shadows designed to deliver 3D effects for simpler elements focusing on simple flat elements, typography and flat color schemes such as Strong, contrasting colors to add emphasis on details within icons, illustrations, etc.

## Flat design in Ontimize Web

**Flat design** in Ontimize Web is thinking to merge with the theme of ontimize as shown below.

```scss
// Include ontimize-flat desing
@import 'node_modules/ontimize-web-ngx-theming/ontimize-theme-flat.scss';
@include ontimize-flat-styles($theme);

//Include ontimize-lite theme
@import 'node_modules/ontimize-web-ngx-theming/ontimize-theme-lite.scss';
@include ontimize-theme-styles-lite($theme);

// After define theme, it is necessary to transfer color to Ontimize Web framework
@import 'node_modules/ontimize-web-ngx/theme.scss';
@include o-material-theme($theme);

// Propagate theme to screen styles definition.
@import '../../app/login/login.theme.scss';
@include login-theme($theme);
...

```

![Example of flat desing]({{ "/images/customization/flat design/flat-design.png" | absolute_url }}){: .comp-example-img}

## Color Swatches

Colors is almost the most important part of the Flat Design.

| Success | Primary | Info | Default | Warning | Danger |
| ------- | ------- | ---- | ------- | ------- | ------- |
| <span style="background:#2ecc71;padding:6px;color:white"> #2ecc71 </span> | <span style="background:#1ABC9C;padding:6px;color:white ">#1ABC9C</span> |<span style="background:#3498db;padding:6px;color:white ">#3498db</span> | <span style="background:#bdc3c7;padding:6px;color:white">#bdc3c7</span> | <span style="background:#f1c40f;padding:6px;color:white ">#f1c40f</span> | <span style="background:#e74c3c;padding:6px;color:white">#e74c3c</span>


### Buttons

There is a button class for each sample color as indicated below.

![Buttons]({{ "/images/customization/flat design/buttons.png" | absolute_url }}){: .comp-example-img}

```html
<div fxLayout="row">
  <o-button attr="basic1" type="BASIC" label="BASIC" layout-padding class="o-button-success"></o-button>
  <o-button attr="basic2" type="BASIC" label="PRIMARY" layout-padding class="o-button-primary"></o-button>
  <o-button attr="basic3" type="BASIC" label="INFO " layout-padding class="o-button-info"></o-button>
  <o-button attr="basic3" type="BASIC" label="DEFAULT" layout-padding class="o-button-default"></o-button>
  <o-button attr="basic4" type="BASIC" label="WARNING" layout-padding class="o-button-warning"></o-button>
  <o-button attr="basic5" type="BASIC" label="DANGER" layout-padding class="o-button-danger"></o-button>
</div>
```

### Dialog
![Dialog]({{ "/images/customization/flat design/dialog.png" | absolute_url }}){: .comp-example-img}

