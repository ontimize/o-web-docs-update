---
permalink: /components/table/aggregate/
title: "Columns aggregate"
---

In this section we are specifing how to define an aggregate column.

{% capture tableColumnCapture %}
{% include o-component-single.md comp="tableColumnAggregate" %}
{% endcapture %}
{{ tableColumnCapture | replace: '    ', ''}}


<h3 class="grey-color">Example</h3>

```html
<o-table service="branches" entity="account" keys="ACCOUNTID"
    columns="ACCOUNTID;ENTITYID;OFFICEID;CDID;ANID;BALANCE;STARTDATE;ENDDATE;INTERESRATE;ACCOUNTTYP"
    visible-columns="ENTITYID;OFFICEID;CDID;ANID;ACCOUNTTYP;BALANCE,INTERESRATE"
    fxFlex layout-padding attr="accounts" title="ACCOUNTS"
    sort-columns="ANID:DESC"  query-on-init="true"
    quick-filter="yes"   filter-case-sensitive="true" >
    <o-table-column attr="BALANCE" title="BALANCE" type="currency" currency-symbol="€" thousand-separator=","></o-table-column>
    <o-table-column attr="INTERESRATE" title="INTERESRATE" type="real" ></o-table-column>
    <o-table-column-aggregate attr="BALANCE" title="sum">
    <o-table-column-aggregate attr="INTERESRATE" [function-aggregate]="custonm"></o-table-column-aggregate>
</o-table>
```


<h3 class="grey-color">Typescript code</h3>

```javascript

  ...

  custom(data:any[]):number{
    let result = 0;
    for(var i=0;i<data.length;i++){
      if(i%2==0) result+=data[i];
    }
    return result;
  }
```