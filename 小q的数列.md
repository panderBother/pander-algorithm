本题来自牛客网的[小q的数列](https://www.nowcoder.com/practice/8ea1e0d996f64e15961ae42e658a04a7?tpId=386&tags=&title=&difficulty=0&judgeStatus=0&rp=0&sourceUrl=%2Fexam%2Foj)（来源：牛客（newcoder））

> <img src="C:\Users\35543\AppData\Roaming\Typora\typora-user-images\image-20250729201846671.png" alt="image-20250729201846671" style="zoom:50%;" />

Java：

> 用的数一种数学方法来解题的，找规律会发现 展开式的结果就是 `x` 在二进制表示下所有位的值的总和。这恰好就是 `x` 的二进制表示中 1 的个数 ，而第一次出现的位置 数学表达式为 `2^c - 1`，这可以通过位运算 `(1 << c) - 1` 来实现。

```java
import java.util.Scanner;

// 注意类名必须为 Main, 不要有任何 package xxx 信息
public class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        // 注意 hasNext 和 hasNextLine 的区别
        int t=in.nextInt();
        while(t-->0){
            long x=in.nextLong();
            int c=Long.bitCount(x);
            long k=(1L<<c)-1;
            System.out.println(c+" "+k);
        }
    }
}
```



