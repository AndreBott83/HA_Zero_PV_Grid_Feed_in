# Summary

This automation will react on changes of energy imported or exported from the grid.
It will control the Photovoltaic power generation by setting the limit to a value avoiding exporting to the grid

## Required sensors / entities

### GridPowerMeters:
Sensors measuring Grid import or export e.g. all 3 phases in W.
All power meters will be summed up to define the total grid import or export.

### PVPowerMeters:
Sensors measuring PV Generation in W
If sevaral Sensors are selected, those will be summed up.

### NonPersistantLimit:
Entity to set the non persistant absolut limit in W. It should be the non persistant limit to avoid too many writes towards the flash memory.

### InverterOnlineStatus:
Entity indicating if the inverter is available ('On' -> available)


Kudos for the simple algorithm and idea go to:
https://selbstbau-pv.de/wissensbasis/nulleinspeisung-hoymiles-hm-1500-mit-opendtu-python-steuerung/

# Change log
**Version: 0.0.3** - Add parameter to define, at which feed in power the controller will get active. Also add parameter to select the control mode

**Version: 0.0.2** - Improve Error handling in case sensors are unavailable

**Version: 0.0.1** - Initial commit
