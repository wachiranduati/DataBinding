## DATABINDING
Data binding playground

## Intro
Databinding library is a support library that allows you to bind your UI with your data sources using a declarative format rather than programmatically.

The magic that comes about from this is taking code from this
```
findViewById<TextView>(R.id.sample_text).apply {
     text = viewModel.userName
 }
 ```

 ## TO

 ```
 <TextView
      android:text="@{viewmodel.userName}" />
      ```
right in your xml code

## To get Started
include the following declaration in your build.gradle file to enable databinding on your project

```
android {
     ...
     buildFeatures {
         dataBinding true
     }
 }
 ```

 with data binding you can use expression in the xml files that resemble something like
 ```
 android:text="@{String.valueOf(index + 1)}"
 android:visibility="@{age < 13 ? View.GONE : View.VISIBLE}"
 android:transitionName='@{"image_" + id}'
 ```
 ### Example 1 : Using Static Values
 ```
  <data>
         <variable name="name" type="String"/>
         <variable name="lastName" type="String"/>
     </data>
     ```

    ```
    <TextView
                    android:id="@+id/plain_name"
                    android:text="@{name}"
            ... />
            ```

 ### Reference

 - [DataBinding](https://developer.android.com/topic/libraries/data-binding)