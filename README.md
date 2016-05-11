vlc源代码
---

编译于2016年5月11号，git下来用android studio运行

add gradle.properties
```
keyStoreFile=/home/xxx/.android/debug.keystore
storealias=androiddebugkey
storepwd=android
```

vlc源代码编译
---

> 环境:Ubuntu 15.04

过了一年又来编译vlc，no zuo no die

如果正准备想自己编译，按我的方法编译，先看[官方编译文档](https://wiki.videolan.org/AndroidCompile)

编译步骤：
0. git clone https://code.videolan.org/videolan/vlc-android.git

- 添加环境变量，$ vi ~/.bashrc

```
export ANDROID_SDK=/home/xxx/Android/Sdk
export ANDROID_NDK=/home/xxx/Android/android-ndk-r11c
```

$ source ~/.bashrc

- 下载源码`git clone https://code.videolan.org/videolan/vlc-android.git`

- 编译

$ cd vlc-android
$ ./compile.sh
$ ./compile.sh release

**遇到错误(网络不行)时，去https://download.videolan.org/contrib/下载同名的安装名放在vlc-android/vlc/contrib/tarballs目录下**

- 导入`android studio`运行成功

> 注意事项：  
> 1. 不要在那等它自动下载，有时太慢了，直接`ctrl + c`，自己下载重启编译  
> 2. ndk用最新的版本  
> 3. 代码里有两处`ARMv5Debug`相关的被我注释了，如果你是自己编译的完整是不会报这个错误的，我有删除两个目录:vlc && android-headers  

Messages:
```
Information:Gradle tasks [:vlc-android:clean, :vlc-android:generateChromeARMv5DebugSources, :vlc-android:prepareChromeARMv5DebugUnitTestDependencies, :vlc-android:mockableAndroidJar, :vlc-android:generateChromeARMv5DebugAndroidTestSources, :vlc-android:assembleChromeARMv5Debug]
code:42fadbb
vlc:7c3d71b
:vlc-android:clean
:vlc-android:preBuild UP-TO-DATE
:vlc-android:preChromeARMv5DebugBuild UP-TO-DATE
:vlc-android:checkChromeARMv5DebugManifest
:api:preBuild UP-TO-DATE
:api:preReleaseBuild UP-TO-DATE
:api:compileReleaseNdk UP-TO-DATE
:api:compileLint
:api:copyReleaseLint UP-TO-DATE
:api:checkReleaseManifest
:api:preDebugAndroidTestBuild UP-TO-DATE
:api:preDebugBuild UP-TO-DATE
:api:preDebugUnitTestBuild UP-TO-DATE
:api:preReleaseUnitTestBuild UP-TO-DATE
:api:prepareComAndroidSupportAppcompatV72311Library UP-TO-DATE
:api:prepareComAndroidSupportSupportV42311Library UP-TO-DATE
:api:prepareReleaseDependencies
:api:compileReleaseAidl UP-TO-DATE
:api:compileReleaseRenderscript UP-TO-DATE
:api:generateReleaseBuildConfig UP-TO-DATE
:api:mergeReleaseShaders UP-TO-DATE
:api:compileReleaseShaders UP-TO-DATE
:api:generateReleaseAssets UP-TO-DATE
:api:mergeReleaseAssets UP-TO-DATE
:api:generateReleaseResValues UP-TO-DATE
:api:generateReleaseResources UP-TO-DATE
:api:mergeReleaseResources UP-TO-DATE
:api:processReleaseManifest UP-TO-DATE
:api:processReleaseResources
:api:generateReleaseSources
:api:incrementalReleaseJavaCompilationSafeguard UP-TO-DATE
:api:compileReleaseJavaWithJavac UP-TO-DATE
:api:extractReleaseAnnotations UP-TO-DATE
:api:mergeReleaseProguardFiles UP-TO-DATE
:api:packageReleaseRenderscript UP-TO-DATE
:api:packageReleaseResources UP-TO-DATE
:api:processReleaseJavaRes UP-TO-DATE
:api:transformResourcesWithMergeJavaResForRelease UP-TO-DATE
:api:transformClassesAndResourcesWithSyncLibJarsForRelease UP-TO-DATE
:api:mergeReleaseJniLibFolders UP-TO-DATE
:api:transformNative_libsWithMergeJniLibsForRelease UP-TO-DATE
:api:transformNative_libsWithSyncJniLibsForRelease UP-TO-DATE
:api:bundleRelease UP-TO-DATE
:axmlrpc:compileJava UP-TO-DATE
:axmlrpc:processResources UP-TO-DATE
:axmlrpc:classes UP-TO-DATE
:axmlrpc:jar UP-TO-DATE
:libvlc:preBuild UP-TO-DATE
:libvlc:preReleaseBuild UP-TO-DATE
:libvlc:compileReleaseNdk UP-TO-DATE
:libvlc:compileLint
:libvlc:copyReleaseLint UP-TO-DATE
:libvlc:checkReleaseManifest
:libvlc:prepareReleaseDependencies
:libvlc:compileReleaseAidl UP-TO-DATE
:libvlc:compileReleaseRenderscript UP-TO-DATE
:libvlc:generateReleaseBuildConfig UP-TO-DATE
:libvlc:mergeReleaseShaders UP-TO-DATE
:libvlc:compileReleaseShaders UP-TO-DATE
:libvlc:generateReleaseAssets UP-TO-DATE
:libvlc:mergeReleaseAssets UP-TO-DATE
:libvlc:generateReleaseResValues UP-TO-DATE
:libvlc:generateReleaseResources UP-TO-DATE
:libvlc:packageReleaseResources UP-TO-DATE
:libvlc:processReleaseManifest UP-TO-DATE
:libvlc:processReleaseResources
:libvlc:generateReleaseSources
:libvlc:incrementalReleaseJavaCompilationSafeguard UP-TO-DATE
:libvlc:compileReleaseJavaWithJavac UP-TO-DATE
:libvlc:extractReleaseAnnotations UP-TO-DATE
:libvlc:mergeReleaseProguardFiles UP-TO-DATE
:libvlc:packageReleaseRenderscript UP-TO-DATE
:libvlc:processReleaseJavaRes UP-TO-DATE
:libvlc:transformResourcesWithMergeJavaResForRelease UP-TO-DATE
:libvlc:transformClassesAndResourcesWithSyncLibJarsForRelease UP-TO-DATE
:libvlc:mergeReleaseJniLibFolders UP-TO-DATE
:libvlc:transformNative_libsWithMergeJniLibsForRelease UP-TO-DATE
:libvlc:transformNative_libsWithSyncJniLibsForRelease UP-TO-DATE
:libvlc:bundleRelease
:vlc-android:preChromeARMv5ReleaseBuild UP-TO-DATE
:vlc-android:preChromeARMv6fpuDebugBuild UP-TO-DATE
:vlc-android:preChromeARMv6fpuReleaseBuild UP-TO-DATE
:vlc-android:preChromeARMv6nofpuDebugBuild UP-TO-DATE
:vlc-android:preChromeARMv6nofpuReleaseBuild UP-TO-DATE
:vlc-android:preChromeARMv7DebugBuild UP-TO-DATE
:vlc-android:preChromeARMv7ReleaseBuild UP-TO-DATE
:vlc-android:preChromeARMv8DebugBuild UP-TO-DATE
:vlc-android:preChromeARMv8ReleaseBuild UP-TO-DATE
:vlc-android:preChromeMIPS64DebugBuild UP-TO-DATE
:vlc-android:preChromeMIPS64ReleaseBuild UP-TO-DATE
:vlc-android:preChromeMIPSDebugBuild UP-TO-DATE
:vlc-android:preChromeMIPSReleaseBuild UP-TO-DATE
:vlc-android:preChromeX86DebugBuild UP-TO-DATE
:vlc-android:preChromeX86ReleaseBuild UP-TO-DATE
:vlc-android:preChromeX86_64DebugBuild UP-TO-DATE
:vlc-android:preChromeX86_64ReleaseBuild UP-TO-DATE
:vlc-android:preVanillaARMv5DebugBuild UP-TO-DATE
:vlc-android:preVanillaARMv5ReleaseBuild UP-TO-DATE
:vlc-android:preVanillaARMv6fpuDebugBuild UP-TO-DATE
:vlc-android:preVanillaARMv6fpuReleaseBuild UP-TO-DATE
:vlc-android:preVanillaARMv6nofpuDebugBuild UP-TO-DATE
:vlc-android:preVanillaARMv6nofpuReleaseBuild UP-TO-DATE
:vlc-android:preVanillaARMv7DebugBuild UP-TO-DATE
:vlc-android:preVanillaARMv7ReleaseBuild UP-TO-DATE
:vlc-android:preVanillaARMv8DebugBuild UP-TO-DATE
:vlc-android:preVanillaARMv8ReleaseBuild UP-TO-DATE
:vlc-android:preVanillaMIPS64DebugBuild UP-TO-DATE
:vlc-android:preVanillaMIPS64ReleaseBuild UP-TO-DATE
:vlc-android:preVanillaMIPSDebugBuild UP-TO-DATE
:vlc-android:preVanillaMIPSReleaseBuild UP-TO-DATE
:vlc-android:preVanillaX86DebugBuild UP-TO-DATE
:vlc-android:preVanillaX86ReleaseBuild UP-TO-DATE
:vlc-android:preVanillaX86_64DebugBuild UP-TO-DATE
:vlc-android:preVanillaX86_64ReleaseBuild UP-TO-DATE
:vlc-android:prepareComAndroidDatabindingAdapters11Library
:vlc-android:prepareComAndroidDatabindingLibrary11Library
:vlc-android:prepareComAndroidSupportAppcompatV72311Library
:vlc-android:prepareComAndroidSupportCardviewV72311Library
:vlc-android:prepareComAndroidSupportDesign2311Library
:vlc-android:prepareComAndroidSupportLeanbackV172311Library
:vlc-android:prepareComAndroidSupportPercent2311Library
:vlc-android:prepareComAndroidSupportPreferenceLeanbackV172311Library
:vlc-android:prepareComAndroidSupportPreferenceV142311Library
:vlc-android:prepareComAndroidSupportPreferenceV72311Library
:vlc-android:prepareComAndroidSupportRecyclerviewV72311Library
:vlc-android:prepareComAndroidSupportSupportV42311Library
:vlc-android:prepareVlcApiUnspecifiedLibrary
:vlc-android:prepareVlcLibvlcUnspecifiedLibrary
:vlc-android:prepareChromeARMv5DebugDependencies
:vlc-android:compileChromeARMv5DebugAidl
:vlc-android:compileChromeARMv5DebugRenderscript
:vlc-android:generateChromeARMv5DebugBuildConfig
:vlc-android:generateChromeARMv5DebugResValues
:vlc-android:generateChromeARMv5DebugResources
:vlc-android:mergeChromeARMv5DebugResources
:vlc-android:dataBindingProcessLayoutsChromeARMv5Debug
:vlc-android:mergeChromeARMv5DebugShaders
:vlc-android:compileChromeARMv5DebugShaders
:vlc-android:generateChromeARMv5DebugAssets
:vlc-android:mergeChromeARMv5DebugAssets
:vlc-android:processChromeARMv5DebugManifest
/home/yf/workspace/app0b-20160505/vlc/vlc-android/flavors/chrome/AndroidManifest.xml:42:5-95 Warning:
	uses-permission#android.permission.READ_PHONE_STATE was tagged at AndroidManifest.xml:42 to remove other declarations but no other declaration present
:vlc-android:processChromeARMv5DebugResources
:vlc-android:generateChromeARMv5DebugSources
:vlc-android:preChromeARMv5DebugUnitTestBuild UP-TO-DATE
:vlc-android:prepareChromeARMv5DebugUnitTestDependencies
:vlc-android:mockableAndroidJar UP-TO-DATE
:vlc-android:preChromeARMv5DebugAndroidTestBuild UP-TO-DATE
:vlc-android:prepareChromeARMv5DebugAndroidTestDependencies
:vlc-android:compileChromeARMv5DebugAndroidTestAidl
:vlc-android:processChromeARMv5DebugAndroidTestManifest
:vlc-android:compileChromeARMv5DebugAndroidTestRenderscript
:vlc-android:generateChromeARMv5DebugAndroidTestBuildConfig
:vlc-android:generateChromeARMv5DebugAndroidTestResValues
:vlc-android:generateChromeARMv5DebugAndroidTestResources
:vlc-android:mergeChromeARMv5DebugAndroidTestResources
:vlc-android:dataBindingProcessLayoutsChromeARMv5DebugAndroidTest
:vlc-android:mergeChromeARMv5DebugAndroidTestShaders
:vlc-android:compileChromeARMv5DebugAndroidTestShaders
:vlc-android:generateChromeARMv5DebugAndroidTestAssets
:vlc-android:mergeChromeARMv5DebugAndroidTestAssets
:vlc-android:processChromeARMv5DebugAndroidTestResources
:vlc-android:generateChromeARMv5DebugAndroidTestSources
:vlc-android:dataBindingExportBuildInfoChromeARMv5Debug
:vlc-android:incrementalChromeARMv5DebugJavaCompilationSafeguard
:vlc-android:compileChromeARMv5DebugJavaWithJavac
/home/yf/workspace/app0b-20160505/vlc/vlc-android/src/org/videolan/vlc/gui/helpers/UiTools.java
Error:(145, 24) 警告: Application namespace for attribute bind:alignMode will be ignored.
/home/yf/workspace/app0b-20160505/vlc/vlc-android/src/org/videolan/vlc/gui/helpers/AsyncImageLoader.java
Error:(127, 24) 警告: Application namespace for attribute bind:imageUri will be ignored.
Error:(127, 24) 警告: Application namespace for attribute bind:binding will be ignored.
Error:(144, 24) 警告: Application namespace for attribute bind:mediaWithArt will be ignored.
Error:(157, 24) 警告: Application namespace for attribute bind:media will be ignored.
Error:(165, 24) 警告: Application namespace for attribute bind:item will be ignored.
Error:(193, 24) 警告: Application namespace for attribute bind:media will be ignored.
Error:(193, 24) 警告: Application namespace for attribute bind:binding will be ignored.
警告: Method references using '.' is deprecated. Instead of 'holder.onClick', use 'holder::onClick'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/video_list_card.xml Line:51
警告: Method references using '.' is deprecated. Instead of 'holder.onMoreClick', use 'holder::onMoreClick'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/video_list_card.xml Line:101
警告: Method references using '.' is deprecated. Instead of 'holder.onClick', use 'holder::onClick'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/list_item.xml Line:25
警告: Method references using '.' is deprecated. Instead of 'holder.onClick', use 'holder::onClick'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/list_item.xml Line:35
警告: Method references using '.' is deprecated. Instead of 'holder.onClick', use 'holder::onClick'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/video_grid_card.xml Line:52
警告: Method references using '.' is deprecated. Instead of 'holder.onMoreClick', use 'holder::onMoreClick'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/video_grid_card.xml Line:104
警告: Method references using '.' is deprecated. Instead of 'holder.onClick', use 'holder::onClick'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/extension_item_view.xml Line:21
警告: Method references using '.' is deprecated. Instead of 'handler.onCancel', use 'handler::onCancel'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/vlc_login_dialog.xml Line:79
警告: Method references using '.' is deprecated. Instead of 'handler.onLogin', use 'handler::onLogin'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/vlc_login_dialog.xml Line:89
警告: Method references using '.' is deprecated. Instead of 'holder.onClick', use 'holder::onClick'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/directory_view_item.xml Line:33
警告: Method references using '.' is deprecated. Instead of 'holder.onCheckBoxClick', use 'holder::onCheckBoxClick'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/directory_view_item.xml Line:53
警告: Method references using '.' is deprecated. Instead of 'holder.onMoreClick', use 'holder::onMoreClick'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/directory_view_item.xml Line:107
警告: Method references using '.' is deprecated. Instead of 'holder.onClick', use 'holder::onClick'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/playlist_item.xml Line:27
警告: Method references using '.' is deprecated. Instead of 'holder.onMoreClick', use 'holder::onMoreClick'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/playlist_item.xml Line:78
警告: Method references using '.' is deprecated. Instead of 'handler.onCancel', use 'handler::onCancel'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/vlc_progress_dialog.xml Line:35
警告: Method references using '.' is deprecated. Instead of 'handler.onCancel', use 'handler::onCancel'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/vlc_question_dialog.xml Line:29
警告: Method references using '.' is deprecated. Instead of 'handler.onAction1', use 'handler::onAction1'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/vlc_question_dialog.xml Line:40
警告: Method references using '.' is deprecated. Instead of 'handler.onAction2', use 'handler::onAction2'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/vlc_question_dialog.xml Line:51
警告: Method references using '.' is deprecated. Instead of 'handler.onMoreClick', use 'handler::onMoreClick'
  file:///home/yf/workspace/app0b-20160505/vlc/vlc-android/res/layout/audio_browser_item.xml Line:91
注: 某些输入文件使用或覆盖了已过时的 API。
注: 有关详细信息, 请使用 -Xlint:deprecation 重新编译。
注: 某些输入文件使用了未经检查或不安全的操作。
注: 有关详细信息, 请使用 -Xlint:unchecked 重新编译。
27 个警告
:vlc-android:compileChromeARMv5DebugNdk UP-TO-DATE
:vlc-android:compileChromeARMv5DebugSources
:vlc-android:buildInfoChromeARMv5DebugLoader
:vlc-android:transformClassesWithExtractJarsForChromeARMv5Debug
:vlc-android:transformClassesWithInstantRunVerifierForChromeARMv5Debug
:vlc-android:transformClassesWithJavaResourcesVerifierForChromeARMv5Debug
:vlc-android:mergeChromeARMv5DebugJniLibFolders
:vlc-android:transformNative_libsWithMergeJniLibsForChromeARMv5Debug
:vlc-android:processChromeARMv5DebugJavaRes
:vlc-android:transformResourcesWithMergeJavaResForChromeARMv5Debug
:vlc-android:transformResourcesAndNative_libsWithJavaResourcesVerifierForChromeARMv5Debug
:vlc-android:transformClassesWithInstantRunForChromeARMv5Debug
:vlc-android:transformClasses_enhancedWithInstant+reloadDexForChromeARMv5Debug
:vlc-android:incrementalChromeARMv5DebugTasks
:vlc-android:prePackageMarkerForChromeARMv5Debug
:vlc-android:fastDeployChromeARMv5DebugExtractor
:vlc-android:generateChromeARMv5DebugInstantRunAppInfo
:vlc-android:coldswapKickerChromeARMv5Debug
:vlc-android:transformClassesWithInstantRunSlicerForChromeARMv5Debug
:vlc-android:transformClassesWithDexForChromeARMv5Debug
To run dex in process, the Gradle daemon needs a larger heap.
It currently has approximately 949 MB.
For faster builds, increase the maximum heap size for the Gradle daemon to more than 2048 MB.
To do this set org.gradle.jvmargs=-Xmx2048M in the project gradle.properties.
For more information see https://docs.gradle.org/current/userguide/build_environment.html
:vlc-android:validateDebugSigning
:vlc-android:packageChromeARMv5Debug
:vlc-android:zipalignChromeARMv5Debug
:vlc-android:fullChromeARMv5DebugBuildInfoGenerator
:vlc-android:luaMetaCopy UP-TO-DATE
:vlc-android:luaPlaylistCopy UP-TO-DATE
:vlc-android:assembleChromeARMv5Debug
Information:BUILD SUCCESSFUL
Information:Total time: 39.977 secs
Information:8 errors
Information:0 warnings
Information:See complete output in console
```

参考：
http://xuie0000.com/2015/11/01/ubuntu-15-04-%E7%BC%96%E8%AF%91Android-VLC/
https://wiki.videolan.org/AndroidCompile
https://download.videolan.org/contrib/
http://stackoverflow.com/questions/33021089/compiling-vlc-android-ubuntu
