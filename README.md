+ `/Users/kingsonwu/programming/java-src/gradle-8.4/bin/gradle  init  -Dorg.gradle.java.home=/Users/kingsonwu/programming/java-src/jdk-21.jdk/Contents/Home`
+ `/Users/kingsonwu/programming/java-src/gradle-8.4/bin/gradle  build  -Dorg.gradle.java.home=/Users/kingsonwu/programming/java-src/jdk-21.jdk/Contents/Home`

## graalvm install
+ https://www.graalvm.org/downloads/
+ https://www.graalvm.org/latest/docs/getting-started/
+ HelloWorld 在macos编译出二进制文件，结果是7.2M


## spring boot
+ https://start.spring.io/

+ https://spring.io/blog/2023/09/09/all-together-now-spring-boot-3-2-graalvm-native-images-java-21-and-virtual
+ You can run the program as usual: ./gradlew bootRun. And it's using Project Loom! But for the real fun stuff: let's build a GraalVM native image! ./gradlew nativeCompile. This might take a minute or two.
+ Once it's done, you can run the native binary in the build directory: ./build/native/nativeCompile/demo.
+ ./gradlew bootRun -Dorg.gradle.java.home=/Users/kingsonwu/programming/java-src/jdk-21.jdk/Contents/Home
+ export JAVA_HOME=/Users/kingsonwu/programming/java-src/jdk-21.jdk/Contents/Home
+ export JRE_HOME=$JAVA_HOME/jre
+ export CLASSPATH=.:$JAVA_HOME/lib:$JRE_HOME/lib:$CLASSPATH
+ export PATH=$PATH:$JAVA_HOME/bin
+ export PATH=$PATH:/Users/kingsonwu/programming/java-src/graalvm-jdk-21.0.1+12.1/Contents/Home/bin
+ export GRAALVM_HOME=/Users/kingsonwu/programming/java-src/graalvm-jdk-21.0.1+12.1/Contents/Home
+ ./gradlew nativeCompile -Dorg.gradle.java.home=/Users/kingsonwu/programming/java-src/jdk-21.jdk/Contents/Home
+ [native-image-plugin] Native Image written to: /Users/kingsonwu/programming/java-src/graalvm_demo/app/build/native/nativeCompile
<pre>
ll -lh
total 153696
-rwxr-xr-x@ 1 kingsonwu  staff    75M Oct 22 17:24 app
 ./app 
</pre> 

