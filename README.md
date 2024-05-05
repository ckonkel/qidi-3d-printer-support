# qidi-3d-printer-support

General support for Qidi X-Max 3 and X-Plus 3

resources from
* emails with qidi support
* redit
* facebook
* and personal troubleshooting

# Firmware

## Restore emmc to factory firmware

@TODO


# Troubleshooting

## Z offset issues
Perform a factory reset on the touch screen interface and recalibrate afterward. Qidi utilizes z-axis babystepping for z-offset adjustment, stored in "config.mksini." This file may become corrupted after a firmware update, preventing z babystep values from being stored.
After the factory reset, the file is refreshed, enabling z babystep value saving. In QIDISlicer's "Device" tab, verify the "Z-Offset" entry reflects your adjusted value, not "0.000." If it shows "0.000," redo the adjustment via the printer's display to save the new value.
If there's no update in the "Device" tab, exit and re-enter to refresh. Ensure the Z-offset value in Klipper's printer.config is set to 0.000.

**Caution**: Do not alter the Z-Offset value in fluidd and save, as it modifies printer.config, leading to nozzle-bed collision.
