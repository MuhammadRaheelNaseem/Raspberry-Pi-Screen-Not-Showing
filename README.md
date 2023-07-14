# Raspberry-Pi-Screen-Not-Showing

# `How to fix ‘Cannot currently show the desktop’ on Raspberry Pi`

![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/f30ace39-a360-40e8-a3f7-4988d06da535)

### If you installed a remote connection to your Raspberry Pi using VNC, it can happen you get a black screen with an error message ‘Cannot currently show the desktop’ on your next connection attempt. In this repository, we’ll see how you can fix this issue easily.

# `Open Putty SSH`
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/e911924b-0b44-4ec9-8eb0-1a9d6b89c414)
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/5fdc050a-b8b7-45f0-b93f-4fcd3077698a)
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/e5e33934-6fc6-4542-aeaf-d0a97e9a5698)
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/c30ebcae-32b5-478d-bf2c-1a501e1364cb)

# Check Raspberry Pi OS version by this command ==> `cat /etc/os-release`
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/64801398-7882-4c54-b96f-112f50360d56)

# Switch to root user ==> `sudo su`
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/eb9a3cd8-bfe3-4233-83be-d9240790d2e8)

# `Only for version 10`
# Change the display settings in your config.txt file as following command:
## command #1 ==> `echo 'hdmi_force_hotplug=1'>> /boot/config.txt`
## command #2 ==> `echo 'hdmi_group=2'>> /boot/config.txt`
## command #3 ==> `echo 'hdmi_mode=51'>> /boot/config.txt`
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/7208b521-6bde-43bb-b0d2-e3d94882eb63)

It’s optional, but if you want to visualise the changes you just made in your config.txt file, enter :
`nano /boot/config.txt`
Have a look at the bottom of the file.
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/104b3729-e1eb-4280-9d2f-06515ebe931a)

# Now Restart Raspberry Pi
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/b9820667-d0db-4f35-89bf-66de44be44c7)

# Open VNC Viewer
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/4f557841-b57e-4256-84f0-d9417248953d)
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/82eac953-4eb2-4ddc-9f32-9f092c7e7070)
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/5c5b2592-0837-4cbd-b2eb-a9e9d09c0a9e)
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/aab338cb-6f4c-4d44-8e2e-d34cf4404278)
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/761a0638-e5d9-4382-b4ab-36634fc0efff)


<hr>
# Another method for version 11:

# Only for version 11 : Change the display settings in the Raspberry Pi Software Configuration Tool (raspi-config) as follows :
To open the raspi-config tool, enter :
`sudo raspi-config`
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/00af8294-52d4-4734-b68d-339a1b55e972)

Now navigate to :
`2 Display Options`
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/3ff82294-078d-405d-bfc0-2a25105d65b2)

then to :
`D5 VNC Resolution`
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/f7c582ad-0dfe-415b-909d-ac7c789aedcb)


and select a resolution that suits you best. I always choose the maximum resolution :
`1920x1080`
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/ad5154c9-e45e-49f4-85bf-7af6f4890367)

Click on your ‘Tab’ and then the ‘Enter’ key to select the chosen resolution.
Click on ‘OK’ and then ‘Finish’ to save your settings.
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/cca7e22c-2cb9-4fd8-a53a-efdce9a703b8)
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/bd5bead3-6b39-4710-ad0f-32598c8b6165)
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/94404522-d200-4e55-ab83-d8fa3bf86197)

Finally, enter :
`reboot`
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/84ef46d5-524e-4b95-81a7-3211f840bdc3)

Reconnect remotely with your VNC viewer.
![image](https://github.com/MuhammadRaheelNaseem/Raspberry-Pi-Screen-Not-Showing/assets/63813881/65b9979e-2cd1-4394-926f-f84de56a6572)



