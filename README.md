<p align="center" >
  <img src="https://raw.githubusercontent.com/malcommac/SwiftSimplify/master/logo.png" width=200px height=205px alt="SwiftSimplify" title="SwiftSimplify">
</p>

[![CI Status](http://img.shields.io/travis/daniele margutti/SwiftSimplify.svg?style=flat)](https://travis-ci.org/daniele margutti/SwiftSimplify)
[![Version](https://img.shields.io/cocoapods/v/SwiftSimplify.svg?style=flat)](http://cocoapods.org/pods/SwiftSimplify)
[![License](https://img.shields.io/cocoapods/l/SwiftSimplify.svg?style=flat)](http://cocoapods.org/pods/SwiftSimplify)
[![Platform](https://img.shields.io/cocoapods/p/SwiftSimplify.svg?style=flat)](http://cocoapods.org/pods/SwiftSimplify)

<p align="center" >★★ <b>Star our github repository to help us!</b> ★★</p>

# SwiftSimplify
SwiftSimplify is a tiny high-performance Swift polyline simplification library ported from Javascript's [Simplify.js](http://mourner.github.io/simplify-js/). Original work come from [Leaflet](http://leafletjs.com/), a JS interactive maps library by [Vladimir Agafonkin](http://agafonkin.com/en).
It uses a combination of [Douglas-Peucker](http://en.wikipedia.org/wiki/Ramer-Douglas-Peucker_algorithm) and Radial Distance algorithms. Works both on browser and server platforms.

Polyline simplification dramatically reduces the number of points in a polyline while retaining its shape, giving a huge performance boost when processing it and also reducing visual noise. For example, it's essential when rendering a 70k-points line chart or a map route in the browser using MapKit.

![SwiftSimplify](https://raw.githubusercontent.com/malcommac/SwiftSimplify/master/screenshot.png)

## You also may like
-------

Do you like `SwiftRichString`? I'm also working on several other opensource libraries.

Take a look here:

* **[SwiftDate](https://github.com/malcommac/SwiftDate)** - Full features Dates & TimeZone management for iOS,macOS,tvOS and watchOS
* **[Hydra](https://github.com/malcommac/Hydra)** - Promise, Async/Await on sterioids!
* **[SwiftLocation](https://github.com/malcommac/SwiftLocation)** - CoreLocation and Beacon Monitoring on steroid!
* **[SwiftScanner](https://github.com/malcommac/SwiftScanner)** - String scanner in pure Swift with full unicode support
* **[SwiftSimplify](https://github.com/malcommac/SwiftSimplify)** - Tiny high-performance Swift Polyline Simplification Library
* **[SwiftMsgPack](https://github.com/malcommac/SwiftMsgPack)** - MsgPack Encoder/Decoder in Swit

## Requirements
* iOS 8.0+ / Mac OS X 10.10+
* Xcode 8.0
* Swift 3.0

## Communication
- If you **found a bug**, open an issue.
- If you **have a feature request**, open an issue.
- If you **want to contribute**, submit a pull request.

## Installation
SwiftSimplify is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "SwiftSimplify"
```
## Usage
Usage is pretty straightforward: in fact you need just call the SwiftSimplify's class method simplify by passing your configuration.
Allowed parameters are:
```swift
class func simplify<T:SimplifyValue>(points: [T], tolerance: Float?, highQuality: Bool = false) -> [T];
```
* ```points```: An array of points. SwiftSimplify supports Swift's generic so you can pass an array of SimplifyValue (```[SimplifyValue]```). 
* ```tolerance```: *(1 by default)* Affects the amount of simplification (in the same metric as the point coordinates)
* ```highQuality```: *(false by default)* Excludes distance-based preprocessing step which leads to highest quality simplification but runs ~10-20 times slower.

## Author

Daniele Margutti, [me@danielemargutti.com](mailto:me@danielemargutti)
You can reach me on twitter [@danielemargutti](http://www.twitter.com/danielemargutti). My web site is [danielemargutti.com](http://www.danielemargutti.com)

## License

SwiftSimplify is available under the MIT license. See the LICENSE file for more info.
