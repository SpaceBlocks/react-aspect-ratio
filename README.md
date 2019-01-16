<p align="center">
  <h1>React Aspect Ratio</h1>
  <img src="https://cloud.githubusercontent.com/assets/3906130/23882532/7e0cd586-081e-11e7-995f-005196385335.jpg" width="400" alt="reac aspect ratio">
  <br>
  <a href="https://www.npmjs.org/package/react-aspect-ratio"><img src="https://img.shields.io/npm/v/react-aspect-ratio.svg?style=flat" alt="npm"></a>
  <a href="https://unpkg.com/react-aspect-ratio"><img src="https://img.badgesize.io/https://unpkg.com/react-aspect-ratio/dist/es/index.js?compression=gzip" alt="gzip size"></a>
  <a href="https://www.npmjs.com/package/react-aspect-ratio"><img src="https://img.shields.io/npm/dt/react-aspect-ratio.svg" alt="downloads" ></a>
  <a href="https://circleci.com/gh/roderickhsiao/react-aspect-ratio"><img src="https://circleci.com/gh/roderickhsiao/react-aspect-ratio.svg?style=svg" alt="circleci"></a>
</p>

<hr>
This is a React implementation for aspect ratio placeholder preventing browser reflow before browser downloads and renders your component.

[Demo](https://roderickhsiao.github.io/react-aspect-ratio/)

Inspired by [Thierry](https://twitter.com/thierrykoblentz)

Original idea from [Sérgio Gomes](https://twitter.com/sergiomdgomes)

You can also read a detail [post](https://css-tricks.com/aspect-ratio-boxes/) by [Chris Coyier](https://twitter.com/chriscoyier)

## Installation

via [yarn](https://yarnpkg.com/en/docs)

```
$ yarn add react-aspect-ratio
```

or via [npm](https://docs.npmjs.com/)

```
$ npm install react-aspect-ratio
```

## Usage

**You will need to `import 'react-aspect-ratio/aspect-ratio.css'`**

```js
import AspectRatio from 'react-aspect-ratio';

const RatioImage = () => (
  <AspectRatio ratio="3/4" style={{ maxWidth: '400px' }}>
    <img src="https://c1.staticflickr.com/4/3896/14550191836_cc0675d906.jpg" />
  </AspectRatio>
);
```

For browser support [CSS variable](http://caniuse.com/#feat=css-variables), you can use it to wrap other elements (like iframe, video, object ...etc) as well

```js
import AspectRatio from 'react-aspect-ratio';

const RatioIframe = () => (
  <AspectRatio ratio="560/315" style={{ maxWidth: '560px' }}>
    <iframe src="https://www.youtube.com/embed/Bku71V5f66g" frameBorder="0" allowFullScreen />
  </AspectRatio>
);
```

Can also use for background image

```js
import AspectRatio from 'react-aspect-ratio';

<AspectRatio
  ratio={0.75}
  style={{
    maxWidth: '300px',
    backgroundImage: 'url(https://c1.staticflickr.com/4/3896/14550191836_cc0675d906.jpg)',
    backgroundSize: 'cover'
  }}
/>;
```

## API

### Props

- `ratio`: string | number
- any other props, note that the component will add custom variable `--aspect-ratio` to component `style`
- children: single DOM child
