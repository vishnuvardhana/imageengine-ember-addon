# ImageEngine

[ImageEngine](https://web.wurfl.io/?utm_source=npmjs.com&utm_medium=page&utm_term=ember-addon&utm_campaign=ember-addon#image-engine) is an intelligent image CDN for optimizing, compressing and resizing images. ImageEngine will enhance your responsive images by enabling support for HTTP2, automatic webp conversion, Client Hints and more.

It is likely that ImageEngine will shave off 50-60% of data traffic generated by images on your site. To better support mobile devices, ImageEngine relies on WURFL for server side device detection in cases where responsive images and Client Hints fall short.

[Registration](https://scientiamobile.com/imageengine/signup?utm_source=npmjs.com&utm_medium=page&utm_term=ember-addon&utm_campaign=ember-addon#imageengine-lite) is required to get the most out of ImageEngine. There is both a completely [free option, and a commercial option](http://www.scientiamobile.com/page/imageengine?utm_source=npmjs.com&utm_medium=page&utm_term=ember-addon&utm_campaign=ember-addon). 

Images weight is by far the most important challenge to address when optimizing a web page for the plethora of devices on the web today. This is why ImageEngine will instantly give your users a better experience by reducing load time of your page. Not to mention the reduced data cost.

ImageEngine works as a CDN proxy. By referencing the ImageEngine servers and providing the full URL to the original image as a parameter, ImageEngine will identify the device, and its capabilities, and resize and optimize the image accordingly.

## Client Hints

The plugin will enable Client Hint support for your site. Client Hints, with information about the viewport size, device pixel ratio and actual image size, are added to the image request (HTTP header) enabling ImageEngine to resize the image with surgical precision.

## HTTP2 support

HTTP will give additional performance improvement on the network level. ImageEngine supports HTTP2 over SSL, which means that if you serve your sites and images by `https://`, ImageEngine will automatically serve all images over HTTP2.

## WebP

WebP is a lightweigh image format with great quality. WebP is well supported by browsers. ImageEngine will detect if the end user's browser supports WebP and automatically convert any format to WebP to increase performance.

## Installation

* `npm i ember-addon-imageengine --save` this repository

## Setup

In order to use the addon you need to [register](https://scientiamobile.com/imageengine/signup?utm_source=npmjs.com&utm_medium=page&utm_term=ember-addon&utm_campaign=ember-addon#imageengine-lite) to obtain your personal token.

	* In the build/environment.js file in your ember-cli project
	* Add this object to your EmberENV variable
	* ImageEngine:{
        token:"Your-Token-Goes-Here",
        is_lite:(true - if you are using only lite version , default:false)
      }



## Usage

* Basic usage `{{image-engine  ImgSrc="http://link-to-your-hosted-image.png" }}`

Check the [ImageEngine Documentation](https://docs.scientiamobile.com/documentation/image-engine/image-engine-getting-started?utm_source=npmjs.com&utm_medium=page&utm_term=ember-addon&utm_campaign=ember-addon) for the list of available settings.

* Example : To set width and height of the image call ImageEngine with options w and h
`{{image-engine  ImgSrc="http://link-to-your-hosted-image.png"  w="100" h="100"}}`

* Example : {{image-engine ImgSrc="http://link-to-your-hosted-image.png"  w="200" h="200" m="letterbox" pc="300"}}


For more information on using ember-cli, visit [http://www.ember-cli.com/](http://www.ember-cli.com/)
