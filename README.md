# About the solution

Passport MRZ Scanner enables camera to scan the MRZ code of a passport. It will extract all data like firstname, lastname, passport number, nationality, date of birth, expiration date and personal numer from the MRZ string, and converts the encoded string into human-readable fields. Welcome to visit dynamsoft's [official website](https://dynamsoft.com/capture-vision/docs/web/programming/javascript/user-guide/passport-mrz-scanner.html) to learn more about this solution.

## Web demo

The web demo is at [...]() (nothing is uploaded)

## Run this Solution

1. Clone the repo to a working directory

```sh
git clone https://github.com/Dynamsoft/passport-MRZ-scanner-javascript
```

2. CD to the folder and run a https server

```sh
cd passport-MRZ-scanner-javascript
```

> Basic Requirements
>
>  * Internet connection  
>  * [A supported browser](#system-requirements)
>  * An accessible Camera

-----

## Project structure

```text
Passport MRZ Scanner
├── assets
│   ├── ...
│   ├── ...
│   └── ...
├── css
│   └── index.css
├── font
│   ├── ...
│   ├── ...
│   └── ...
├── js
│   ├── define.js
│   ├── index.js
│   ├── init.js
│   └── util.js
├── index.html
└── template.json
```

 * `/assets` : This directory contains all the static files such as images, icons, etc. that are used in the project.
 * `/css` : This directory contains the CSS file(s) used for styling the project.
 * `/font` : This directory contains the font files used in the project.
 * `/js` : This directory contains all the JavaScript files used in the project.
   * `define.js` : This file contains definitions of certain constants or variables used across the project.
   * `index.js`: This is the main JavaScript file where the core logic of the project is implemented.
   * `init.js` : This file is used for initialization purposes, such as initializing license, load resources, etc.
   * `util.js` : This file contains utility functions that are used across the project.
 * `index.html` : This is the main HTML file that represents the homepage of the project.
 * `template.json` : This file contains a predefined templates used in the project.

# System Requirements

This project requires the following features to work:

* Secure context (HTTPS deployment)

  When deploying your application / website for production, make sure to serve it via a secure HTTPS connection. This is required for two reasons
  
  * Access to the camera video stream is only granted in a security context. Most browsers impose this restriction.
  > Some browsers like Chrome may grant the access for `http://127.0.0.1` and `http://localhost` or even for pages opened directly from the local disk (`file:///...`). This can be helpful for temporary development and test.
  
  * Dynamsoft License requires a secure context to work.

* `WebAssembly`, `Blob`, `URL`/`createObjectURL`, `Web Workers`

  The above four features are required for the SDK to work.

* `MediaDevices`/`getUserMedia`

  This API is only required for in-browser video streaming.

* `getSettings`

  This API inspects the video input which is a `MediaStreamTrack` object about its constrainable properties.

The following table is a list of supported browsers based on the above requirements:

  Browser Name | Version
  :-: | :-:
  Chrome | v61+<sup>1</sup>
  Firefox | v52+ (v55+ on Android/iOS<sup>1</sup>)
  Edge<sup>2</sup> | v16+
  Safari | v13+

  <sup>1</sup> iOS 14.3+ is required for camera video streaming in Chrome and Firefox or Apps using webviews.

  <sup>2</sup> On Edge, due to strict Same-origin policy, you must host the SDK files on the same domain as your web page.

  > Note: iOS 12 is currently not compatible with Dynamsoft Label Recognizer v 2.2.30+, due to certain technical limitations.

Apart from the browsers, the operating systems may impose some limitations of their own that could restrict the use of the SDK. Browser compatibility ultimately depends on whether the browser on that particular operating system supports the features listed above.