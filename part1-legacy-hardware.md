## Part 1: Kisi + Legacy Hardware Integration
### Legacy reader + Kisi Reader
- [Wire the Kisi Reader](https://docs.kisi.io/access_control/hardware/readers/kisi_reader_pro_2_1/wire_reader_pro_2_1) to the [Kisi controller](https://docs.kisi.io/access_control/hardware/controllers).
- Connect the **legacy reader** to a [Wiegand channel](https://docs.kisi.io/access_control/hardware/controllers/kisi_wiegand_board/wire_legacy_hardware) set to `READER` mode.
- The **Kisi Controller** now receives credentials from both readers, if *either* provides a valid credential, the door unlocks.

### Kisi Controller + Legacy Controller
- Connect the [Kisi Controller](https://docs.kisi.io/access_control/hardware/controllers) via its [Wiegand board](https://docs.kisi.io/access_control/hardware/controllers/kisi_wiegand_board/wire_legacy_hardware) to the legacy controller wired to the door.  
- When a user authenticates through Kisi, the [Kisi Controller](https://docs.kisi.io/access_control/hardware/controllers) sends a valid credential to the legacy controller.
- If any controller receives a valid credential, the door opens.

This integration allows for a smooth transition to Kisi while preserving legacy systems.  

