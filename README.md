cesium-gradient
=========================


An elevation visualiser for [Cesium](https://cesiumjs.org/) acting as an imagery provider.  Elevation samples from a terrain provider are passed to a 2D WebGL renderer.  The renderer then applies a combination of the following algorithms:

* Colour ramp
* Hillshade
* Contour lines


Run the test app with a local server
------------------------------------
```
npm install
npm start
```
Then browse to [http://localhost:8080](http://localhost:8080)

Using in your app
-----------------
This code uses GLSL shaders.  It is currently set up to load them using [shader-loader for webpack](https://github.com/makio64/shader-loader).  If you happen to be using webpack on your project then you should be able to...

*  install shader-loader:
```
npm install shader-loader --save-dev
```
* set it up in your webpack.config.js:
```
module: {
    loaders: [{
        test: /\.(glsl|vs|fs)$/,
        loaders: ['shader']
    }]
}
```
* import (or require()) into your app
```
import ElevationGradientImageryProvider from '/lib/ElevationGradientImageryProvider'
```

