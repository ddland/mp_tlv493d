# tlv493d_microPython
MicroPython driver for the TLV493D sensor. Based on the [Adafruit circuitpython](https://github.com/adafruit/Adafruit_CircuitPython_TLV493D) library.

Example code:

```python
from machine import Pin, I2C
import time
import tlv493d

i2c = I2C(0, scl=Pin(1), sda=Pin(0), freq=400000)
tlv = tlv493d.TLV493D(i2c)
print(tlv.temperature())
while True:
    print("X: %s, Y: %s, Z: %s uT" % tlv.magnetic)
    time.sleep(0.1)
```

