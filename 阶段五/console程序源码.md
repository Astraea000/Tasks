# console程序源码

`package main`

`import "fmt"`

`func main() {`

  `var a,b float64`

  `var res float64`

  `var num int`

  `var c,d,sum string`

  `fmt.Println("---简易数据计算及字符拼接程序---")`

  `fmt.Println("1.两数字相加")`

  `fmt.Println("2.两数字相减")`

  `fmt.Println("3.两数字相乘")`

  `fmt.Println("4.两数字相除")`

  `fmt.Println("5.两字符拼接")`

  `fmt.Println("请选择你需要的程序：")`

  `fmt.Scanln(&num)`

  `switch num {`

  `case 1,2,3,4:`

​    `fmt.Println("请输入两个数字：")`

​    `fmt.Scan(&a,&b)`

​    `switch num{`

  `case 1:`

​    `res=a+b`

​    `fmt.Printf("计算结果：%f",res)`

  `case 2:`

​    `res=a-b`

​    `fmt.Printf("计算结果：%f",res)`

  `case 3:`

​    `res=a*b`

​    `fmt.Printf("计算结果：%f",res)`

  `case 4:`

​    `res=a/b`

​    `fmt.Printf("计算结果：%f",res)`

  `}`

  `case 5:`

​    `fmt.Println("请输入两个字符串：")`

​    `fmt.Scan(&c,&d)`

​    `sum=c+d`

​    `fmt.Printf("拼接结果：%s",sum)`

  `default:`

​    `fmt.Println("输入无关选项！")`

`}`

`}`