这可能是历史上最简单的一道java面试题了。

题目很简单，完成代码，判断一个整数是否是奇数：

```java
public boolean isOdd(int i)

```



```java
public boolean isOdd(int i) {
    if (i % 2 == 1) {
        System.out.println("是奇数");
    } else {
        System.out.println("是偶数");
    }
}

```



```java
public boolean isOdd(int i) {
    if (i % 2 == 1) {
        return true;
    } else {
        return false;
    }
}

```



```java
public boolean isOdd(int i) {
    return i % 2 == 1;
}

```


```java
public boolean isOdd(int i) {
    return i % 2 == 1 || i % 2 == -1;
}

```



```java
public boolean isOdd(int i) {
    return i % 2 != 0;
}

```




```java
public boolean isOdd(int i) {
    return i >> 1 << 1 != i;
}

```



```java
public boolean isOdd(int i) {
    return (i & 1) == 1;
}

```


