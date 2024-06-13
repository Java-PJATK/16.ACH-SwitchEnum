# 16.ACH-SwitchEnum
  
We will talk about enumerations later, but here we will just mention that for them the number of values is usually small, so we just have to ensure that they all have been taken into account:

### Listing 16 ACH-SwitchEnum/SwitchEnum.java Page 36  

```java
public class SwitchEnum {
    enum Country {FRANCE, GERMANY, MEXICO, CANADA, CHINA}

    public static void main(String[] args) {
        Country c = Country.CANADA;

        var continent = switch (c) {
            case FRANCE, GERMANY -> "Europe";
            case MEXICO, CANADA -> "America";
            case CHINA -> "Asia";
        };

        System.out.println("Continent: " + continent);
    }
}
