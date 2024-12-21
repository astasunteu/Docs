# File structure

Grouping folders and files in both Android and iOS versions of the app, which are alphabetized by default.

## Application

### Android

The application class for getting context in any part of the code, use it to store the necessary data in the device memory, and to initialize libraries and set general display parameters for the application.

### iOS

System **Delegate** files which initialize the application, scene window and libraries.


## Components

Sets of custom reusable components and drawables in Android in the interface that are grouped relatively to a certain type like button, bar, input field etc.


## Data

Set of data, depending on the chosen architecture, in the form of models or viewmodels which are used respectively to retrieve and transmit data via API requests or other means, and to display formatted data in the interface.


## Extensions

Sets of methods for base classes like String, Integer and others for custom formatting or validations or for classes like View to extend the functionality of processing of tapping, displaying etc.


## Screens

Grouped files with screens as Activity, Fragment or ViewController that can be reused in different scenarios with different content, as well as Views or Adapters which are presented only on their respective screens.


## Services

Classes with a set of static methods for API requests and working with the internet, calendar and other data to modify and prepare them for displaying on screens.


## Styles

Classes or enumerations with a set of typography, colors, sizes, icons, images and text variables used throughout the application.


## System

Set of files which exist exclusively in iOS apps, storing property configuration list, sets of colors, icons and images, as well as other supporting system files like font etc.

In Android such files are stored in **manifests** and **res** folders.