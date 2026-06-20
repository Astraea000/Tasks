# TCP服务端

`package main`

`import (`
    `"fmt"`
    `"net"`
`)`

`func main() {`
    `listener, _ := net.Listen("tcp", "127.0.0.1:8080")`
    `conn, _ := listener.Accept()`

    buf := make([]byte, 1024)
    n, _ := conn.Read(buf)
    fmt.Println("收到:", string(buf[:n]))
    conn.Write([]byte("收到!"))
`}`

#  TCP客户端

`package main`

`import (`
    `"fmt"`
    `"net"`
`)`

`func main() {`
    `conn, _ := net.Dial("tcp", "127.0.0.1:8080")`
    `conn.Write([]byte("你好"))`

    buf := make([]byte, 1024)
    n, _ := conn.Read(buf)
    fmt.Println(string(buf[:n]))
`}`



# HTTP服务端

`package main`

`import "net/http"`

`func main() {`
    `http.HandleFunc("/", func(w http.ResponseWriter, r *http.Request) {`
        `w.Write([]byte("收到!"))`
    `})`
    `http.ListenAndServe("127.0.0.1:9090", nil)`
`}`

# HTTP客户端

`package main`

`import (`
    `"fmt"`
    `"net/http"`
`)`

`func main() {`
    `resp, _ := http.Get("http://127.0.0.1:9090")`
    `buf := make([]byte, 1024)`
    `resp.Body.Read(buf)`
    `fmt.Println(string(buf))`
`}`