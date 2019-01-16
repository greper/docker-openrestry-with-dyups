# docker-openrestry
编译安装openresty，构建docker镜像 ，并安装自定义模块:ngx_http_dyups_module


+  _**step1**_ 准备工作  
`安装docker、docker-compose`


+  _**step2**_ 构建镜像 
    >cd build  
    docker-compose build  
    docker-compose up -d

+  _**step3**_ 验证dyups效果  
    >curl http://127.0.0.1:48081/detail  

    >host1
    server 127.0.0.1:8088 weight=1 max_conns=0 max_fails=1 fail_timeout=10 backup=0 down=0  
    >
    >host2
    server 127.0.0.1:8089 weight=1 max_conns=0 max_fails=1 fail_timeout=10 backup=0 down=0
 