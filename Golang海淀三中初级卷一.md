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