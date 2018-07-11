# EasyLazyFragment
An lib make Fragment lazy load easy !

##Gradle 

----

Add the following to your `build.gradle` to use:

```
	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
	
	dependencies {
	   implementation 'com.github.chenguandong:EasyLazyFragment:version-1.0.0'
	}
```

## Usage

Usage1.Base 

```
public class DemoFragment extends LazyFragment {

    @Override
    protected void getData() {
    	//load your data  ↓

    }

}
```

Usage2.Loaded data once 

```
public class DemoFragment extends LazyFragment {
	//data loaded tag
	private boolean isLoaded;
	
    @Override
    protected void getData() {
    	
		if (!isLoaded){
            isLoaded = true;
            //load your data ↓
        }
    }

}
```

