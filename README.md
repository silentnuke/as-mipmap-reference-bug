# Android Studio mipmap reference bug
https://issuetracker.google.com/issues/157498440

1. Create a `drawables.xml` which defines a new mipmap reference.
```
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <item name="ic_launcher_foreground" type="mipmap">@mipmap/ic_launcher_foreground_en</item>
</resources>
```
2. Reference `@mipmap/ic_launcher_foreground` somewhere in xml. Android Studio shows an error `cannot resolve symbol reference`, even though everything works, compiles and runs successfully. Also, if you change reference `type` from `mipmap` to `drawable` and then reference as drawable `@drawable/ic_launcher_foreground` AS doesn't show any error. This happens only for mipmap as far as I see.  
![issue](https://raw.githubusercontent.com/silentnuke/as-mipmap-reference-bug/master/screens/as.png)
