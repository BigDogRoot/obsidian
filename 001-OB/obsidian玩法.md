
#map
个思路是等你有需求时再去找相应的插件/教程，比如说我现在只是轻度使用，用得比较多的就是admonition（好看的文本框，类似notion的callout）、advanced tables（用tab和enter快速创建表格）、auto link title（自动补全链接标题）、daily notes、easy typing（中英文间加空格，功能性字符无需切换输入法），再加上emoji和/图标快捷输入和双向链接


```mermaid
graph TD
    subgraph "Application Layer"
        HTTP[HTTP]
        FTP[FTP]
        SSH[SSH]
        DHCP[DHCP]
        DNS[DNS]
    end
    
    subgraph "Transport Layer"
        TCP[TCP]
        UDP[UDP]
    end
    
    subgraph "Network Layer"
        IP[IP]
    end
    
    subgraph "Link Layer"
        ETH[Ethernet or Wi-Fi]
    end
    
    HTTP --> TCP
    FTP --> TCP
    SSH --> TCP
    DHCP --> UDP
    DNS --> UDP
    
    TCP --> IP
    UDP --> IP
    
    IP --> ETH
    
    style HTTP fill:#e1f5fe
    style FTP fill:#e1f5fe
    style SSH fill:#e1f5fe
    style DHCP fill:#e1f5fe
    style DNS fill:#e1f5fe
    style TCP fill:#f3e5f5
    style UDP fill:#f3e5f5
    style IP fill:#e8f5e8
    style ETH fill:#fff3e0
```



试试同步再试试
我是PC端
[[Android手机远程同步]]
[[PC远程同步]]