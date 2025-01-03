# File structure

Grouping folders and files in both Android and iOS versions of the app, which are alphabetized by default.


## Content

[Application](#application)

[Components](#components)

[Data](#data)

[Envoy](#envoy)

[Extensions](#extensions)

[Localizations](#localizations)

[Screens](#screens)

[Services](#services)

[Styles](#styles)

[System](#system)


## Application

### Android

The application class for getting context in any part of the code, use it to store the necessary data in the device memory, and to initialize libraries and set general display parameters for the application.

### iOS

System **Delegate** files which initialize the application, scene window and libraries.


## Components

Sets of custom reusable components and Android drawables which are used more than 2 times in the separate interfaces and grouped relatively to a certain type like button, bar, input etc.


## Data

Sets of data in the form of `models` and optional `viewmodels` which are used respectively to retrieve and send data via API requests or other means, and to display formatted data in the interface.


## Envoy

Set of supporting classes as layers between `data` and `view`, which contain the logic for retrieving, processing and storage of prepared data by means of accessing the corresponding services. There is also a specific protocol with a set of methods that are delegated to the `view` layer to communicate with an envoy.


## Extensions

Sets of methods for base classes like String, Integer and others for custom formatting or validations or for classes like View to extend the functionality of processing of tapping, displaying etc.


## Localizations

Sets of localizable files in different languages with key-value pairs that are used throughout the application via the text styles layer.


## Screens

Grouped files with Activity, Fragment or ViewController screens that can be reused in different scenarios with different content, as well as Views or Adapters which are presented only on their respective screens.


## Services

Classes in the form of singletons or with a set of static methods for API requests and working with the internet, calendar and other data to modify and prepare them for displaying on screens.


## Styles

Classes or enumerations with a set of typography, colors, sizes, icons, images, text including localization used throughout the application.


## System

Set of files which exist exclusively in iOS apps, storing property configuration list, sets of colors, icons and images, as well as other supporting system files like font etc. In Android such files are stored in **manifests** and **res** folders.