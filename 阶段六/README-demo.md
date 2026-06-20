## 一、程序用途

实现基础TCP、HTTP网络通信，完成服务端与客户端的数据收发交互。

## 二、程序功能

1. TCP服务端监听8080端口，接收客户端数据并返回应答消息
2. TCP客户端连接服务端，发送消息并接收服务端应答
3. HTTP服务端监听9090端口，响应所有GET请求并返回固定内容
4. HTTP客户端发起HTTP GET请求，读取并打印服务端响应数据

## 三、使用步骤

1. 打开终端，优先启动对应服务端程序，监听对应端口
2. 新开终端启动客户端程序，自动发起连接与请求
3. 查看终端打印内容，验证网络通信效果

## 四、相关知识点

`package main`：声明当前为可执行程序包

`func main()`：程序唯一入口函数，程序从这里开始执行

`import "fmt"`：导入标准输入输出包，用于控制台打印输出信息

`import "net"`：导入网络基础库，用于实现TCP服务监听、客户端拨号连接

`import "net/http"`：导入HTTP网络库，用于快速搭建HTTP服务、发起HTTP请求

`net.Listen()`：监听指定端口，创建TCP服务端监听器

`listener.Accept()`：阻塞等待，接收客户端TCP连接

`net.Dial()`：客户端拨号，建立TCP网络连接

`conn.Read() / conn.Write()`：TCP连接数据读取与数据发送

`http.HandleFunc()`：注册HTTP路由及请求处理函数

`http.ListenAndServe()`：启动HTTP服务，监听端口处理请求

`http.Get()`：客户端发起HTTP GET网络请求