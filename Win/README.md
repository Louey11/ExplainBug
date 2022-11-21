# WIN BUGS

## We can't sign into your account 
  **Explanation** : Mainly this Bug is caused by a corrupt file in user files or failed update. When the windows trying to load the user data this corrput file prevent it to load correctly so the windows create a tempory user and create a backup for the main user wich we gonna call YOFI .
  **Solution** : there is several solution for this bug and all not the sae it may work and may not. 
  #### Rename Profile List : 
  first you need to acces **regedit** press `ctrl` + `R` write `regedit` then go to this dir `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\ProfileList` then locate your User (eg: S-1-5-21-....-1001) by profileimagepaht (in our case C:\Users\YOFI)
  ##### there is several cases :
  **1. If the SID key is without .bak:**
      
      In the right panel of the SID key (eg: S-1-5-21-....-1001), double click on the ProfileImagePath value name to modify it.

      Enter the correct path (eg: C:\Users\<user-name>) of the user's profile folder, and click OK.

      Verify that the State DWORD is set with a value data of 0 (number zero).
  
 **2. If the SID key is with .bak:**
    
    Right click on the SID key (eg: S-1-5-21-....-1001.bak), click on Rename, and rename the SID key to only remove ".bak" (eg: S-1-5-21-....-1001) at the end of the key's name.

     In the right panel of the SID key (eg: S-1-5-21-....-1001) now without .bak at the end, double click on the ProfileImagePath value name to modify it.

     Enter the correct path (eg: C:\Users\<user-name>) of the user's profile folder, and click OK.

     Verify that the State DWORD is set with a value data of 0 (number zero).
     
**3. If the SID key is without and with .bak:**
     
     Right click on the SID key without .bak (eg: S-1-5-21-....-1001), and click on Delete.

     Right click on the SID key with .bak (eg: S-1-5-21-....-1001.bak), click on Rename, and rename the SID key to only remove ".bak" (eg: S-1-5-21-....-1001) at the end of the key's name.

    In the right panel of the SID key (eg: S-1-5-21-....-1001) now without .bak at the end, double click on the ProfileImagePath value name to modify it.

    Enter the correct path (eg: C:\Users\<user-name>) of the user's profile folder, and click OK.

    Verify that the State DWORD is set with a value data of 0 (number zero).

