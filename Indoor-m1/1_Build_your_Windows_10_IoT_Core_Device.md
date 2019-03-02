Setting up your sensor device
=============================

This lab document is to help students with the FarmBeats Student Kit hardware
setup. It includes installing Windows 10 IoT Core on your Raspberry Pi,
installing the sensor software, connecting the sensors and getting the device
claim code needed to register the device in the [FarmBeats Student Kit
Portal](https://farmbeatsstudentkit.com) and Azure IoT Central cloud service.

Installing Windows 10 IoT Core on you Raspberry Pi 3
----------------------------------------------------

Windows 10 IoT Core is a version of Windows 10 that is optimized for smaller
devices with or without a display, and that runs on small devices like the
Raspberry Pi 3. Windows 10 IoT Core utilizes the extensible Universal Windows
Platform (UWP) API for building rich Internet of Things solutions.

-   Go to the [Windows 10 IoT Core Dashboard Documentation
    Page](https://docs.microsoft.com/en-us/windows/iot-core/connect-your-device/iotdashboard)

-   Click **Get Windows 10 IoT Core Dashboard**

![](media/9de93f80bd289832fe0b57fadfcb24e0.jpg)

-   Install the dashboard application and open it

-   Select **set up a new device** from the side bar.

-   Select the options as shown in the image below. Make sure you select the
    correct drive for your microSD card and give your device a name and admin
    password.

    -   You may need to use the SD card adapter and install it in a USB port on
        your PC

![](media/14b397bfb07da245ad7b078ee05417b0.jpg)

-   Select the Wi-Fi network connection you want your Raspberry Pi to connect
    to, if required. Only wi-fi networks your PC already connects to will be
    shown. The Wi-Fi information from your PC will be shared with the Raspberry
    Pi.

-   Select the **I accept the software license** terms and click **download and
    install.**

-   The application will now download the necessary files from Microsoft and
    flash them to your microSD card. It'll take a little while, but the
    dashboard will show you the progress.

![](media/d02a8f386599a6d7a6a0d5ccfd2041f8.jpg)

-   Once the image has been installed on the microSD card, you will get the
    message “Your SD card is ready”. Now it's time to eject it from your PC and
    go over to the Raspberry Pi and insert it into the slot on the underneath.

![](media/4d30fd69f13ba83c035814c019a86aad.jpg)

Connect Sensors
---------------

Adding sensors to your Raspberry Pi is easy.

-   Add the Grove Base Hat to your Raspberry Pi. Match the end pins up and press
    down firmly.

![](media/4b802b3790f57552645748940ee204f0.jpg)

-   It’s also a good idea to screw in the supports on the side opposite the pins
    to provide support and stop the other side of the board from collapsing.

![](media/1f209ed732abfc9e0d013b58ee6b912e.png)

-   Plug the Capacitive Soil Moisture Sensor into socket A2. If you have a
    second one plug it into A4.

![](media/f5480d415f29c578760d73d7f20ef930.png)

-   Plug the Light Sensor into socket A0.

![](media/d13a81eb0f03be4b60cd1230990784d3.png)

-   Plug the Barometer Sensor (BME280) with Temperature and Humidity into the
    bottom left I2C socket.

![](media/10bf337bf57976cb561754df48831bc3.png)

-   Once all your sensors are plugged in you should have something that looks
    like this.

![](media/f0c289152a4ecce31ae8c600494f414d.jpg)

>   image1.jpeg

Connecting to the LAN and Internet
----------------------------------

There are multiple options to getting your Raspberry Pi online and manageable by
your PC. Ideally you would have the PC and Raspberry Pi on the same network.

-   **Ethernet Cabled** – Plug one side of the LAN cable into the Raspberry Pi
    and the other into the same Ethernet Hub or Switch that your PC is plugged
    into.

![](media/ceab608d1b677684ce329ee41425de39.jpg)

![](media/034244884046f41ec0ddc435fb656049.jpg)

-   **Wi-Fi** - During the creation of the device image you had the option of
    having the Raspberry Pi join a wi-fi as part of the SD Card operating system
    deployment. If that didn’t work then see this page for more details
    <https://docs.microsoft.com/en-us/windows/iot-core/connect-your-device/setupwifi>

-   **Mouse, Keyboard, Monitor** – The easiest way to get connected and see what
    is going on with your networking status is to connect a mouse, keyboard and
    monitor to the device. This can help you provision wi-fi or lookup the IP
    address if you are plugged into ethernet. You can use the console to see the
    network IP address.

Power on your device
--------------------

-   Plug the large end of the micro USB cable into the power adapter

-   Plug the small end of the micro USB cable into the Raspberry Pi and Power
    Up!

The “out of the box” setup process. (if you have connected a mouse monitor and keyboard)
----------------------------------------------------------------------------------------

Unlike your Windows 10 desktop, laptop or tablet, there's not much of a setup
process.

-   You'll be asked to choose a language

-   Select the level of information you want to send back to Microsoft.

-   Select the privacy setting for sharing your location.

-   If not already connected via Ethernet cable or with Wi-Fi details it was
    provided when you installed the SD card then you will be asked to enter your
    Wi-Fi password to connect to the web. If needed, connect a keyboard to
    complete this step.

It'll take a couple of minutes, but when booted up you'll see the Windows 10 IoT
Core splash screen. There is not much to see here, the Windows 10 Operating
System part is designed to disappear, since once you deploy an app to your
Raspberry Pi, it becomes that app. There's no flipping in and out of Windows and
launching apps like you would on a PC.

![](media/0133c1daaa3b5ba6bbdfa18aad4bdb77.png)

-   When booted, check that you have a valid IP address.

Now you can go back to the dashboard application on your PC, and you'll see your
Raspberry Pi listed as one of your devices.

Configuring Windows 10 IoT Core
-------------------------------

-   In the Windows IoT Dashboard select the **My devices** tab on the top left.

![](media/fbd090a89c367aa72d697c8a7c213b5f.png)

-   In the **My devices** page right click on your Raspberry Pi to access the
    menu.

-   Select the **Open in device portal** menu item

![](media/bb5260823b9a908db763d51bc5b5a08a.png)

-   Login to Windows Device Portal using the username **Administrator** and the
    password you used when making the SD card. The [Windows Device
    Portal](https://docs.microsoft.com/en-us/windows/iot-core/manage-your-device/DevicePortal)
    (WDP) lets you configure and manage your device remotely over your local
    network.

![](media/e3e42de7d615f0dcbde66ed907c1e98f.png)

-   Select **Connectivity** on the menu on the left, then Select **Network**

    -   On the right hand side of the screen are listed all the types of network
        connections on the Raspberry Pi. Look for the one that starts Record the
        Mac address of your LAN card

![](media/3696af5f61d76ece9e7422b8b2a6d107.png)

-   Look for the one that starts with LAN and record the Physical address. This
    is your unique device ID that is used as the claim code for device
    registration on the Student Kit Portal.

![](media/4e2048303dd6880d896ea3baaa9ebfc8.png)

-   On the left menu click on the Windows Updates. Click Check for Updates to
    see if there are any updates for your device. This process can take a while
    but will download and install in the background.

-   Change your Time zone (optional)

-   To change the **device name** select “Device Settings” on the left menu.
    Then type a new name and select Save. It will prompt you to reboot the
    device.

![](media/9905fa05c59c88c819f3d1cfd81a019f.png)

Installing Gateway Application
------------------------------

-   Download and unzip the latest [Sensor
    Application](https://fblassets.blob.core.windows.net/releases/FarmBeatsLabs.UWP.Headless_1.0.11.0_arm.zip)
    software.

![](media/a91b28a4890c5a24427279e20aadc9d9.png)

-   Select Apps on the left menu ad then App manager

![](media/515bd27e42ff7da4f2d6d0589da9fd1d.png)

-   Select Browse in the “Select the application package” input dialog

-   Browse to the location of the downloaded files and select the file ending in
    FarmBeatsLabs Appxbundle file.

![](media/ee2058e2e0cdaa676a719212aeac5569.png)

-   Next select the “Allow me to select optional packages”

-   Choose file, and select the Microsoft.NET.CoreRuntime2.1.appx file

-   Choose file again and select the Microsoft.VCLibs.ARM.Debug.14.00.appx file

![](media/24c4147d4c7ed9ff6ce841b681f42c6f.png)

-   Click the Install button

![](media/a4386c03a586f8b9f8ab4ac52c4e5d8e.png)

-   The application should install and give you a “Package Successfully
    Registered” message at the end with it’s complete.

![](media/b354423514a58623f768a1cfba0a9150.png)

-   The application should now show up in the Apps list.

-   Set the FarmBeatsLabs Indoor Grove Base Hat to Startup when the device boots
    by switching the startup toggle. This will also start the application now.

![](media/26106e22a35f9156e50772ec7e130abc.png)

You have successfully installed your Windows 10 IoT Core sensor device and
software

Now proceed to [Step 2 – Register your FarmBeats Student Kit User and
Device](https://github.com/farmbeatslabs/studentkit/blob/master/Indoor-m1/2_Register_your_FarmBeats_Student_Kit_User_and_Device.md)
