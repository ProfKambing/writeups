# Resource cache rat.
Not a common rat, but really dangerous. The only client i know that had this is renosense-beta made by zopac.

The 3 pastebins are still up and so are the downloads but the webhook's are nuked, so dont worry running old renosense beta.

## Investigating 
Thanks to [Sxmurai](https://github.com/Sxmurai/renosense-RATs) for providing these. The rat is located in CFont.java but the file is never used.

Zopac used bytes to avoid suspicion.

![bytes](https://cdn.upload.systems/uploads/stsyvbx7.png)

## Deep dive
After translating it, theres three pastebin link's (Which are still up).

How it works is it install INSTALLER.jar and it install CLIENT.jar then it rats the user by installing SERVER.jar.

All of this was done in resource cache so you wont even know that you gave zopac free alts.

## How to avoid
- Decompile and searches for keywords like "Bootstrap" since these ratters are smart.
- Don't run oyvey skids, only run clients that you trust.
- If you want to run it anyway, do it in a VM environment or offline.

big madlad zopac.
