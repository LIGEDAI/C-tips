
[Skip to content](https://github.com/LIGEDAI/C-tips/edit/main/README.md#start-of-content)

## Navigation Menu

[](https://github.com/)

-   [LIGEDAI](https://github.com/LIGEDAI)/
-   [C-tips](https://github.com/LIGEDAI/C-tips)

Type  /  to search

[](https://github.com/notifications)

![](https://avatars.githubusercontent.com/u/134901215?v=4)

-   [Code](https://github.com/LIGEDAI/C-tips)
-   [Issues](https://github.com/LIGEDAI/C-tips/issues)
-   [Pull requests](https://github.com/LIGEDAI/C-tips/pulls)
-   [Actions](https://github.com/LIGEDAI/C-tips/actions)
-   [Projects](https://github.com/LIGEDAI/C-tips/projects)
-   [Wiki](https://github.com/LIGEDAI/C-tips/wiki)
-   [Security](https://github.com/LIGEDAI/C-tips/security)
-   [Insights](https://github.com/LIGEDAI/C-tips/pulse)
-   [Settings](https://github.com/LIGEDAI/C-tips/settings)

# Editing README.md in C-tips

## Breadcrumbs

1.  [C-tips](https://github.com/LIGEDAI/C-tips/tree/main)

/

in

[main](https://github.com/LIGEDAI/C-tips/tree/main)

[Cancel changes](https://github.com/LIGEDAI/C-tips/blob/main/README.md)Commit changes...

-   Edit
    
-   Preview
    

Code 55% faster with GitHub Copilot

Indent modeSpacesTabs

Indent size248

Line wrap modeNo wrapSoft wrap

Editing README.md file contents

1

2

3

4

5

6

7

8

9

10

11

12

13

14

15

16

17

18

19

20

21

22

23

24

25

26

27

28

29

30

31

32

33

34

35

36

# C/C++的一些注意事项

## tips1 指针数组&数组指针

### 1.指针数组

#include <stdio.h>

int main()

{

char arr1[] = "abcdef";

char arr2[] = "hello world";

char arr3[] = "cuihua";

char* parr[10] = { arr1, arr2, arr3 }; //指针数组

printf("%s\n", parr[0]);

return 0;

}

指针数组是把多个指针，以数组的形式存储在内存中，数组中的每个元素都是一个地址，占有多个指针的存储空间，可以用[]来替代解引用的操作。

此处`parr[10]`是一个有三个元素的指针数组，其每一个元素储存了指向对应元素的地址。因为**可以用[]来替代解引用的操作**，所以最后输出的结果为abcdef

### 2.数组指针

数组指针是一个指针变量，占有内存中一个指针大小，存放着数组的地址，指向该数组arr。

  

#include <stdio.h>

int main()

{

int arr[]={1,2,3,4,5,6,7,8,9,10};

int (*p)[10]=&arr;

printf("%p ",p);

}

此处`p`是一个指针，指向储存`arr[10]`这个数组的地址，输出结果为`000000000062FDF0`（`arr[10]`数组的储存地址）

  

## tips2 数组和地址

(1)在 C/C++ 中，数组名本身可以表示数组的首地址，比如：

`int arr[5] = {10, 20, 30, 40, 50};`

`arr` 表示数组 `arr` 的首地址，等价于 `&arr[0]`。

`arr + 1`等价于`& arr[1]`

(2)`tx_buffer_ptr[i]` 其实等价于 `*(tx_buffer_ptr + i)`，即 `tx_buffer_ptr` 地址加上偏移量 `i` 后的内存位置。
 

## tips3 十六进制地址表示

嵌入式里一般用诸如`0x1200000`这样的十六进制数表示内存地址。对于`0x1200000`，`0x`表示十六进制（Hexadecimal）。`1200000`代表十六进制的数值。

  

Use  Control + Shift + m  to toggle the  tab  key moving focus. Alternatively, use  esc  then  tab  to move to the next interactive element on the page.

Attach files by  dragging & dropping,  selecting or pasting them.[](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

Editing C-tips/README.md at main · LIGEDAI/C-tips
