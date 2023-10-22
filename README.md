1. 安装jdk21
2. 安装graalvm
3. 配置环境变量
    <pre>
    export JAVA_HOME=/path/to/jdk21/home
    export JRE_HOME=$JAVA_HOME/jre
    export CLASSPATH=.:$JAVA_HOME/lib:$JRE_HOME/lib:$CLASSPATH
    export GRAALVM_HOME=/path/to/graalvm/home
    export PATH=$PATH:$JAVA_HOME/bin
    export PATH=$PATH:$GRAALVM_HOME/bin
    </pre>
4. 运行： `./gradlew bootRun`
5. 打包二进制文件：`./gradlew nativeCompile`

