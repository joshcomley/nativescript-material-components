[![npm](https://img.shields.io/npm/v/nativescript-material-textview.svg)](https://www.npmjs.com/package/nativescript-material-textview)
[![npm](https://img.shields.io/npm/dt/nativescript-material-textview.svg?label=npm%20downloads)](https://www.npmjs.com/package/nativescript-material-textview)
[![GitHub forks](https://img.shields.io/github/forks/Akylas/nativescript-material-components.svg)](https://github.com/Akylas/nativescript-material-components/network)
[![GitHub stars](https://img.shields.io/github/stars/Akylas/nativescript-material-components.svg)](https://github.com/Akylas/nativescript-material-components/stargazers)

## Installation

If using ```@nativescript``` :
* `tns plugin add nativescript-material-textview`

If using ```tns-core-modules```
* `tns plugin add nativescript-material-textview@2.5.4`

Be sure to run a new build after adding plugins to avoid any issues.

---

##### [Material Design Spec](https://material.io/design/components/text-fields.html)

### Usage


## Plain NativeScript

<span style="color:red">IMPORTANT: </span>_Make sure you include `xmlns:mdt="nativescript-material-textview"` on the Page element_

### XML

```XML
<Page xmlns:mdt="nativescript-material-textview">
    <StackLayout horizontalAlignment="center">
        <mdt:TextView text="raised textview"/>
        <mdt:TextView variant="flat" text="flat textview"/>
        <mdt:TextView variant="text" text="text textview"/>
        <mdt:TextView elevation="5" rippleColor="red" text="raised custom textview"/>
   </StackLayout>
</Page>
```

### CSS

```CSS
mdctextview {
    ripple-color: blue;
    elevation: 4;
}
```

## NativeScript + Angular

```typescript
import { NativeScriptMaterialTextViewModule } from "nativescript-material-textview/angular";

@NgModule({
    imports: [
        NativeScriptMaterialTextViewModule,
        ...
    ],
    ...
})
```

```html
<MDTextView  helper="example helper" placeholderColor="green" keyboardType="datetime"
        hint="i am an hint" returnKeyType="next" (focus)="onFocus($event)" (blur)="onBlur($event)"
        (textChange)="onTextChange($event)"></MDTextView>
```

## NativeScript + Vue

```javascript
import TextViewPlugin from 'nativescript-material-textview/vue';

Vue.use(TextViewPlugin);
```

```html
<MDTextView helper="example helper" placeholderColor="green" keyboardType="datetime"
        hint="i am an hint" returnKeyType="next" @focus="onFocus" @blur="onBlur"
        @textChange="onTextChange"/>
```

Also, you can bind the text to some instance data using the `v-model` directive:

```html
<MDTextView v-model="value" />
```


## Attributes

Inherite from Nativescript [TextView](https://docs.nativescript.org/ui/ns-ui-widgets/text-view) so it already has all the same attributes

## Attributes

* **variant** _optional_

An attribute to set the variant of the textview. Can be ```outline``` or ```underline``` or ```filled```. No value means ```underline``` textview

* **errorColor** _optional_

An attribute to set the error color of the textview.

* **helper** _optional_

An attribute to set the helper text of the textview.

* **floating** _optional_

A boolean attribute to set the floating state of the textview.
