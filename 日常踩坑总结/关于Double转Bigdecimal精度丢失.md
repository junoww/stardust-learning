#### Double转Bigdecimal精度丢失

```java
public static void main(String[] args) {
		Double doubleValue = 0.01;
		BigDecimal a = new BigDecimal(doubleValue);
		BigDecimal b = BigDecimal.valueOf(doubleValue);
		BigDecimal c = new BigDecimal(doubleValue.toString());
		System.out.println(a);
		System.out.println(b);
		System.out.println(c);
	}
```

​		double类型直接new Bigdecimal会出现精度丢失的问题

###### 解决方案

1. 使用BigDecimal.valueOf()
2. 先将doule转为string

