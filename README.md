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

```
mDrawerToggle = new ActionBarDrawerToggle(
  getActivity(),                    /* host Activity */
  mDrawerLayout,                    /* DrawerLayout object */
  R.drawable.ic_drawer,             /* nav drawer image to replace 'Up' caret */
  R.string.navigation_drawer_open,  /* "open drawer" description for accessibility */
  R.string.navigation_drawer_close  /* "close drawer" description for accessibility */
);
```
to
```
mDrawerToggle = new BlurActionBarDrawerToggle(
  getActivity(),                    /* host Activity */
  mDrawerLayout,                    /* DrawerLayout object */
  R.drawable.ic_drawer,             /* nav drawer image to replace 'Up' caret */
  R.string.navigation_drawer_open,  /* "open drawer" description for accessibility */
  R.string.navigation_drawer_close  /* "close drawer" description for accessibility */
);
```
and initialize it with a RelativeLayout(working to fix this) passed as View and a blur radius.
```
mDrawerToggle.init(getActivity().findViewById(R.id.mylayout), 10);
```

and enjoy your blur effect!

Feel free to fork it and pull request if you want to fix a bug ! ;)

