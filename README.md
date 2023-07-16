# install-multiple-java-versions-on-macos
Install and setup JAVA_HOME path for multiple java versions on MAC OS



1. How to check current java version.
   `java -version`
2. How to check current java home path.
    `$echo $JAVA_HOME` - Library/Java/JavaVirtualMachines/jdk-20.jdk/Contents/Home
3. java_home & JAVA_HOME

   `$echo $JAVA_HOME` - Library/Java/JavaVirtualMachines/jdk-20.jdk/Contents/Home

    `echo $JAVA_HOME` - /usr/libexec/java_home
4. Default java version.
    `$echo /usr/libexec/java_home`
5. How to install multiple java version on mac machine.
   ```
       export JAVA_HOME=`/usr/libexec/java_home -v <java version>`
   ```
6. how to check all java versions installed java versions
  `/usr/libexec/java_home -V` 
7. How to switch between java versions.
   `/usr/libexec/java_home -v <version>`
8. How to run a java command on specific java version,
 `/usr/libexec/java_home -v <version> --exec java <java command>`
9. How to change env variable for easy change of java version.
    ```
   vi ~/.zshrc or vi ~/.bash_profile
    press I or Insert
    add  alias setJDK11='export JAVA_HOME=`/usr/libexec/java_home -v 11`'
         alias setJDK20='export JAVA_HOME=`/usr/libexec/java_home -v 20`'
    esc
    :wq
    press enter
```
