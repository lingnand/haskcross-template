# haskcross-template

A stack template to quickly jumpstart cross platform haskell development.

Currently supported platforms:

- android: full support, immediate building/debuging on new project initiation
- linux/mac/windows: supported by stack

## Prerequisites

- stack: to use the template; also, building the project for PC platforms uses stack
- docker: needed for running the ghc-android image to build the app
- android sdk: an android sdk is needed to debug the app on your device. The `platform-tools` directory need to be in your `PATH` so that the tools inside can be invoked directly in the make script

## Usage

### Creating a new project

~~~
stack new <proj-name> https://raw.githubusercontent.com/lynnard/haskcross-template/master/haskcross.hsfiles
~~~

You can also clone this repository somewhere and point stack to use the local copy of the template.

### Building for Android

~~~
make -f android.mk configure
make -f android.mk build
~~~

To debug (make sure that your android phone is connected and in debug mode first)

~~~
make -f android.mk debug 
~~~

### Building for PC

~~~
stack build
~~~

Typical stack build as normal.
