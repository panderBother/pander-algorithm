[【模板】快速幂Ⅰ ‖ 整数](https://www.nowcoder.com/practice/3d624107a6904da1bd0e8c9c85e17167?tpId=386&tqId=11079132&sourceUrl=%2Fexam%2Foj%3FquestionJobId%3D10%26subTabName%3Donline_coding_page)（来源：牛客（newcoder））

![image-20250801215644342](C:\Users\35543\AppData\Roaming\Typora\typora-user-images\image-20250801215644342.png)

> ```java
> import java.io.*;
> import java.util.*;
> 
> public class Main {
> 
>     // 快速幂算法，计算 a^b % p
>     public static long modPow(long a, long b, long p) {
>         long ans = 1;  // 结果初始值为1
>         while (b > 0) {  // 当指数b大于0时循环
>             if ((b & 1) ==
>                     1) {  // 判断b的二进制最后一位是否为1（即b是否为奇数）
>                 ans = ans * a % p;  // 如果是奇数，将当前a乘到结果中，并取模p
>             }
>             a = a * a % p;  // a自乘（相当于a的平方、四次方、八次方...）
>             b >>= 1;  // b右移一位（相当于b = b / 2，去掉二进制最后一位）
>         }
>         return ans % p;  // 最终结果再取一次模（确保不超过p）
>     }
> 
>     public static void main(String[] args) throws IOException {
>         Scanner sc = new Scanner(System.in);
>         // 读取测试用例的数量
>         int T = sc.nextInt();
> 
>         // 遍历每组测试数据
>         for (int i = 0; i < T; i++) {
> 
>             long a = sc.nextLong();
>             long b = sc.nextLong();
>             long p = sc.nextLong();
> 
>             // 计算 a^b % p
>             long result = modPow(a, b, p);
> 
> 
>         }
>     }
> }
> 
> ```
>
> 