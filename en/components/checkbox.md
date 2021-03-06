---
title: Checkbox Component
_description: Ignite UI for Angular Checkbox component is a selection control that allows users to make a binary choice for a certain condition.
_keywords: Ignite UI for Angular, UI controls, Angular widgets, web widgets, UI widgets, Angular, Native Angular Components Suite, Native Angular Controls, Native Angular Components Library, Angular Checkbox components, Angular Checkbox controls
---

##Checkbox
<p class="highlight">The Ignite UI for Angular Checkbox component is a selection control that allows users to make a binary choice for a certain condition. It behaves similarly to the native browser checkbox.</p>
<div class="divider"></div>

### Checkbox Demo
<div class="sample-container" style="height: 200px">
<iframe src='{environment:demosBaseUrl}/checkbox-sample-2' width="100%" height="100%" seamless frameBorder="0"></iframe>
</div>
<div class="divider--half"></div>

### Usage
At its core the checkbox component allows for a choice between selected/unselected state. The default styling is done according to the selection controls specification as per the Material Design guidelines.
To get started with the Ignite UI for Angular Checkbox import the **IgxCheckboxModule** in the **app.module.ts** file:

```typescript
// app.module.ts

...
import { IgxCheckboxModule } from 'igniteui-angular/main';

@NgModule({
    ...
    imports: [..., IgxCheckboxModule],
    ...
})
export class AppModule {}
```

To get a simple checkbox, add the following code inside the compnent template:

```html
<igx-checkbox checked="true">
    simple checkbox
</igx-checkbox>
```

If all went well, you should see something like the following in the browser:

<div class="sample-container" style="height: 100px">
<iframe src='{environment:demosBaseUrl}/checkbox-sample-1' width="100%" height="100%" seamless frameBorder="0"></iframe>
</div>

#### Checkbox properties

Let's enhance the code above by binding the checkbox properties to some data. Say, we have an array of task objects, each having two properties: description and done. You can bind the checkbox component checked property to the underlying task object done property. Analogically you can bind the value property to description.
Optionally, you can also bind the change event and add some custom logic in the provided event handler method.

```typescript
// tasks.component.ts
...
public tasks = [
  { done: true, description: 'Research' },
  { done: true, description: 'Implement' },
  { done: false, description: 'Test' },
];

...
statusChanged()
{
    // event handler logic
}
```
Enhance the component template by adding a checkbox for each task and then setting the corresponding property bindings:

```html
<!--tasks.component.html-->

<igx-checkbox *ngFor="let task of tasks" [checked]="task.done">
    {{ task.description }}
</igx-checkbox>
```

The final result would be something like that:

<div class="sample-container" style="height: 200px">
<iframe src='{environment:demosBaseUrl}/checkbox-sample-2' width="100%" height="100%" seamless frameBorder="0"></iframe>
</div>

### API Summary

####Inputs
The following inputs are available on the **igx-checkbox** component:
| Name | Type | Description |
| :--- | :--- | :--- |
| `checked` | bool | Checkbox is checked if true. |

<div class="divider"></div>

####Outputs
The following outputs are available on the **igx-checkbox** component:
| Name | Type | Description |
| :--- | :--- | :--- |
| `change` | EventEmitter | Emits an event when the checkbox is clicked. |

###Additional Resources

<div class="divider--half"></div>
Our community is active and always welcoming to new ideas.

* [Ignite UI for Angular **Forums**](https://www.infragistics.com/community/forums/f/ignite-ui-for-angular)
* [Ignite UI for Angular **GitHub**](https://github.com/IgniteUI/igniteui-angular)



