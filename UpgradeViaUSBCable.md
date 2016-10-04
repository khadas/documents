# Upgrade introductions:  Via a USB-C Cable

**Preparations:**
* Download the [USB Upgrade Tool](http://www.mediafire.com/file/mvf43ds0iacs8i7/USB_Burning_Tool_v2.0.8_x86.rar) and extract it.
* Run 'setup_v2.0.8.exe' to install the tool for Vim upgrading:

![Image of USB_Upgrade_Tool_Setup_V208](https://github.com/khadas/documents/blob/master/images/usb_upgrade_tool_setup_v208.png)

## Upgrading Steps:
Make sure that you have right installed the USB Upgrade Tool, then follow the below steps to upgrade:

1. Open ‘USB_Burning_Tool_v2.0.8.exe’, click ‘File-->Import image’ to chose an image for Vim.
2. Connect Vim and PC with an USB-C cable(Vim will power on automately).
3. Let Vim enter into upgrade mode to complete the upgrading:
  * Long press `Power` key without release
  * Short press `Reset` key and release
  * Count 2-3 seconds and release the `Power` key to enter into upgrade mode
4. Your PC should have found Vim device as upgrade mode if you correctly follow the above operations. Now all you need to do is to click `Start` button of the tool and wait the upgrading to complete:
![Image of USB_Upgrade_Tool_Setup_V208](https://github.com/khadas/documents/blob/master/images/usb_upgrade_tool_interface_v208.png)

Tips:
* Click `Stop` button first, then close the tool to quit current upgrading operation.
* [Extra power supply](https://github.com/khadas/documents/blob/master/ExtraPowerInput.md) is required in some case your PC cannot provide enough current for the upgrading.


Have Fun!

**See also:**

1. [Upgrade Via a TF Burning Card](https://github.com/khadas/documents/blob/master/UpgradeViaTFBurningCard.md)
2. [Other Methods to Enter Into Upgrade Mode](https://github.com/khadas/documents/blob/master/All_upgrade_mode_mothods.md)
