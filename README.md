# React Aspect Ratio Component

React Aspect Ratio Component

This is a React implementation for aspect ratio placeholder preventing browser reflow before browser downloads and renders your component.

Inspired by awesome post from [CSS Mojo](http://www.cssmojo.com/aspect-ratio-using-custom-properties-and-calc/)

CSS style suggested by [Thierry](https://twitter.com/thierrykoblentz)

Original idea from [Sérgio Gomes](https://twitter.com/sergiomdgomes)

## Usage

**You will need to `import 'react-aspect-ratio/style.css'`**


```js
import AspectRatio from 'react-aspect-ratio';

const RatioImage = () => (
  <AspectRatio ratio="3/4" style={{maxWidth: '400px'}}>
    <img src="https://c1.staticflickr.com/4/3896/14550191836_cc0675d906.jpg" />
  </AspectRatio>
);
```

For browser support [CSS variable](http://caniuse.com/#feat=css-variables), you can use it to wrap other elements (like iframe, video, object ...etc) as well

```js
import AspectRatio from 'react-aspect-ratio';

const RatioIframe = () => (
  <AspectRatio ratio="560/315" style={{maxWidth: '560px'}}>
    <iframe src="https://www.youtube.com/embed/Bku71V5f66g" frameBorder="0" allowFullScreen />
  </AspectRatio>
);
```

Can also use for background image
```js
import AspectRatio from 'react-aspect-ratio';

<AspectRatio
  ratio="3/4"
  style={{
    maxWidth: '300px',
    backgroundImage: 'url(https://c1.staticflickr.com/4/3896/14550191836_cc0675d906.jpg)',
    backgroundSize: 'cover'
  }}
/>
```
