# Raspberry Pi Media Center

This project sets up a media center on a Raspberry Pi using LibreELEC. The media center supports various functionalities including PVR TV, gaming, local media playback, and more. This setup can transform your old TV into a smart TV with access to global TV channels (more than 10,000 channels), YouTube, gaming, weather overview, new movies, songs, and everything you need for an enhanced media experience.

## Table of Contents
- [Introduction](#introduction)
- [Requirements and Components Needed](#requirements-and-components-needed)
- [Setup Raspberry Pi for LibreELEC OS](#setup-raspberry-pi-for-libreelec-os)
  - [My Setup](#my-setup)
- [Setup New Skins](#setup-new-skins)
- [Setup PVR TV (IPTV Simple Client)](#setup-pvr-tv-iptv-simple-client)
- [Setup for Gaming](#setup-for-gaming)
- [Add Local Movies Folder](#add-local-movies-folder)
- [Add Local Songs Folder](#add-local-songs-folder)
- [Add Local Pictures Folder](#add-local-pictures-folder)
- [Setup Weather Display](#setup-weather-display)
- [Setup YouTube](#setup-youtube)
- [Comparison Between Smart TV and Smart TV Using Raspberry Pi](#comparison-between-smart-tv-and-smart-tv-using-raspberry-pi)

## Introduction

This project aims to turn your Raspberry Pi into a powerful media center using LibreELEC. LibreELEC is a lightweight Linux distribution that transforms your device into a full-fledged media center. This setup can make your old TV into a smart TV that has access to global TV channels (more than 10,000 channels), YouTube, gaming, weather overview, new movies, songs, and everything you need for an enhanced media experience. LibreELEC is required to run Kodi.

Kodi is a free and open-source home theater software that allows users to play and view most videos, music, podcasts, and other digital media files from local and network storage media and the internet. It was originally developed as XBMC (Xbox Media Center) for the first-generation Xbox game console, but has since been expanded to run on various platforms including Windows, macOS, Linux, Android, and iOS. LibreELEC is a minimal operating system specifically designed to run Kodi, providing a stable, efficient, and easy-to-use platform that enhances Kodi's capabilities and performance.


## Requirements and Components Needed
- Raspberry Pi (My case it is Rpi 4B 2GB version)
- MicroSD card (8GB or larger)
- Power supply for Raspberry Pi
- HDMI cable
- Internet connection (Ethernet or Wi-Fi)
- USB keyboard and mouse (optional, for initial setup)
- External storage (optional, for additional media storage)
- Joystick (need to play games)


## Setup Raspberry Pi for LibreELEC OS
### My Setup
1. **Download LibreELEC:**
   - Visit [LibreELEC Downloads](https://libreelec.tv/downloads/) and download the appropriate version for your Raspberry Pi. You can also do this using [Raspberry Pi Imager.](https://www.raspberrypi.com/software/)

2. **Insert MicroSD Card and Boot:**
   - Insert the MicroSD card into your Raspberry Pi and connect it to your TV or monitor using the HDMI cable. Power up the Raspberry Pi. This will take a while.

3. **Initial Setup:**
   - Follow the on-screen instructions to complete the initial setup, including network configuration. If you want to access your Raspberry Pi using SSH, enable SSH and SAMBA.

4. **SSH Configuration:**
   - To enable SSH, navigate to **Settings** > **LibreELEC** > **Services** and toggle the **Enable SSH** option. Make a note of the IP address shown in the network settings.

5. **Accessing LibreELEC via SSH:**
   - Open a terminal on your local machine and use the following command to access LibreELEC via SSH:
     ```sh
     ssh root@<IP_ADDRESS>
     ```
     Replace `<IP_ADDRESS>` with the IP address of your Raspberry Pi. The default password is `libreelec`.

6. **Accessing Files on LibreELEC:**
   - You can access and transfer files to LibreELEC using SFTP. Use a file transfer client like FileZilla or WinSCP and connect to your Raspberry Pi using the following settings:
     - Host: `<IP_ADDRESS>`
     - Username: `root`
     - Password: `libreelec`
     - Port: `22`

   - You can also access shared folders using SAMBA:
     - On your local machine, open a file explorer and enter the following address:
       ```
       \\<IP_ADDRESS>\storage
       ```
     - Replace `<IP_ADDRESS>` with the IP address of your Raspberry Pi. This will allow you to browse and manage files in the storage directory.


## Setup New Skins
1. Navigate to **Settings** > **Interface** > **Skin**.
2. Select **Get more...** to browse and install new skins.
3. Choose and apply your preferred skin. My preference is **QUARTZ**.

## Setup PVR TV (IPTV Simple Client)
1. Navigate to **Add-ons** > **Install from repository** > **PVR clients**.
2. Select **PVR IPTV Simple Client** and install it.
3. Configure the PVR IPTV Simple Client with your IPTV m3u playlist URL:
   - Go to **Add-ons** > **My add-ons** > **PVR clients** > **PVR IPTV Simple Client** > **Configure**.
   - Under **General**, set the **M3U Playlist URL** to your IPTV provider's URL.
   - You can find url using [this repo.](https://github.com/iptv-org/iptv)
     
##  Setup for Gaming
### RetroArch
1. Install the **RetroArch** add-on:
   - Navigate to **Add-ons** > **Install from repository** > **Program add-ons** > **RetroArch** and install it.
2. Download and install the desired game ROMs.
3. Configure controllers and enjoy gaming on your media center.

### RetroArch
1. Download [this repo](https://github.com/zach-morris/plugin.program.iagl) in your downloads folder.
2. Type following.
```
https://github.com/zach-morris/plugin.program.iagl
```
3. Download and install the desired game ROMs.
4. Configure controllers and enjoy gaming on your media center.

## Add Local Movies Folder
1. Navigate to **Videos** > **Files**.
2. Select **Add videos...**.
3. Browse to the directory where your movies are stored and add it as a source.
4. Name the source and set the content type to **Movies**.

## Add Local Songs Folder
1. Navigate to **Music** > **Files**.
2. Select **Add music...**.
3. Browse to the directory where your music is stored and add it as a source.
4. Name the source and set the content type to **Music**.

## Add Local Pictures Folder
1. Navigate to **Pictures** > **Files**.
2. Select **Add pictures...**.
3. Browse to the directory where your pictures are stored and add it as a source.
4. Name the source.

## Setup Weather Display
1. Navigate to **Settings** > **Add-ons** > **Install from repository** > **Weather**.
2. Select a weather add-on (e.g., **Yahoo! Weather**) and install it.
3. Configure the weather add-on with your location.

## Setup YouTube
1. Navigate to **Add-ons** > **Install from repository** > **Video add-ons**.
2. Select **YouTube** and install it.
3. Follow the on-screen instructions to log in and set up your YouTube account.

## Comparison Between Smart TV and Smart TV Using Raspberry Pi
| Feature                         | Smart TV                         | Raspberry Pi Media Center     |
|---------------------------------|----------------------------------|-------------------------------|
| Cost                            | High                             | Low                           |
| Customizability                 | Limited                          | High                          |
| Software Updates                | Manufacturer-dependent           | User-controlled               |
| Add-ons and Plugins             | Limited                          | Extensive                     |
| Gaming                          | Limited to apps                  | Retro gaming support          |
| Local Media Support             | Varies                           | Excellent                     |
| PVR and IPTV                    | Limited                          | Full support                  |

## Contributing
Contributions are welcome! Please fork this repository and submit pull requests.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
