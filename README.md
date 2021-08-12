# packaging-aar

This repo is base on [https://github.com/kezong/fat-aar-android](https://github.com/kezong/fat-aar-android "fat-aar-android") and fix bugs on gradle 7.0+ 

packaging multi modules to arr .

1.unzip localMaven.zip to root project path.

2.add classpath in your root build scritp file :

	buildscript {
	   
	    repositories {
	        maven { url uri('repo') }
	        ...
	    }
	    dependencies {
	        ...
	        classpath 'personal.nfl.packaging.aar:packaging-aar:+'
	    }
	}

3.add plugin in your main android library:

	apply plugin: 'packaging-aar'

4.add applicationId in your main android library:

	fataar {
	    ...
	    applicationId = 'your main android library packagename in AndroidManifest.xml'
	}
5.others 
 
	see https://github.com/kezong/fat-aar-android
