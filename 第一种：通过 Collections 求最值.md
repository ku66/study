第一种：通过 `Collections` 求最值

```java
import java.util.Arrays;
import java.util.Collections;
 
public class Demo {
    public static void main(String[] args) {
        Integer[] numbers = { 8, 2, 7, 1, 4, 9, 5};
        int min = (int)Collections.min(Arrays.asList(numbers));
        int max = (int)Collections.max(Arrays.asList(numbers));
        System.out.println("最小值: " + min);
        System.out.println("最大值: " + max);
    }
}
```

第二种：将 `int` 数组转换成 `Integer`数组，通过 `Collections` 求最值

```java
/*数组中比较最值*/
import java.util.Arrays;
import java.util.Collections;

public class Demo{
    public static void main(String[] args) {
       int[] arr = {18,25,32,64,55};
       Integer[] numbers =new Integer[arr.length];
       for (int i = 0; i < arr.length; i++) {
            numbers[i]=arr[i];
        }
        int max = Collections.max(Arrays.asList(numbers));
        int min = Collections.min(Arrays.asList(numbers));
        System.out.println("最大值是："+max);
        System.out.println("最小值是："+min);
        }
    }
```

第三种：利用三元运算符求最值

```java
public class Demo{
    public static void main(String[] args) {
        int a = 1;
        int b = 2;
        int c = 3;
        int num = a>b?a:b;
        int max = num>c?num:c;
        System.out.println(max);
    }
}
```

第四种：利用 `if...else` 判断求最值

```java
public class Demo {
    public static void main(String[] args) {
        int a = 1;
        int b = 2;
        int c = 3;
        int max = a;
        if(max>b){
            System.out.println(max=a);
        }else if(max>c){
            System.out.println(max);
        }else{
            System.out.println(max=c);
        }
    }
}
```

第五种：求数组中的最大值（把max当成武林萌主，数组元素就是比萌的选手。依次遍历，就相当于选手轮番上场比萌。当有元素萌过萌主，那么这个元素就是新的萌主。但这只是暂时的，因为还要接受余下的其他选手挑战。只有笑到最后的那位选手，才是真正的萌主。而盟主就是最大值。）

```java
public class Demo {
    public static void main(String[] args) {
        int [] arr = {1,2,3};
        int max = arr[0];
        for (int i = 1; i<arr.length ;i++ ){
            if(arr[i] > max){
                max = arr[i];
            }
        }
        System.out.println(max);
    }
}
```

第六种：求集合中的最大值（把max当成武林萌主，集合元素就是比萌的选手。依次遍历集合，就相当于选手轮番上场比萌。当有元素萌过萌主，那么这个元素就是新的萌主。但这只是暂时的，因为还要接受余下的其他选手挑战。只有笑到最后的那位选手，才是真正的萌主。而盟主就是最大值。）

```Java
import java.util.ArrayList;
import java.util.List;

public class Demo {
    public static void main(String[] args) {
        ArrayList<Integer> list = new ArrayList<>(List.of(1, 2, 3));
        int max = list.get(0);
        for (int i = 0; i < list.size(); i++) {
            if(max<list.get(i)){
                max=list.get(i);
            }
        }
        System.out.println(max);
    }
}

```