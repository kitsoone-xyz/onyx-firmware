# Onyx Keyboard Firmware

This repository contains the firmware for the Onyx keyboard, with support for different hardware configurations.

## Branches

There are three branches, one per hardware variant:

- onyx-standard — Standard keyboard (no display)

- onyx-oled — Keyboard with OLED display

- onyx-nice-view — Keyboard with nice!view display

### ⚠️ Important
Before making any changes, you must select the branch that matches your hardware.
All configuration and builds depend on the correct branch.

## How to customize and build your firmware

1. Select the correct branch

    Choose the branch based on your keyboard hardware:

      - No screen → onyx-standard
      - OLED screen → onyx-oled
      - nice!view screen → onyx-nice-view

2. Fork the repository

    Fork the selected branch to your own GitHub account.

3. Make your changes

    - Edit your configuration (keymap, behavior, etc.)
    - Commit and push your changes to your fork

4. Build the firmware

    - Go to the Actions tab in your forked repository
    - Click on the latest workflow run
    - Download the generated firmware artifact
    - This will download a ZIP file containing:
        - Left half firmware (*.uf2)        
        - Right half firmware (*.uf2)        
        - Reset firmware (*.uf2)

## Flashing the firmware  

### Flashing steps

1. Double-click the reset button on the half you want to flash
(the half will appear as a USB drive)

2. Drag and drop the correct firmware file:
    - Left half → left firmware
    - Right half → right firmware

3. Repeat the process for the other half

### If you have problems

If flashing fails or a half doesn’t respond:

1. Flash the reset firmware on both halves

2. Then flash the correct left and right firmware again

  This usually resolves connection or pairing issues.

## Changing the keymap

You have two options to modify your keymap.

### Option 1: ZMK Studio (easiest)
  
  - Use ZMK Studio to visually edit your keymap:
    👉 https://zmk.studio/ 
  - Once you’re done, save your changes.

### Option 2: Edit the keymap file manually

  - Open the onyx.keymap file in the repository
  - Modify the keymap directly
  - Commit, push, and build via GitHub Actions

If you need a list of available keycodes, refer to:

👉 https://zmk.dev/docs/keymaps/list-of-keycodes

Default keymap

The default keymap is shown in the image below:

![Onyx-layout](./Assets/keymap-diagram.svg)


