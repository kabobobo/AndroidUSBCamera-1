How to use

1��at project gradle add  maven { url 'http://raw.github.com/saki4510t/libcommon/master/repository/' }

allprojects {
    repositories {
        google()
        maven { url 'http://raw.github.com/saki4510t/libcommon/master/repository/' }
        jcenter()
    }
}
����������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������

2��at APP libs add aac
   how to add aac in libs
   look this link
   https://www.jianshu.com/p/75c145a5373e


����������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������
3��at APP gradle  add

    repositories {
        flatDir {
            dirs 'libs'
        }
    }
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }

����������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������
4��at APP gradle implementation add

    implementation (name: 'libusbcamera-release', ext: 'aar')
    api("com.serenegiant:common:2.12.4") {
        exclude module: 'support-v4'
    }

    
