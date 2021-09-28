# Revert String And Convert To Int

{% hint style="info" %}
Without using Integer.parseInt\(\), we can use **str.charAt\(i\) - '0'** to convert char to int.
{% endhint %}

```java
public class Main {
    public static int RevertStringAndConvertToInt(String str){
        int result = 0;
        for(int i = str.length() - 1; i >= 0; i--){
            //notice how to convert char to int without using Integer.parsInt
            //int temp = Integer.parseInt(Character.toString(str.charAt(i)));
            int temp = str.charAt(i) - '0';
            result = (result * 10) + temp;
        }
        return result;
    }
    
    public static void main(String[] args) {
        if(RevertStringAndConvertToInt("4321") == 1234)
            System.out.println("true");
    }
}
```

