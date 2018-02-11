## 支持手表独立应用

出门问问想先在这里对所有一路支持、陪伴我们的Ticwear开发者致谢。现在Ticwatch的功能日益丰富，其中愈来愈多的功能可在手表端独立运行。我们下一步的大目标是全力支持和发展手表端独立应用以实现手表完全脱离手机独立运行，从而给用户带来更加无缝、流畅、无限制的体验。出门问问真诚地希望各位开发者能拥抱这个变化并与我们一道实现这个目标。

### 手表应用根据其独立性可划分为如下三种：
 - 手表端完全独立应用：此应用无需手机端应用即可独立地在手表上运行和操作；
 - 半独立应用： 此应用无需手机端应用，但在手表端只可实现部分功能；
 - 非独立应用：应用本身必须依赖手机端应用才可使用；
 
如果您的手表应用可在手表上完全或部分独立运行，请在您的手表apk包中的Manifest文件中定义一个新的meta-data，具体定义方式如下：

```
<application>
...
  <meta-data
    android:name="com.google.android.wearable.standalone"
    android:value="true" />
...
</application>
```
如果该应用是独立使用或者半独立的应用，则value值为true，反之，则置为false。

注：当您在开发者网站上提交应用时，该状态需和以上Manifest文件中定义的内容保持一致。
![standalone](http://developer.chumenwenwen.com/uploads/img/markdown/standalone_cn.jpg)


### 为什么要开发手表端独立应用
现阶段，Ticwatch的安卓用户可任意下载所有类别的应用，而iOS用户只能下载手表端独立应用。如果您能开发手表端独立应用，您将同时获取安卓和iOS用户，并为他们带来更顺畅的使用体验。

请注意：
上传手表端独立应用时只需上传手表apk,无需将手表apk包装至对应的手机apk包内。如果您之前已上传可在手表端独立运行的应用或表盘，请在您上传独立应用的更新版时依照上述方式操作以避免应用被错误归类。