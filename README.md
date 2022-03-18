# android_system_sign_file
安卓系统应用签名文件
清单文件配置：android:sharedUserId="android.uid.system"
将所需文件放置于同一文件夹中，所j需文件路径如下；
signapk.jar， 位置：out/host/linux-x86/framework/signapk.jar
platform.x509.pem，位置：build/target/product/security/platform.x509.pem
platform.pk8，位置：build/target/product/security/platform.pk8
若是Linux系统拷贝（也在Android源码中）；out/soong/host/Linux-x86/lib64/libconscrypt_openjdk_jni.so
以下命令在Linux系统中执行。
执行命令：java -Djava.library.path=. -jar signapk.jar platform.x509.pem platform.pk8 原来.apk  签名生成.apk
