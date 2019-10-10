# circuitpython-dfplayer

Micropython implementation of DFPlayer from (PLdeSousa/micropython-dfplayer) ported to CircuitPython

Only dfplayer.py was ported

![alt text](550px-Miniplayer_pin_map.png)

* DFPlayer Mini
    * VCC           => 5V Vin
    * All GND pins  => GND
    * Busy Pin (immediately opposite VCC) => GPIO2 (NodeMCU D3)
    * RX Pin (immediately below VCC)      => GPIO0 (NodeMCU D4)
    * SPK1+SPK2 to a 3W speaker (limiting the volume to 0.5 can help prevent brownout for larger wattage speakers)
    * ...or...
    * DAC_R+DAC_L to a 3.5mm Line Out Jack




