# Java调用Unix本地so库
2. 1. 创建 testJNI 文件夹


<!--more-->


2. 新建 JavaJNI.java

```java
public class JavaJNI {
   	static {
   		System.load("/Users/khan/Desktop/testJNI/libHelloWorld.so");
   		//Unix系统下指定so库文件地址
   	}
   	public native static int get();
   	public native static void set(int i);
   	public static void main(String[] args) {
   		JavaJNI test = new JavaJNI();
   		test.set(123);
   		System.out.println("Helloworld!" + "\ti = " + test.get());
   	}
}
```

3. 将 JavaJNI.java 编译成 JavaJNI.class 字节码，并生成 JavaJNI.h 头文件

4. 新建 JavaJNI.c 文件
```c
#include "JavaJNI.h"
int i = 0;
JNIEXPORT jint JNICALL Java_JavaJNI_get(JNIEnv *env, jclass jc)
{
    return i;
}
JNIEXPORT void JNICALL Java_JavaJNI_set(JNIEnv *env, jclass jc, jint j)
{
    i = j;
}
```
5. 利用 JVM 自带的 jni.h 和 jni_md.h 编译生成 JavaJNI.o 文件，然后生成JavaJNI.so库文件

```shell
gcc -fPIC -D_REENTRANT -I/Library/Java/JavaVirtualMachines/jdk1.8.0_121.jdk/Contents/Home/include -I/Library/Java/JavaVirtualMachines/jdk1.8.0_121.jdk/Contents/Home/include/darwin -c JavaJNI.c
# 第一个目录是jni.h所在路径，第二个是jni_md.h所在路径
gcc -shared JavaJNI.o -o libHelloWorld.so
```

6. 运行JavaJNI
## 操作截图
![](https://ws3.sinaimg.cn/large/006tKfTcgy1fjx1us1l7aj31ck0qedi4.jpg)

## P.S.
mac查看JVM安装目录可以用 `/usr/libexec/java_home -V` 命令