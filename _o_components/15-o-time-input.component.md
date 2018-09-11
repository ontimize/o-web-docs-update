---
permalink: /components/input/time/
title: "Time"
comp: time
---

{% include base_path %}
{% include toc %}

The `o-time-input` component is used in [forms]({{ base_path }}/components/form/) for getting or displaying a date and hour input submitted by the user.

The time input is automatically registered on its parent `o-form`, which provides the value for the input programatically. Its value can be also set manually via the `data` parameter. This and other attributes are explained on the **API** section of this page.

## Basic example
![Time input component]({{ "/images/components/inputs/o-time-input.png" | absolute_url }}){: .comp-example-img}

```html
<o-form editable-detail="no" show-header="no">
   <div fxLayout="column" layout-padding>
      <label class="input-comp-title">{{ 'INPUTS.READ_ONLY' | oTranslate }}</label>
      <o-time-input fxFlex attr="input" label="{{ 'INPUT.BUTTON.TIME' | oTranslate }}" [data]="getValue()"></o-time-input>
    </div>
    <div fxLayout="column" layout-padding>
      <label class="input-comp-title">{{ 'INPUTS.EDITABLE' | oTranslate }}</label>
      <o-time-input attr="input2" label="{{ 'INPUT.BUTTON.TIME' | oTranslate }}" [data]="getValue()" read-only="no" required="yes"
        tooltip="This is an awesome tooltip!" clear-button="yes" format="24"></o-time-input>
    </div>
    <div fxLayout="column" layout-padding>
      <label class="input-comp-title">{{ 'INPUTS.DISABLED' | oTranslate }}</label>
      <o-time-input attr="input3" label="{{ 'INPUT.BUTTON.TIME' | oTranslate }}" enabled="no" [data]="getValue()"></o-time-input>
</o-form>
```
You can see this and more examples of this component in the [OntimizeWeb playground](https://try.imatia.com/ontimizeweb/playground/main/inputs/time){:target="_blank"}.
