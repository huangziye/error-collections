# 1. `Failed to execute goal org.apache.maven.plugins:maven-compiler-plugin:3.1:compile (default-compile) on project sdk: Fatal error compiling`

需要注释掉下面部分

```java
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-compiler-plugin</artifactId>
    <configuration>
        <source>1.6</source>
        <target>1.6</target>
        <encoding>UTF-8</encoding>
        <!--<compilerArguments>
            <verbose/>
            &lt;!&ndash; 下面这行添加jce.jar，注意它和rt.jar中间分隔符，window下是“;”，linux下是“:” &ndash;&gt;
            <bootclasspath>${java.home}/lib/rt.jar;${java.home}/lib/jce.jar</bootclasspath>
        </compilerArguments>-->
    </configuration>
</plugin>
```
