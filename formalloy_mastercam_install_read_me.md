# Mastercam and APlus Installation Instruction 
## For Formalloy use only


### Mastercam Installation
Open a browser and go to [Download Mastercam Installer 2025.3](https://mlc-cad.com/downloads/mastercam2025-update3-web.exe). Run the executable as an administrater. 

When prompted, select _Mastercam 2025 Install_, then click _next_ on the minimum requirements and installation language configuration page. On the Mastercam installation configuration page, select _edit configuration_. Edit the following fields:

- User Name: _RCSID_
- Company Name: _RPI_
- Install For: _All Users_

and copy the _Shared Defaults Path_ and store it. Follow the prompts and install Mastercam.

### Mastercam Network License Configuration

Once Mastercam is installed, go to [Download CodeMeter 8.2](https://downloads.mastercam.com/public/drivers/CodeMeterRuntime_8_20.exe). Check [Mastercam Drivers and Utilities](https://www.mastercam.com/support/technical-support/drivers-and-utilities/) for a more up to date version of CodeMeter. Install then open CodeMeter Control Center.

Select _File > Web Admin_. This will launch a browser app and display your computer's name, IP address, and other basic information. Navigate to _Configurations_, then under _Server Search List_, select _add new Server_. 

Paste _licsrvr35.win.rpi.edu_ into the pop-up window, then select _add_. Click _apply_ before closing the browser. 

### APlus Installation and License Configuration

Go to [APlus Installer Download](https://ln5.sync.com/dl/d881317d0#jd94sqng-4b2u5dyb-xwsgy7x3-zhgcybzq). The password is _9Lm#f6GvC_. 

Unzip the installer and install APlus. 

Contact [Glenn Saunders](saundg@rpi.edu) for the license file (_CAMU.mclf_). Note down the directory of the license file. 

Open CMD, then run the following commands sequentially:

``` cd [License File Root Directory]```

For example

``` cd C:\Users\local_user\Downloads```

Then, run:

``` move CAMU.mclf [Shared Default Paths] ```

``` cd [Shared Default Paths] ```

``` echo. > AM_Net_License_client.ini```

``` notepad AM_Net_License_client.ini```

Paste _https://128.113.26.47:22355/_ into the document and save.
