完整版dns64:see more[ c-only Version](https://github.com/BMEI1314/dns64)

**实现dnsquery**

**1.输入：**
         A:查询域名
         B:超时时间
         C:dns服务器
 
 
**2.输出：**
        保存到结构体_ipinfo ：                     size           ip个数
                                            v4_addr        解析ipv4地址
                                            v6_addr        解析ipv6 地址
                                            
                                            
**3.原理：**
              1.判断自己的ip_stack
                                    if(ipv4_stack)   ipv4封装dns报文
                                    if(ipv6_stack_only)    ipv6封装dns报文
                2.解析返回的包（默认发一次收一次连续三次，某次成功break）
**4.功能**
            1.支持ipv4，ipv6
             2.输入dns64服务器，返回合成ipv4-mapped ipv6 addr

**5.结果**
 ![](./dnsquery/img/dnsquery.png)
