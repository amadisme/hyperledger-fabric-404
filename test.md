there is a test about why pushing to git is so slow

changes after git add test.md

how upload a .md from other folder

be eager to prepare meeting material

10月25日14点31分


之前push出现这个问题：fatal: unable to access 'https://github.com/amadisme/hyperledger-fabric-404.git/': OpenSSL SSL_read: Connection was reset, errno 10054
估计就是因为流量没有走代理，不走代理==断网，擦

解决办法：
git config --global --unset http.proxy
git config --global --unset http.https://github.com.proxy

这不对啊，这个命令是取消了代理