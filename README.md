BlurActionBarDrawerToggle Library
=========================
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-BlurActionBarDrawerToggle-brightgreen.svg?style=flat)](https://android-arsenal.com/details/1/874)

Blur Navigation Drawer Toggle like Etsy app.

<img src="https://raw.githubusercontent.com/charbgr/BlurActionBarDrawerToggle/master/Screenshot/BlurActionDrawerToggleClosed.png"  height="480" width="300" />
<img src="https://raw.githubusercontent.com/charbgr/BlurActionBarDrawerToggle/master/Screenshot/BlurActionDrawerToggleOpened.png"  height="480" width="300" />





How to Use
==========

Just replace your default toggle with this awesome blurred toggle effect just by adding 4 letters !

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

then modify your layout to include a RelativeLayout around the drawer main frame:
```xml
<!-- This is the RelativeLayout that you must have for blur effect!-->

<RelativeLayout
    android:id="@+id/mylayout"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <!-- As the main content view, the view below consumes the entire
         space available using match_parent in both dimensions. -->
    <FrameLayout
        android:id="@+id/container"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />

</RelativeLayout>
```

and initialize BlurActionBarDrawerToggle with the RelativeLayout (working to fix this) passed as View and a blur radius.
```java
mDrawerToggle.init(getActivity().findViewById(R.id.mylayout), 10);
```

and enjoy your blur effect!

Feel free to fork it and pull request if you want to fix a bug ! ;)

