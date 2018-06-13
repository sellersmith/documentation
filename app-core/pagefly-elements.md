# Pagefly Elements



## Introduction \*\*\*

explain the significant importants of elements

### Output

All element output should always be HTML and must the as elementary as possible

```markup
<section>...</section>
<h3>Lorem ipsum dolor sit amet</h3v>
<p>Lorem ipsum dolor sit amet</p>
```

### Datastore

How element data are store and how does it flow through our application

```javascript
{
    "type": "Heading"
}
```

## Files Structure

All elements are located in the /common/elements folder or /projects/{name}/elements if override. Create a folder with the name of the element. This is the type name of the element so the app knows where to load your element. Note that this name should be fixed and should not be changed in the future so pick the name wisely. Your element folder should look like the following

* elements/
  * Example/
    * Example.js
    * Foo.js

According to the above structure, we have to elements "Example" and Example.Foo

## Code the element 

### Edit the file Example.js. 

All elements is sub class of Element so we need to import it first

```jsx
import Element from 'components/Element'
```

Then export default the class of your element. Element class should have a render\(\) method as required by React

```jsx
export default class Example extends Element {
    render() {
        return <div>This is an example element</div>
    }
}
```



