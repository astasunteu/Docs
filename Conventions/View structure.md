# View structure

Grouping code parts for View, Adapter, Fragment, Activity and ViewController classes in iOS and Android projects to organize variables and methods.

There is a complete list of groups that can be used in a View class, but it is also worth noting, most of them are optional and their presence depends on the specific class.


## Content

[Callbacks](#callbacks)

[Properties](#properties)

[Views](#views)

[Setup](#setup)

[Handlers](#handlers)

[Modifications](#modifications)

[Presentation](#presentation)

[Navigation](#navigation)

[Lifecycle](#lifecycle)


## Basics

Each group should be labeled in the code with an appropriate comment indicating the name of the group and subgroup if necessary.

```
// ********
// Group – subgroup
```

Each group is separated by 2 empty lines, within a group each method is separated by 1 empty line and variable or callbacks are grouped line by line.


## Groups

### Callbacks

Lambda methods which are called to notify parent view and pass data or states to it if necessary.

Name of methods may begin with a name of view or context of calling and should contain keywords like `clicked`, `tapped`, `switched`, `changed`, `selected` etc.


### Properties

Set of supporting **private** variables, including extras, data models and view models, which are used throughout the lifecycle of screen or component, and which are populated from the data that was passed via Intents to newly created Activity from another Fragment or Activity in Android.

Variables should be grouped under different comments, indicating the name of the subgroup.

```
// Properties – data, status, extras etc
```


### Views

Set of **private** views which are displayed permanently or temporarily on the screen or in a component, used and edited exclusively within the object in which they were created by calling available modification methods.

Name of views should contain keywords like `View`, `LinearLayout`, `StackView`, `Button` to point to the parent view, whether it is a default UI element or a custom-built one component.

If both permanent and temporary views are displayed on the screen, they should be separated into different subgroups.

```
// Views – permanent, temporary
```


### Setup

Set of **private** supporting methods for initializing the screen in general, extra and local variables and views that are always displayed on the screen or shown temporary.

The order of initialization methods always remains unchanged:

1. view or screen itself,
2. properties
3. other views.


### Handlers

Set of **private** methods to track changes in screen display, offsets or theme, and user interaction with views.

The methods are called when screen or component is initialized in the **setup** group.

Name of methods should be structure with leading `handle` keyword, following with the name of view and resulting with the action like `Click`, `Switch` or property which is observed like `Offset`, `Theme` etc.


### Modifications

Set of **private** and **public** methods for changing the content in displayed views and their appearance with passing corresponding parameters if needed.

Name of methods should start with keyword `set`, following with the name of property like `Title`, `Color`, `Icon` or display state like `Selected`, `Active` etc.


### Presentation

**Private** methods for controlling the display of both permanent and temporary views on the screen which can be either shown or hidden.

Name of the methods should begin with the keywords `show` and `hide` following with the name of the view.


### Navigation

**Private** methods which allow to navigate from the current screen to another screen, open page in the browser, or open another application.

Name of methods should begin with keywords `show` or `open` following with the name of the view or external application with context.


### Lifecycle

Standard **override** methods for monitoring screen or component display status when it appears, hides, etc., and to get data from other screens if needed.
