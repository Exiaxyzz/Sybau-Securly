# Sybau-Securly
#Onestop shop for securly removal needs.
#How to remove Securly on the #$%^#% Laptops:
  There are a few steps to this process:
    Step 1:
      Grab your Bitlocker key at https://aka.ms/myrecoverykey
      Then go to your devices and find the key.
      WRITE IT DOWN!!!
      If u cant find it under ur devices, ur cooked.
    Step 2:
      Log in to your account and go to the start menu. Once you have done that, click the power options and restart while holding left shift until winRE (Blue Screen recovery options) comes up.
    Step 3:
      Navigate to recovery options and click command prompt.
      If ur on a @#%@%^ managed pc this is where ur Bitlocker key comes in handy.
      Enter it and u should see smth like :x/Windows/ blah blah blah
      type:
        cd C:/Name of ur drive
        cd Windows
        cd System32
        ren utilman.exe utilman1.exe
        ren cmd.exe utilman.exe
        exit
      Then:
        UR DONE!!!
        click out and boot into windows. Before logging in, click the bottom right accessibilty options, then a cmd windows shuld popup. U might needa try a few times. 
        Then type:
          cd C:"name of ur drive"/Users
          net user add "ur choice"
          netplwiz
        THen:
          u shuld see a window to manage the users, u click on the one u js created and set it to ADMIN, and u can change the pass there too.
      Step 4:
        LOGIN!
        go to other users and first type Administrator, same caps everything must be the same, then below it shuld say sign into ur device name. Remeber that and delete the username column. then type:
        Your device name exactly\ur username
        then:
        IT MUST BE A BACKSLASH
        THE BACKWARDS ONE
        type ur password
        then u should login.
        THEN UR DONE
        
