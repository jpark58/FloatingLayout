# FloatingLayout

The FloatingLayout enables you to drag and drop the whole layout on the screen. This layout inherits all features of Constranint Layout. 

## How to use

1. Add the JitPack repository to your build file.

   ```xml
   allprojects {
   		repositories {
   			...
   			maven { url 'https://jitpack.io' }
   		}
   	}
   ```

2. Add the dependency

   ```xml
   dependencies {
   	        implementation 'com.github.jpark58:FloatingLayout:1.0.0'
   	}
   ```

## Example Usage

Include the FloatingLayout in the layout that you want to use.

```xml
// In your main layout
<com.example.floatingview.FloatingLayout
        android:layout_width="200dp"
        android:layout_height="200dp"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:setLayout="@layout/item"
        android:background="#ffd581"
        >
    </com.example.floatingview.FloatingLayout>
```

**Important:** you need to specifiy *app:setLayout="@layout/item"*

So, basically, the item layout will contain your own layout/view or whatever you want to call it. 

```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout 
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    xmlns:app="http://schemas.android.com/apk/res-auto">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="This is in the layout!!!"
        android:textColor="@color/black"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintBottom_toBottomOf="parent"/>

</androidx.constraintlayout.widget.ConstraintLayout>
```

![](https://user-images.githubusercontent.com/48766032/111488261-6ed3c980-877c-11eb-93b2-b12aae913e7f.gif)

![](https://user-images.githubusercontent.com/48766032/112371067-88978280-8d21-11eb-80e3-7b49153da2b2.gif)