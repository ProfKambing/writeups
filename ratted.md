# Resource cache rat.
not a common rat, but really dangerous. The only client i know that had this is renosense-beta made by zopac

The pastebins are terminated and the webhook is nuked, so dont worry running old renosense beta.

## Investigating 
thanks to [Sxmurai](https://github.com/Sxmurai/renosense-RATs) for providing these. The rat is located in CFont.java but the file is never used.
Zopac used bytes to avoid suspicion.
![bytes](https://antiaim.org/stsyvbx7)

## Deep dive
after translating it, theres one pastebin link (which is termed).
How it works is it install INSTALLER.jar and it install CLIENT.jar then it rats the user by installing SERVER.jar.
All of this was done in resource cache so you wont even know that you gave zopac free alts.

## How to avoid
- decompile and searches for keywords like "Bootstrap" since these ratters are smart.
- Dont run oyvey skids, only run clients that you trust.
- If you want to run it anyway, do it in a VM environment or offline.

big madlad zopac
