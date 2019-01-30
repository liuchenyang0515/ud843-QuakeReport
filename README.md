lesson-three分支有Loader使用和处理有无网络连接的代码示例。

lesson-three笔记记录：
第一次运行到手机，调用方法onCreateLoader,EarthquakeLoader(这是构造方法),onStartLoading,loadInBackground,onLoadFinished.

1.按Home键，不变，再回到界面，回调onStartLoading->loadInBackground->onLoadFinished.

2.直接退出程序，在原生库回调onLoaderReset.在支持库不会回调onLoaderReset.

3.界面横屏，原生库只回调onLoadFinished.支持库不会回调onLoadFinished.

4.退出程序再进，回调onCreateLoader,EarthquakeLoader(这是构造方法),onStartLoading,loadInBackground,onLoadFinished.

5.进入下一个fragment，再返回到刚刚的界面

如果是在原生库中：onLoaderReset->onCreateLoader->EarthquakeLoader(构造)->onStartLoading->loadInBackground->onLoadFinished.

在支持库中：onCreateLoader->EarthquakeLoader(构造)->onStartLoading->loadInBackground->onLoadFinished.

可以看出在支持库中，onLoaderReset失去了行踪，但是还是必须实现。

确定和监控连接状态讲解官网：https://developer.android.google.cn/training/monitoring-device-state/connectivity-monitoring?utm_source=udacity&utm_medium=course&utm_campaign=android_basics
