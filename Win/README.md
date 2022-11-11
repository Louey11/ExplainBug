# WIN BUGS

## We can't sign into your account 
  **Explanation** : Mainly this Bug is caused by a corrupt file in user files or failed update. When the windows trying to load the user data this corrput file prevent it to load correctly so the windows create a tempory user and create a backup for the main user wich we gonna call YOFI .
  **Solution** : there is several solution for this bug and all not the sae it may work and may not. 
  #### Rename Profile List : 
  first you need to acces **regedit** press `ctrl` + `R` write `regedit` then go to this dir `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\ProfileList` then locate your User (eg: S-1-5-21-....-1001) by profileimagepaht (in our case C:\Users\YOFI)
  ther is several cases : 
  
