
<p align="center">
  Simple and beautiful portfolio item viewer for VueJS.
</p>

## Demo
Live demo of the component can be found [here.](https://vueportfolioviewer.netlify.app/)

## Installation
`npm i vue-portfolio-viewer`

## Usage

After the installation, the component can be used by passing the appropriate props for displaying the data and messages. A sample usage within a single file component is as follows:

```html
<template>
  <div>
    <PortfolioItem :img="require('../assets/logo.png')"
      href="clicklink"
	  borderColor ="#3f3f3f"
 />
  </div>
</template>

<script>
import PortfolioItem from "vue-portfolio-viewer/PortfolioItem"

export default {
  components: {
    PortfolioItem,
  },
};
</script>
```
### Props

There are basically three different props
The props are as follows:

| prop         | Type                | Optional? | Default                | Description                                                                                                                                                  |
|--------------|---------------------|--------------|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `img`  | `String`            | :x:         | `''`               | Image file url.                                                                                 |
| `borderColor` | `String`            | :white_check_mark:          | `#e74c3c` | Color of the border.                                                                                                                         |
| `href`  | `String` | :white_check_mark:           | `''` | External link |


## License
The project is under MIT License.