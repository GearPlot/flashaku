# ![icon](https://github.com/GearPlot/flashaku/blob/main/flashaku_icon.png) Flashaku

Flashaku is a simple, lightweight USB image writer utility designed specifically for Haiku OS. Written in **Yab**, it provides a graphical user interface (GUI) wrapper around the native `dd` utility, allowing users to securely write ISO and raw disk images to USB flash drives.

![App Screenshot](https://github.com/GearPlot/flashaku/blob/main/flashaku_sc.png)


## Features

- **Device Auto-Detection:** Automatically scans and lists un-mounted USB storage devices under `/dev/disk/usb/`.
- **Haiku Native File Browser:** Uses Haiku's native file panel to easily locate and select source ISO/image files.
- **Safety Overwrite Warnings:** Prompts users with a modal warning dialog before proceeding with any data-destructive write operation.
- **Volume Safety Check:** Continuously checks the target USB device at every step of the process and blocks writing if volume is mounted, preventing data corruption.
- **Asynchronous Copy Tracking:** Executes the writing process in the background using a non-blocking loop, keeping the UI responsive while tracking bytes written, total MBs, and percentage.
- **Visual Copy Animation:** Features an animated indicator demonstrating active write operations.

---

## Requirements

- **Haiku OS** (Tested on R1/beta5)
- **Yab** (Version 1.8.2 or newer)

---

## Installation & Running

1. **Packages Available:** 

   Flashaku 32 bit .hpkg [Download here](https://github.com/GearPlot/flashaku/releases/download/v1.0.0/Flashaku-1.0.0-1-x86_gcc2.hpkg)

   Flashaku 64 bit .hpkg [Download here](https://github.com/GearPlot/flashaku/releases/download/v1.0.0/Flashaku-1.0.0-1-x86_64.hpkg)


2. **Clone or Download the Script:**
   
   If you are installing via the provided pre-built packages, you can safely skip this section—all graphic assets and paths are configured automatically.

   Save the Yab script to a directory on your Haiku system. The application references graphic assets at specific locations. Every line in the source code that handles file and asset paths includes inline comments to guide you on what needs to be updated when building for different system directories.


---

## How to Use

1. **Select Source Image:** Click the **Select** button in the *Source* box and locate your target `.iso` or `.img` file.
2. **Select Target USB:** Plug in your USB drive and **do not** mount it, and select the appropriate device from the drop-down list. If you plugged the device in after launching, click **Refresh** to update the list.
3. **Write Image:** Click **Start**. Read and verify the target path in the warning prompt, then click **Continue** to start writing.
4. **Monitor Progress:** Wait for the write window status bar to reach 100% and notify you of completion.

*Caution: Writing an image will erase all existing partitions and files on the chosen USB target device. Ensure you have backed up any critical data before proceeding.*


---

## License

This project is released into the **Public Domain**. Feel free to modify, distribute, and adapt it to your needs. 

## AI Disclosure
Created with assistance from AI.

