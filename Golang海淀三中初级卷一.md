### Golang中为了实现协程之间的同步，有几种常用的方法？
回答：老李偷懒

### C语言中如下函数会有问题吗？相同过程用Golang实现会不会有问题，为什么？
````
#include <stdio.h>
int *returnPointer();

int main(int argc, char *argv[])
{
    int *counter_pointer;
    counter_pointer = returnPointer();
    printf("counter_pointer = %p\r\n", counter_pointer);
    return 0;
}

int *returnPointer() {
    int counter = 1;
    return &counter;
}
````
````
package main

import (
	"fmt"
)

func main() {
	pointer := returnPointer()
	fmt.Printf("pointer addr=%p\r\n", pointer)
}

func returnPointer() (*int) {
	counter := 12
	return &counter
}

````
回答：老李偷懒

### Golang中的Context有几种，应用场景是什么？
回答：老李偷懒

### Golang中如何较为精确得（秒级）人肉控制另外一个协程的按时退出或取消执行？
回答：老李还是偷懒

### Golang中的interface是处于一种怎样的设计理念？你是怎么用的？
回答：你就说老李没用过

### 唠唠Golang中的error你平时是怎么用的，有没有找到比原生更好的处理方式？
回答：老李用过一个error包

### Golang中的Channel是什么？一般说来，分为哪几类？操作起来有什么区别？
回答：初级卷里这些真的都是非常初级的问题，要是连这个也答不出来，那就答不出来吧...
