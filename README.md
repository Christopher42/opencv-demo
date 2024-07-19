# opencv-demo

Lightweight implementation of opencv in the browser with a number of example uses. Should be deployable via github pages.

## Decisions

### Stack

To be able to deploy via github pages, the application must completely avoid using any backend. This restricts usage of the openCV library to the js or web assembly (wasm) version - or requires an intermediate compiler that will just compile the whole thing down to one version or the other. From a user standpoint, a locally-ran instance with no capacity to export data to a backend aleviates a number of security concerns on how images from the camera may be used.

#### OpenCV.js

Rather than employing a framwork, as index.html with included javascript can load everything needed. It's not as pretty as a framework, but it's very simple and lightweight.

#### Shinylive

Shiny was originally developed to easily demonstrate the functionality of R code without requiring complex backend code. Shiny for Python extends this functionality to python code and shinylive neatly compiles down to wasm. The shiny framework is capable of producing some very elegant graphics, but this stack is pretty deep and seems overbuilt for this project. As python is the typical language for developing new ML algorithms, this stack could be useful if applied as a template for new repositories that provides a builtin lightweight demonstration with little implementation cost.

#### Web Assembly and Rust

I would likely chose this stack for a very robust production-grade implementation, if it was still desirable to avoid usage of a server.

## Versions

Using version 4.10.4 of opencv.js obtained from opencv-4.10.0-docs.zip on the offical release page. <https://github.com/opencv/opencv/releases>

## resources for further learning
- using OpenCV.js <https://docs.opencv.org/3.4/d0/d84/tutorial_js_usage.html>
