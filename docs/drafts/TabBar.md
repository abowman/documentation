A tab bar appears at the bottom of an app screen and provides the ability to quickly switch between different sections of an app. Tab bars are translucent, may have a background tint, maintain the same height in all screen orientations, and are hidden when a keyboard is displayed. A tab bar may contain any number of tabs, but the number of visible tabs varies based on the device size and orientation. If some tabs can’t be displayed due to limited horizontal space, the final visible tab becomes a More tab, which reveals the additional tabs in a list on a separate screen.

![TabBarr](images/tabbar1.png)
A `TabBar` with 4 child `Window`.

### Best practices
When an application has multiple sections then `TabBar` is usually the root screen and is used to present a clear interface to switch between the sections, ie:

- the sections of a social app: 1 screen for the feeds, 1 screen for the user profile, 1 for creating new posts and so on

- the sections of a navigator app: 1 screen for driving informations, 1 screen to explore your surrounding and 1 for the public transport

### How to use
1. add a `TabBar` as a root screen and customize the appearance, ie translucent, tint and so on
1. add 1 or more child `Window` or `Navigation`
1. for each childrencustomize its `TABBAR Item` by tapping the _(+)_ icon

#### Example
- start adding a `TabBar` by tapping the _New Navigation_ button on the _bottom bar_

![New TabBar](images/tabbar0.png)

- configure the `TabBar` by adding `Window` or `Navigation` child screens

- configure each screen to add a `TABBAR Item` 
- keep doing the same until you have a hierarchy like this

![New TabBar](images/tabbar5.png)

```
- TabBar
  - Navigation1 (startup window)  
    - TabBarItem1
    - Window1
  - Navigation2
    - TabBarItem1
    - Window2
  - Navigation3
    - TabBarItem1
    - Window3
```

**Note:**

it is common practice to drop `Navigation` as the child of a `TabBar` and configure the `Navigation Bar` setting `Hide Navigation Bar` to _true_.

#### Interacting using Gravity

`TABBAR Item` properties can be set by code, ie

```
Navigation1.TabbarItem1.badgeValue = "10"
```

### Subnodes
The `TABBAR Item` can be created by tapping the subnode icon _(+)_, the top settings include:

- A custom title
- A badge value
- An icon

The icon can both be custom (with a user provided image) or selected from the list of system _TabBar_ icons.
![System buttons](images/tabbar3.png)

**Note:** without the _TABBAR Item_ the title itself is automatically retrieved from the name of the current children `Window`.

### UI Properties
Several UI aspects can be configured but (see the inspector) but usually you want to set the `TabBar` tint color to match your ui

![Inspector](images/tabbar4.png)
