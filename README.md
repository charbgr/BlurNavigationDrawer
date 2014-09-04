Blur Navigation Drawer Library
=========================
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-BlurActionBarDrawerToggle-brightgreen.svg?style=flat)](https://android-arsenal.com/details/1/874)

Blur Navigation Drawer like Etsy app.

<img src="https://raw.githubusercontent.com/charbgr/BlurActionBarDrawerToggle/master/Screenshot/BlurActionDrawerToggleClosed.png"  height="480" width="300" />
<img src="https://raw.githubusercontent.com/charbgr/BlurActionBarDrawerToggle/master/Screenshot/BlurActionDrawerToggleOpened.png"  height="480" width="300" />


How to Use
==========

Declare your layout
```xml
<com.charbgr.BlurNavigationDrawer.library.BlurDrawerLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    app:blurRadius="19"
    app:downScaleFactor="8.0"
    app:drawerUpImageId="@drawable/ic_drawer"
    app:openDescription="@string/navigation_drawer_open"
    app:closeDescription="@string/navigation_drawer_close"
    ... >
```
Or replace your default toggle with this awesome blurred toggle effect just by adding 4 letters !

For example: 

```java
mDrawerToggle = new ActionBarDrawerToggle(
  getActivity(),                    /* host Activity */
  mDrawerLayout,                    /* DrawerLayout object */
  R.drawable.ic_drawer,             /* nav drawer image to replace 'Up' caret */
  R.string.navigation_drawer_open,  /* "open drawer" description for accessibility */
  R.string.navigation_drawer_close  /* "close drawer" description for accessibility */
);
```
to
```java
mDrawerToggle = new BlurActionBarDrawerToggle(
  getActivity(),                    /* host Activity */
  mDrawerLayout,                    /* DrawerLayout object */
  R.drawable.ic_drawer,             /* nav drawer image to replace 'Up' caret */
  R.string.navigation_drawer_open,  /* "open drawer" description for accessibility */
  R.string.navigation_drawer_close  /* "close drawer" description for accessibility */
);
```
and set your radius or your down scale factor
```java
mDrawerToggle.setRadius(15);
mDrawerToggle.setDownScaleFactor(6.0f);
```

and enjoy your blur effect!

Feel free to fork it and pull request if you want to fix a bug ! ;)

