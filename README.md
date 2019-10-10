# circuitpython-dfplayer

Micropython implementation of DFPlayer from (PLdeSousa/micropython-dfplayer) ported to CircuitPython (4.1)

Only dfplayer.py was ported

![alt text](550px-Miniplayer_pin_map.png)

* DFPlayer Mini     => e.g. Adafruit ItsyBitsy M4 
    * VCC           => 3.3V 
    * All GND pins  => GND
    * Busy Pin      => A5
    * RX Pin        => A2
    * TX Pin        => A3
    * SPK1+SPK2 to a 3W speaker (limiting the volume to 0.5 can help prevent brownout for larger wattage speakers)
    * ...or...
    * DAC_R+DAC_L to a 3.5mm Line Out Jack
    
    
 Songs are organized in folders named: 1,2,3 etc.
 Songs within  a folder similarly: 1.mp3, 2.mp3 etc.
 
 Example usage:
 ```import board
    import dfplayer
    import time
    
    busy_pin = digitalio.DigitalInOut(board.A5)
    player_uart = busio.UART(board.A2, board.A3, baudrate=9600)
    player = dfplayer.Player(busy_pin=busy_pin, uart=player_uart)
    print("Folder count", player.query_folders())
    print("Songs in folder 1", player.query_filesInfolder(1))
    player.play(1,1)
    while player.playing():
        time.sleep(0.5)
 ```
    
    




