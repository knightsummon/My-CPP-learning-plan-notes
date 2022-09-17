# switch 语句  
<br/>    

````
switch(expression){
    case constant-expression  :
       statement(s);
       break; /* 可选的 */
    case constant-expression  :
       statement(s);
       break; /* 可选的 */  
         
    default : /* 可选的 */
       statement(s);
}  
````    
  
case 的 constant-expression 必须与 switch 中的变量具有相同的数据类型，且必须是一个常量或字面量。
The constant-expression must have the same data type of the variables in switch.  
  
当被测试的变量等于 case 中的常量时，case 后跟的语句将被执行，直到遇到 break 语句为止。  
When the constant expression equals the value of the expression following the switch, the sentences following case wil be carry on, until meet a break closed to it.  

