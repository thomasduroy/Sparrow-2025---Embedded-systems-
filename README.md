---
# 🚀 Sparrow 2025 - Embedded Systems Programming

This repository contains the course handout, as well as the tools and code for your projects.

---

## Directory Structure

| Folder | Content / Description |
| :--- | :--- |
| **`doc/`** | Official course documents: **handout** and presentation **slides**. |
| **`src/`** | **Code** resources and libraries for the embedded board. |

---

## Detailed Content of the `src/` Folder

The `src/` folder contains the following items to help you develop and test your code:

* **`src/tests/`**
    * Test scripts for peripherals: **buzzer**, **servo**, and **accelerometer switch**.
* **`src/libs/`**
    * The essential **libraries** to upload to the board to run your code correctly.
* **`src/main/`**
    * A code **template** for the main task (which you need to produce).
    * A **complete code example** (solution) to use if you are really struggling.
* **`src/sdcard/`** (Bonus)
    * Library for writing data to an **SD card**.
* **`src/picoprobe/`** (Data Recovery)
    * Contains the **`picoprobe.uf2`** image for users who accidentally deleted their flight data.

---

## Getting Started: Uploading Code to Raspberry Pi Pico

This guide explains the process for setting up the **Thonny IDE** and the steps required to upload your Python code files to the **Raspberry Pi Pico** development board.
Note that this serves as a quick reference and summary of the setup and code uploading process detailed within the full course materials.

### 1. Prerequisites and Setup

* **IDE:** Download and install the **Thonny Integrated Development Environment (IDE)**.
* **Cable:** You will need a **USB-A to micro USB cable** that supports **data transfer**. Be aware that some cables only allow charging and cannot transfer data.

### 2. Connecting the Pico in BOOTSEL Mode

To ensure your computer recognizes the Pico as a storage device for initial setup, you must start it in **BOOTSEL mode**.

1.  **Locate:** Find the **BOOTSEL** button on the Pico board. 
2.  **Hold:** Keep the **BOOTSEL** button **pressed down**.
3.  **Connect:** While continuing to hold the button, plug the board into your computer using the USB cable.
4.  **Result:** The Pico will mount as a **USB Mass Storage Device**, and a file explorer window may open. (This window is usually not needed here but can be useful for card debugging.)

### 3. Configuring the Thonny Interpreter

Once the Pico is connected, you must configure Thonny to communicate with the board's **MicroPython** interpreter.

1.  **Select:** In the **bottom-right corner** of the Thonny window, click on the displayed Python version.
2.  **Choose Interpreter:** Select the option **MicroPython (Raspberry Pi Pico)**.
    * *If this option does not appear, check your Pico connection and ensure it is in BOOTSEL mode.*
3.  **Verify Shell:** Look at the **console** (or Shell) at the bottom of the Thonny editor. You should see a MicroPython welcome message, confirming that Thonny is ready to communicate with the board. 

### 4. File Management Setup

To easily navigate and transfer files between your computer and the Pico, enable the File panel.

1.  **Access:** Go to the **View** panel located at the top of Thonny.
2.  **Enable:** Check the **Files** option.
3.  **Result:** You will now see two file trees: one for your computer and one for the MicroPython device (the Pico).

### 5. Uploading a Python File

You can upload a Python file from your computer to the Raspberry Pi Pico using two methods.

#### Method A: Save As... (Standard Method)

1.  Open the desired Python file in the Thonny editor.
2.  Go to **File** in the menu bar.
3.  Choose **Save As...**.
4.  Select the destination: choose to save the file **on the MicroPython device**.

#### Method B: Right-Click (Quick Method)

1.  In the computer file tree panel (usually on the left), locate the Python file you want to transfer.
2.  **Right-click** on the file name.
3.  Select the **Upload to...** option (Upload to MicroPython device).
