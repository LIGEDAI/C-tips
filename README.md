# C/C++的一些注意事项
## tips1 指针数组&数组指针
### 1.指针数组
    #include <stdio.h>
    int main()
    {
    	char arr1[] = "abcdef";
    	char arr2[] = "hello world";
    	char arr3[] = "cuihua";
        char* parr[] = { arr1, arr2, arr3 };  //指针数组
        printf("%s\n", parr[0]);
    	return 0;
    }
 指针数组是把多个指针，以数组的形式存储在内存中，数组中的每个元素都是一个地址，占有多个指针的存储空间，可以用[]来替代解引用的操作。
此处`parr[]`是一个有三个元素的指针数组，其每一个元素储存了指向对应元素的地址。因为**可以用[]来替代解引用的操作**，所以最后输出的结果为abcdef
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
