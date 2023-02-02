## Quick Overview:
Because MidwayR3 has no connection to the Internet, you would need to use a "middleman" - Secure Data Enclave Desktop to access MidwayR3.
Accessing MidwayR3 is a two-step process:<br><br>
1. Login to the Secure Data Enclave (SDE) Desktop using the Azure Virtual Desktop (AVD).<br>
2. Once you are connected to the SDE Desktop, login to MidwayR3 using ThinLinc or an SSH client.<br><br>

* You do not need to be connected to the University VPN before connecting to MidwayR. Azure takes care of encrypting and securing all communications between your local computer and the Virtual Desktop.
* You can connect from your web browser, in addition to the Microsoft Remote Desktop application.
* It is no longer possible to copy/paste between your local computer and the Virtual Desktop. You can still copy/paste inside the AVD environment.
!!! warning
    Once your login session ends with Azure, all data that was downloaded will be purged from the AVD.

#### Connecting To The AVD From The Web Browser
Navigate to [https://rdweb.wvd.microsoft.com/arm/webclient](https://rdweb.wvd.microsoft.com/arm/webclient) on your computer's web browser.
Select "AVD Host" to launch the Virtual Desktop:

![Screenshot showing AVD landing page](images/avd_webpage.png){ width="1000" }

You will be prompted for your username (cnetID@uchicago.edu) and password:

![Screenshot showing AVD login](images/avd_login.png){ width="1000" }

After logging in, you will arrive at the Desktop where you can launch applications:

![Screenshot showing AVD Desktop](images/avd_desktop.png){ width="1000" }

#### Connecting To The AVD From Microsoft Remote Desktop
You can also connect from the Microsoft Remote Desktop App, available for download on the Windows or MacOS app store.
After launching the app, click on the "+" symbol and select "Add Workspace":

![Screenshot showing Microsoft Remote Desktop App](images/avd_desktop_workspace.png){ width="500" }

In the dialog box, put the URL
"https://rdweb.wvd.microsoft.com":

![Screenshot showing Microsoft Remote Desktop App](images/avd_desktop_add.png){ width="700" }

You should then be able to launch the AVD from within the App.

#### Connecting To MidwayR3
Once you are connected to the SDE environment using the AVD client following the steps given above, please follow one of the methods below to connect to MidwayR3 from the SDE environment.

###### Connecting with ThinLinc

ThinLinc is a remote desktop server application. It is recommended to
use ThinLinc when you run a software that requires a graphical user
interface, or "GUI" (e.g., Stata, MATLAB). To use ThinLinc to connect
to MidwayR, please take the following steps:

1. Open a browser (Chrome or Firefox) and enter
   `https://sde.rcc.uchicago.edu` in the address bar.

2. Enter your CNetID and password on the ThinLinc login page:<br><br>
![Screenshot showing Chrome connecting to ThinLinc](images/tl_login.jpg)
<br><br>

3. Follow the two factor authentication prompts:<br><br>
![Screenshot showing ThinLinc 2FA](images/tl_2fa.jpg)
<br><br>

4. If the login process is successful, you will see a Linux desktop
environment. To access the command-line shell, select the Applications
menu, then the Terminal icon:<br><br>
![Screenshot showing ThinLinc terminal launch](images/tl_terminal.jpg)
<br><br>

5. After selecting the Terminal icon, you should see a Terminal window
appear. Typically this will give a console prompt showing which login
node you are connected to, either `sde-login1` or
`sde-login2`:<br><br>
![Screenshot showing ThinLinc terminal](images/tl_terminal2.jpg)
<br><br>

To exit ThinLinc, type `exit` in any Terminal window, select the
top-right icon, then select the "Log Out" menu item and follow
the instructions. Finally, close the browser window.<br><br>
![Screenshot showing ThinLinc logout](images/tl_logout.jpg) <br><br>


## Logging Out
You can log out of the AVD by clicking the "Log off" application on the Desktop.
!!! warning
    Once logged off, any data stored in your AVD user-space will be purged.

