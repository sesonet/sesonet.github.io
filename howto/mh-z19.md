## MH-Z19 CO_2 and Temperature Sensor
* [ESPHOME](https://esphome.io/components/sensor/mhz19.html)

## Pins + uart bus
* D16 -> RX
* D17 -> TX
* 3.3V -> 2-6V
* GND -> GND

## ESPHOME

```yaml
uart:
  rx_pin: 16
  tx_pin: 17
  baud_rate: 9600

sensor:
  - platform: mhz19
    co2:
      name: "MH-Z19 CO2 Value"
    temperature:
      name: "MH-Z19 Temperature"
    update_interval: 60s
    automatic_baseline_calibration: false
```

