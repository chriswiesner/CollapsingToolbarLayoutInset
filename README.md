# CollapsingToolbarLayoutInset

Demo App for showing a bug/side-effect of CollapsingToolbarLayout adding insets when height is set to `wrap_content`

Most likely this behaviour is a side-effect of this commit https://github.com/aosp-mirror/platform_frameworks_support/commit/d1a3eb935cfb5deac478ac26860bcff54b21bc22#diff-1f0f6187bf553656dde3f1fb5acf3c30

This appears if the CollapsingToolbarLayout's height is set to wrap content and the content of the Toolbar has set `android:fitsSystemWindows="true"` .

See sample image below

![Image of Bug](doc/inset_bug.png)


As soon the CollapsingToolbarLayout has a fixed height, the issue is gone. But this approach is not always applicable

![Image of Bug](doc/fixed_inset.png)
