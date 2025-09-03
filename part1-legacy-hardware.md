## Part 1: Kisi + Legacy Hardware Integration
### Installation of a legacy reader alongside a Kisi Reader to a Kisi controller
- At the door, [wire the Kisi Reader](https://docs.kisi.io/access_control/hardware/readers/kisi_reader_pro_2_1/wire_reader_pro_2_1) to the [Kisi controller](https://docs.kisi.io/access_control/hardware/controllers)’s reader interface.
- Also connect the **legacy reader** to a [Wiegand channel](https://docs.kisi.io/access_control/hardware/controllers/kisi_wiegand_board/wire_legacy_hardware) set to `READER` mode.
- The **Kisi Controller** will receive credentials from both readers.
- If *either* reader provides a valid credential, the controller unlocks the door.

### Installation of Kisi controller allongside a legacy controller
- Keep the **legacy controller** wired to the door.  
- Connect the [Kisi Controller](https://docs.kisi.io/access_control/hardware/controllers) via its [Wiegand board](https://docs.kisi.io/access_control/hardware/controllers/kisi_wiegand_board/wire_legacy_hardware) in `CONTRL` mode.  
- When a user authenticates through Kisi (tap to unlock excluded), the Kisi Controller sends a valid credential signal to the legacy controller.  
- The legacy controller then opens the door.  

This allows Kisi to provide a simple transition while preserving the existing legacy systems.  

