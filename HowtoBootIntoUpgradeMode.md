# Howto Boot Into Upgrade Mode

There are many different ways to boot into upgrade mode listed as following:

### Keys Mode(U-Boot is running)
1. Power on Vim.
2. Long press `Power` key without release
3. Short press ‘Reset’ key and release
4. Count 2-3 seconds and release the ‘Power’ key to enter into upgrade mode


### Serial Mode(For developers)
1. Refer this [guidance](https://github.com/khadas/documents/blob/master/SetupSerialTool.md) to setup serial tool for Vim.
2. Make sure again you've done the right connections and setup.
3. Hit any keys at the moment of booting to stop autoboot. This step will let Vim boot into u-boot mode.
4. Type `run update` on the terminal of u-boot as belowing:
```
Vim# run update
```


### MRegister Mode(Maskrom Mode)
1. Power on Vim.
2. Use a tweezer to short-circuit the two pads of `M` register and without release.
3. Short press `Reset` key and release it to boot into upgrade mode

*Tips: The  `M` register is loacated on the bottom of Vim:*

![Image of MRegister_ShortCircuit](https://github.com/khadas/documents/blob/master/images/MRegister_ShortCircuit.png)
