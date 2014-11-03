Blur Navigation Drawer Library
=========================
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-BlurNavigationDrawer-brightgreen.svg?style=flat)](https://android-arsenal.com/details/1/874)

Blur Navigation Drawer like Etsy app.

<img src="https://raw.githubusercontent.com/charbgr/BlurActionBarDrawerToggle/master/Screenshot/BlurActionDrawerToggleClosed.png"  height="480" width="300" />
<img src="https://raw.githubusercontent.com/charbgr/BlurActionBarDrawerToggle/master/Screenshot/BlurActionDrawerToggleOpened.png"  height="480" width="300" />

Demo
====
You can download a demo [here](https://play.google.com/store/apps/details?id=com.charbgr.BlurNavigationDrawer.sample.app).

Updates
=======
- Version 1.1
    * Add support for <b>v7</b> Android Support Library.

How to Use
==========

Declare your layout
```xml
<!-- If you don't use v7 support library include this:
    <com.charbgr.BlurNavigationDrawer.v4.BlurDrawerLayout
        app:drawerUpImageId="@drawable/ic_drawer
        ... > -->
    
<com.charbgr.BlurNavigationDrawer.v7.BlurDrawerLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    app:blurRadius="19"
    app:downScaleFactor="8.0"
    
    app:openDescription="@string/navigation_drawer_open"
    app:closeDescription="@string/navigation_drawer_close"
    app:toolbar="@+id/toolbarRef"
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

Contributing
============
Feel free to fork it and pull request if you want to fix a bug ! ;)

