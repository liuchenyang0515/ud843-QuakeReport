lesson-three分支有Loader使用和处理有无网络连接的代码示例。

lesson-three笔记记录：
第一次运行到手机，调用方法onCreateLoader,EarthquakeLoader(这是构造方法),onStartLoading,loadInBackground,onLoadFinished.

1.按Home键，不变，再回到界面，回调onStartLoading,loadInBackground,onLoadFinished.

2.直接退出程序，回调onLoaderReset.

3.界面横屏，只回调onLoadFinished.

4.退出程序再进，回调onCreateLoader,EarthquakeLoader(这是构造方法),onStartLoading,loadInBackground,onLoadFinished.

确定和监控连接状态讲解官网：https://developer.android.google.cn/training/monitoring-device-state/connectivity-monitoring?utm_source=udacity&utm_medium=course&utm_campaign=android_basics
