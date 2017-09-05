[![Build Status](https://travis-ci.org/gecko0307/dagon.svg?branch=master)](https://travis-ci.org/gecko0307/dagon)
[![DUB Package](https://img.shields.io/dub/v/dagon.svg)](https://code.dlang.org/packages/dagon)
[![DUB Downloads](https://img.shields.io/dub/dt/dagon.svg)](https://code.dlang.org/packages/dagon)
[![License](http://img.shields.io/badge/license-boost-blue.svg)](http://www.boost.org/LICENSE_1_0.txt)

Dagon
=====
Dagon is a 3D/2D game development framework for D. It is a work-in-progress reincarnation of [DGL](https://github.com/gecko0307/dgl) with several architecture improvements. Surrently Dagon has the following features:

* Rendering static and animated meshes, loading OBJ and [IQM](https://github.com/lsalzman/iqm) formats
* Textures in PNG, JPG, TGA, BMP formats
* Flexible material system with simple abstract API and different backends (for example, fixed pipeline or GLSL-based). You can implement custom materials, with your own shaders and parameters
* UTF-8 text rendering using TTF fonts
* Shadow maps
* Particle system with force fields
* Ownership memory model - every object belongs to some object (owner), and deleting the owner will delete all of its owned objects. This allows semi-automatic memory management - you have to manually delete only root owners
* Entity-component model that allows game objects behave differently and combine many behaviours
* Scene management. Any scene has its own assets, entities and logical context
* Live asset reloading - asset can be autimatically reloaded when the file is modified with external application
* [Box](https://github.com/gecko0307/box) container support for assets.

Dagon is still under development and lacks a lot of important functionality. In future, some functionality from DGL will be ported to Dagon. Currently it is not recommended to use Dagon in production due to unstable API.

WIP features:

* Clustered forward shading
* Normal mapping and parallax mapping
* FXAA
* SSAO

Prerequisites
-------------
Dagon is based on OpenGL 1.3 + a number of common extensions, and should run virtually on any hardware. Currently we are not considering implementing OpenGL 3.x/4.x renderer or adding Vulkan support.

Dagon is known to work on Windows, Linux, FreeBSD and OSX.

To use Dagon, a number of libraries should be installed, namely SDL2 and Freetype. If you don't have them installed system-wide (which is a common case on Windows), you can use the libraries provided [here](https://github.com/gecko0307/dagon/releases/tag/v0.0.2). Currently we provide libraries only for Windows and Linux. Download an archive for your system and place the `lib` folder in your project's working directory. Dagon will automatically detect and try to load them. If there are no local libraries in `lib` directory, it will use system ones.

Demos
-----
A test application that demonstrates Dagon's features is hosted [here](https://github.com/gecko0307/dagon-demo). If you are starting from scratch, we recommend to use it for learning purposes.

Documentation
-------------
Not available yet, sorry.

License
-------
Copyright (c) 2016-2017 Timur Gafarov. Distributed under the Boost Software License, Version 1.0 (see accompanying file COPYING or at http://www.boost.org/LICENSE_1_0.txt).
