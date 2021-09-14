Current sonixQMK with RGB layers works but also causes crazy flashing. This is a guide to use an older version of sonixqmk. Hopefully the more current verison will be fixed soon.

You don't have to do some of these steps exactly this way, but here's what I did.

1) If you're running the version of SonixQMK from after July 26th 2021, then the qmk_firmware to a zip file and store it somewhere just in case.

2.1) You can clone either my fork and simply edit my keymap (sebetterRGBFN) or make your own by cloning the repo in step 2.2.

2.2) Open QMK MSYS (or ubuntu) and enter this: 
git clone https://github.com/radunanescu/qmk_firmware.git

3) follow CanUnesi's instruction steps 2.5-2.7 in QMK MSYS (https://github.com/CanUnesi/QMK-on-K6#2-setting-up-the-environment---qmk-msys)

4) Navigate to qmk_firmware/keyboards/keychron/k6/keymaps

5) unzip sebetterRGBFN into the keymaps folder.

6) If there's a rules.mk file in the sebetterRGBFN folder, delete it or move it or rename it.

7) Change the keymap.c file to how you wish. You can change replace the key mappings KC_XXXX to whatever you like

7.1) Change the RGB below by replacing the lines or words with other lines or words as you see fit. You might want to colour code or simply highlight the keys that are active on the FN layer. 

8) in QMK MSYS run: make keychron/k6:sebetterRGBFN

9) You can rename the profile if you like. Make sure the command in step 8 reflects whatever you renamed the profile.

10) check the rules.mk file in the k6 folder. Check for sleep breath enable and NEKRO. See CanUnesi's guide (linked above) for enabling/disabling those settings.

11) flash in SonixQMK. (unplug the keyboard, hold Spacebar+B, plug the keyboard in ((you can release the keys when the lights go on and then off again)).

