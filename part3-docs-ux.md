# Part 1: Kisi + Legacy Hardware Integration

## Legacy reader + Kisi Reader
- [Wire the Kisi Reader](https://docs.kisi.io/access_control/hardware/readers/kisi_reader_pro_2_1/wire_reader_pro_2_1) to the [Kisi controller](https://docs.kisi.io/access_control/hardware/controllers).
- Connect the **legacy reader** to a [Wiegand channel](https://docs.kisi.io/access_control/hardware/controllers/kisi_wiegand_board/wire_legacy_hardware) set to `READER` mode.
- The **Kisi Controller** now receives credentials from both readers, if *either* provides a valid credential, the door unlocks.
<details>
  <summary>Step-by-Step Wiring Instructions for a Legacy Reader (click to expand)</summary>

1. Select one of the four Wiegand channels on the Wiegand board
2. Toggle the switch of the selected Wiegand channel to READER mode
3. Connect the legacy reader's D0 wire to the D0 port of the Wiegand channel (Green - Data line 0)
4. Connect the legacy reader's D1 wire to the D1 port of the Wiegand channel (White - Data line 1)
5. Connect the legacy reader's + wire to the + port of the Wiegand channel (Red - 12 volts direct current)
6. Connect the legacy reader's - wire to the - port of the Wiegand channel (Black - Ground)
7. Connect the legacy reader's LED cable to the G (Green) port of the Wiegand channel
</details>
<!-- All the information I use for this project is from Kisi's documentaition portal, so I have copied the exact text for wiring from the portal, hence the wiring description was not writen by me -->

## Kisi Controller + Legacy Controller
- Connect the [Kisi Controller](https://docs.kisi.io/access_control/hardware/controllers) via its [Wiegand board](https://docs.kisi.io/access_control/hardware/controllers/kisi_wiegand_board/wire_legacy_hardware) to the legacy controller wired to the door.  
- When a user authenticates through the reader, the [Kisi Controller](https://docs.kisi.io/access_control/hardware/controllers) recieves the credential and if it is valid, signal is sent to the legacy controller.
- The legacy controller unlocks the door.
  
This integration allows for a smooth transition to Kisi while preserving legacy systems.  
