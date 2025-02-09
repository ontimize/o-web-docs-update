---
title: "Icons"
permalink: /customize/icons/
excerpt: "How you can add icons to your app."
---

{% include base_path %}
{% include toc %}

## How to use Material Design icons
Every Ontimize Web component having a icon input might use one of the available icons in  [Google material design icons](https://design.google.com/icons/){:target='_blank'}.


## Ontimize Web icons
The Ontimize Web components uses a set of icons stored internally in svg format. You can also use that icons as you can see in the following example:

```html
<mat-icon svgIcon="ontimize:ICON_NAME"></mat-icon>
```

Where you can replace 'ICON_NAME' for one of the following icons (stored [here](https://github.com/OntimizeWeb/ontimize-web-ngx/blob/master/projects/ontimize-web-ngx/assets/svg/ontimize-icon-set.svg){:target='_blank'}):

| BTC | USD | EUR | LIR | PERCENT | GBP | INR | ILS |
| KRW | JPY | add | LIR | keyboard_arrow_left | keyboard_arrow_right | keyboard_arrow_down | keyboard_arrow_up |
| menu | delete | edit | save | clear | done | autorenew | undo |
| perm_identity | vpn_key | arrow_back | mail_outline | search | today | visibility | visibility_off |
| more_vert | filter_list | power_settings_new | settings | drag_handle | first_page | last_page | info_outline |
| error_outline | check_circle | close | EXCEL | PERCENT | HTML | PDF | clock |
| folder_open | fullscreen | sort_by_alpha_desc  | sort_by_alpha_asc  | sort_by_alpha  |   |   |   |

### Adding a svg icon
If you want to add a svg icon to the ontimize icon set you must follow this steps:

* Inject `OntimizeMatIconRegistry` service.
* Define a name for your icon.
* Store your icon in your app resources.
* Use the `OntimizeMatIconRegistry` service `addOntimizeSvgIcon` method (It is recommended to use it in the app main component).

```javascript
import { Component, OnInit, Injector, ViewChild, Inject } from '@angular/core';
import { OntimizeMatIconRegistry } from 'ontimize-web-ngx';

@Component({
  selector: 'o-app',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss']
})
export class AppComponent implements OnInit {
  ontimizeMatIconRegistry: OntimizeMatIconRegistry;

  constructor(protected injector: Injector) {
    this.ontimizeMatIconRegistry = this.injector.get(OntimizeMatIconRegistry);
  }

  ngOnInit() {
    if (this.ontimizeMatIconRegistry.addOntimizeSvgIcon) {
      this.ontimizeMatIconRegistry.addOntimizeSvgIcon('newIcon', 'assets/images/new-icon.svg');
    }
  }
}
```

