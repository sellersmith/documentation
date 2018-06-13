# UI Components References

## UI Controls

> Almost all UI Controls which extend `UIControl` are placed neatly in the Inspector panel, some common UI Controls usage can be found [here](https://www.w3schools.com/Html/html_form_input_types.asp). Also, please mind the type of inputs as it's not the name of the UI Control. You will need to get into the render part of a given UI Control to see which type it belongs to.

**Props explanation**

| Name | Type | Description |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `type` | string | Type of UI Control |
| `bind` | string | Value binding destination |
| `value` | any | Current value of UI Control |
| `target` | any | The instance that stores the value |
| `group` | string | Deprecated |
| `subscribe` | string | Deprecated |
| `parse` | function | Modify value in |
| `format` | function | Modify value out |
| `onChange` | function | Provide user's input value |
| `active` | any | Deprecated |

### UIInput

![UI Input](../../.gitbook/assets/screen-shot-2018-06-13-at-3.45.46-pm.png)

  
**Code related**

{% code-tabs %}
{% code-tabs-item title="pfapp/projects/playground/views/index.js" %}
```jsx
import UIApp from 'components/ui/providers/UIApp'
import UI from 'components'

export default class extends Component {
   render() {
      return (
         <UIApp>
            <Wrapper>
               <h3>I'm UI Input</h3>
               <UI.Input
                  placeholder="Type something..."
                  onChange={value => {
                     console.log('new value', value)
                  }}
               />
            </Wrapper>
         </UIApp>
      )
   }
}
const Wrapper = styled.div`
   margin: 20px auto;
   text-align: center;
   line-height: 20px;
`
```
{% endcode-tabs-item %}
{% endcode-tabs %}

**Props explanation**

| Name | Type | Description |
| --- | --- | --- | --- | --- | --- |
| `type` | string | Type of input to validate user's input value |
| `size` | string | Size of input box |
| `align` | string | Alignment of the text inside the input box |
| `plain` | boolean | Should remove all styles of the input box |
| `placeholder` | string | Appear when UI Input has no value |



### UIButton

It's `<button />` in html, take a look at the Button "Add New Item" with a little plus on the left side.

![UI Button](../../.gitbook/assets/screen-shot-2018-06-13-at-3.49.48-pm.png)

  
**Code related**

{% code-tabs %}
{% code-tabs-item title="pfapp/projects/playground/views/index.js" %}
```jsx
import UIApp from 'components/ui/providers/UIApp'
import UI from 'components'

export default class extends Component {
   render() {
      return (
         <UIApp>
            <Wrapper>
               <h3>I'm UI Button</h3>
               <UI.Button
                  label="Click me"
                  onClick={e => {
                     console.log('you have just clicked me', e)
                  }}
               />
            </Wrapper>
         </UIApp>
      )
   }
}
const Wrapper = styled.div`
   margin: 20px auto;
   text-align: center;
   line-height: 20px;
`
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### Props explanation

| Name | Type | Description |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `order` | number | Flex order |
| `plain` | boolean | Should remove all styles |
| `size` | string | Size of UI Button |
| `disabled` | boolean | Provide disabled style |
| `danger` | boolean | Provide danger style |
| `compact` | boolean | Provide compact style |
| `loading` | boolean | Should has loading |
| `isLoading` | boolean | Should displays loading |
| `loadingTime` | number | The duration of loading |

### UISelect

UI Select is placed underneath the Font Family label in the below picture.

![UI Select](../../.gitbook/assets/screen-shot-2018-06-13-at-4.03.22-pm.png)

**Code related**

{% code-tabs %}
{% code-tabs-item title="pfapp/projects/playground/views/index.js" %}
```jsx
import UIApp from 'components/ui/providers/UIApp'
import UI from 'components'
import { DropdownInstance } from 'modules/dropdown'
import UIWidget from 'components/ui/interfaces/UIWidget'

export default class extends Component {
   render() {
      return (
         <UIApp>
            <Wrapper>
               <h3>I'm UI Select</h3>
               <UI.Select
                  options={['Option 1', 'Option 2', 'Option 3']}
                  onChange={value => {
                     console.log('selected value', value)
                  }}
               />
               <UIWidget.Portal />
               <DropdownInstance />
            </Wrapper>
         </UIApp>
      )
   }
}
const Wrapper = styled.div`
   margin: 20px auto;
   text-align: center;
   line-height: 20px;
`
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% hint style="info" %}
It's important to have `UIWidget.Portal` and `DropdownInstance`, otherwise, the above code will never run.
{% endhint %}

#### Props explanation

| Name | Type | Description |
| --- | --- | --- | --- | --- | --- | --- |
| `type` | string | Type of UI Select |
| `options` | collection \| string \| object \| array | Options of UI Select |
| `multiple` | boolean | Should allow multiple select |
| `searchable` | boolean | Is allowed to search |
| `emptyOption` | boolean | Should provide an empty option |
| `mapping` | object | Defines label, value and icon to map |

### UICheckbox

![UI Checkbox](../../.gitbook/assets/screen-shot-2018-06-13-at-2.25.17-pm%20%281%29.png)

#### Code related

{% code-tabs %}
{% code-tabs-item title="pfapp/projects/playground/views/index.js" %}
```jsx
import UIApp from 'components/ui/providers/UIApp'
import UI from 'components'

export default class extends Component {
   render() {
      return (
         <UIApp>
            <Wrapper>
               <h3>Hi there ;)</h3>
               We introduce to you our UI Slider.
               <UI.Checkbox
                  label="The checkbox is on my left, and I am its label"
                  isOn
                  onChange={value => {
                     console.log('new value', value)
                  }}
               />
            </Wrapper>
         </UIApp>
      )
   }
}
const Wrapper = styled.div`
   margin: 20px auto;
   text-align: center;
   line-height: 20px;
`
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### Props explanation

| Name | Type | Description |
| --- | --- | --- | --- |
| `isOn` | boolean | Should UI Checkbox be checked by default |
| `label` | string | Label of UI Checkbox |
| `onChange` | function | Triggered after checked state is changed |

### UISlider

![UI Slider](../../.gitbook/assets/screen-shot-2018-06-13-at-2.32.40-pm.png)

#### Code related

{% code-tabs %}
{% code-tabs-item title="pfapp/projects/playground/view/index.js" %}
```jsx
import UIApp from 'components/ui/providers/UIApp'
import UI from 'components'

export default class extends Component {
   render() {
      return (
         <UIApp>
            <Wrapper>
               <h3>I'm UI Slider</h3>
               <UI.Slider
                  min={700}
                  max={1200}
                  step={100}
                  onChange={value => {
                     console.log('new value', value)
                  }}
               />
            </Wrapper>
         </UIApp>
      )
   }
}
const Wrapper = styled.div`
   margin: 20px auto;
   text-align: center;
   line-height: 20px;
`
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### Props explanation

| Name | Type | Description |
| --- | --- | --- | --- | --- | --- |
| `min` | number | Min value |
| `max` | number | Max value |
| `step` | number | Sliding step value |
| `points` | array | An array of sliding points in number format |
| `specialValues` | array | An array of special values which have a match label |

### UISwitch

![UI Switch](../../.gitbook/assets/screen-shot-2018-06-13-at-3.26.28-pm.png)

#### Code related

{% code-tabs %}
{% code-tabs-item title="pfapp/projects/playground/views/index.js" %}
```jsx
import UIApp from 'components/ui/providers/UIApp'
import UI from 'components'

export default class extends Component {
   render() {
      return (
         <UIApp>
            <Wrapper>
               <h3>I'm UI Switch</h3>
               <UI.Switch
                  isOn
                  onChange={value => {
                     console.log('new value', value)
                  }}
               />
            </Wrapper>
         </UIApp>
      )
   }
}
const Wrapper = styled.div`
   margin: 20px auto;
   text-align: center;
   line-height: 20px;
`
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### Props explanation

| Name | Type | Description |
| --- | --- | --- |
| `isOn` | boolean | Should UI Switch is On by default |
| `onChange` | function | Triggered after its state is changed |

## UI Widgets

> All UI Widgets use `UIWidget` - A React Component makes its inheritances floated by increasing their zIndex by one based on a global variable `UIWidget.zIndex` so that the latest gets floated always get the highest `zIndex` value.

{% hint style="info" %}
It's important to have `UIWidget.Portal` rendered somewhere so that all UI Widgets have a place to render
{% endhint %}

### UIPopup

![UI Popup](../../.gitbook/assets/screen-shot-2018-06-12-at-3.20.56-pm.png)

#### Code related

{% code-tabs %}
{% code-tabs-item title="pfapp/projects/playground/views/index.js" %}
```jsx
import UIApp from 'components/ui/providers/UIApp'
import UIWidget from 'components/ui/interfaces/UIWidget'
import UI from 'components'

export default class extends Component {
    render() {
        return (
            <UIApp>
                <UI.Layout>
                    <UIWidget.Portal />
                    <UI.Popup trigger={<UI.Button label="Click me" style={{ margin: '20px auto' }} />} event="focus">
                        <Content>Hello, I'm the popup.</Content>
                    </UI.Popup>
                </UI.Layout>
            </UIApp>
        )
    }
}

const Content = styled.div`
    width: 200px;
    height: 200px;
    margin: 20px;
`
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### Props explanation

| Name | Type | Description |
| --- | --- | --- | --- | --- |
| `trigger` | object | A view to open UI Popup  |
| `event` | string | Which event should UI Popup opens |
| `arrow` | boolean | Should UI Popup has arrow |
| `defaultsPos` | string | Default position for UI Popup |

### UIModal

![UI Modal](../../.gitbook/assets/screen-shot-2018-06-12-at-4.15.47-pm.png)

#### Code related

{% code-tabs %}
{% code-tabs-item title="pfapp/projects/playground/views/index.js" %}
```jsx
import UIApp from 'components/ui/providers/UIApp'
import UIWidget from 'components/ui/interfaces/UIWidget'
import UI from 'components'

export default class extends Component {
   state = {
      open: false
   }
   render() {
      return (
         <UIApp>
            <UI.Layout width={300} >
               <UIWidget.Portal />
               <UI.Button
                  label="Click me"
                  onClick={() => {
                     this.setState({ open: true })
                  }}
                  style={{ margin: '20px auto' }}
               />
               <UI.Modal
                  open={this.state.open}
                  onClickOutside={() => {
                     this.setState({ open: false })
                  }}
                  width={400}
                  height={500}
               >
                  <UI.Layout>
                     <Content>Hello, I'm the modal.</Content>
                  </UI.Layout>
               </UI.Modal>
            </UI.Layout>
         </UIApp>
      )
   }
}

const Content = styled.div`
   width: 200px;
   height: 200px;
   margin: 20px;
`
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### Props explanation

| Name | Type | Description |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `open` | boolean | Should UI Modal open |
| `onClickOutside` | function | Triggered after Modal overlay area is clicked |
| `header` | object | UI Modal header view |
| `footer` | object | UI Modal footer view |
| `onClose` | function | Triggered after close icon on the header is clicked |
| `style` | object | Custom styles for UI Modal |
| `dimmer` | boolean | Should UI Modal overlay is dimmed |
| `closeIcon` | boolean | Should UI Modal has close icon |
| `fullScreen` | boolean | Should UI Modal is full screen |
| `primary` | boolean | Should UI Modal header has primary style |
| `styleHeader` | object | Custom styles for header |
| `styleFooter` | object | Custom styles for footer |

## UI Layouts

### UILayout

> `UILayout` has several static variables inside, they all have the same props which function merely the same with UILayout. For example: `UILayout.Nav`, `UILayout.Sidebar`, `UILayout.Header`,...
>
> We make an example at [here](https://developer.pagefly.io/core/components-usage-guidelines/designing-views-using-ui-layouts).

![UI Layout](../../.gitbook/assets/screen-shot-2018-06-12-at-4.58.22-pm.png)

#### Code related

{% code-tabs %}
{% code-tabs-item title="pfapp/projects/playground/views/index.js" %}
```jsx
import UIApp from 'components/ui/providers/UIApp'
import UI from 'components'

export default class extends Component {
   render() {
      return (
         <UIApp>
            <UI.Layout style={{ border: '1px solid green', width: '500px', margin: '100px auto' }}>
               <Content>Block 1</Content>
               <Content>Block 2</Content>
               <Content>Block 3</Content>
            </UI.Layout>
         </UIApp>
      )
   }
}

const Content = styled.div`
   width: 200px;
   height: 200px;
   margin: 20px;
   background: grey;
   color: white;
`
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### Props explanation

| Name | Type | Description |
| --- | --- | --- | --- | --- |
| `vertical` | boolean | Should UI Layout is ordered vertically |
| `reverse` | boolean | Should UI Layout content is reversed |
| `flex` | string | Flex value for UI Layout |
| `style` | object | Custom styles for UI Layout |

 

