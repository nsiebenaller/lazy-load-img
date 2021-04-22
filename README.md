# lazy-load-img
Web Component demo of a Lazy Load image component

<lazy-load-img> acts as a placeholder for an <img> which will render the <img> when the viewport meets a certain threshold. This reduces page load time by avoiding rendering image assets until they are about to come into the viewport, passing all attributes down to the <img> element.

## Get Started!
Open the `index.html` file with VSCode Live Server or directly in your browser

### Web Components
Web Components is a suite of different technologies allowing you to create reusable custom elements — with their functionality encapsulated away from the rest of your code — and utilize them in your web apps.

### Customization
Currently, the only configuration available is the `data-offset` attribute which overrides the default viewport threshold (200px) that needs to be met before fetching the image. 

Examples:
`data-offset="300px"` - image will be fetched when the bottom of the viewport is 300px away from the element, fetching the image before it enters the viewport is useful so images don't pop in, & possibly causing layout shift.

```
<lazy-load-img
  src="https://images.dog.ceo/breeds/finnish-lapphund/mochilamvan.jpg"
  data-offset="300px"
/>
```
This will fetch a dog picture when the element is <=300px below the viewport
