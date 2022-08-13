**1.关于指针数组的使用**  
**1.The using of pointer in array**  
<br/>
<br/>
![1.1](https://github.com/knightsummon/My-CPP-learning-plan-notes/blob/main/2466453.jpg)  
```
Claim a pointer array  
double *pa[2],a[2][3];  
Putting the first address of a[0] and [1] to Pointer array pa[0] and pa[1]  

pa[0]=a[0];  //Equalling pa[0]=&a[0][0];
pa[1]=a[1];  //Equalling pa[1]=&a[1][0];
```  
<br/>
练习    
practice   
  
  
int a=1;
int *b=&a;

printf("%d/n",a);  \\1  
printf("%d/n",&a);  \\23145  
printf("%d/n",b);  \\23145  
printf("%d/n",*b);  \\1  

```
总结（Conclution)  
变量a 本质上代表一个存储单元。a本来代表两个值：存储单元的地址和储单元中的数据。  
Variable a is a storage unit, So a present two values: Address of storage unit and Data of storage unit.  
为了消除这种二义性，C语言规定a表示存储单元中的数据，&a表示存储单元的地址  
In order to eliminate anbiguity, C language specifies that a present the data of storage unit and Using &a to present the address of a  
a存储单元中的数据可以是一个普通数值，也可以是另一个存储单元的地址，比如：a = &b  
In a storage unit where can not only storage a data value, but also an address of another storage unit.  
指针本身也具有二义性  
Pointer also has ambiguity  
使用b表示指针的地址（指针指向哪里哪里就是它的地址),使用\*b来读取指针地址指向的值。
Using b present the address of pointer( Where pointer point, give pointer the same address),Using \*b to present what the data value of Pointer b(addresss)  
```
<br/>
<br/>
##2.指针与二维数组##   

<br/>  

![2.1](https://github.com/knightsummon/My-CPP-learning-plan-notes/blob/main/684255965171918649.jpg)  



