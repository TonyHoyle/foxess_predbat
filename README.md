# foxess_predbat
Package creating entities to help with implementing predbat on fox ess inverters

Predbat requires some entries to be in watts, whereas our inverters use killawatts, so is
package adds converted entties.

# Integration into homeassistant

In configuration.yaml add:

```
homeassistant:
  packages:
    predbat: !include predbatt.yaml
```

# predbat configuraion

example use in apps.yaml:

```
charge_rate:
   - input_number.force_charge_power_w
discharge_rate:
   - input_number.force_discharge_power_w
battery_power:
   - sensor.invbatpower
pv_power:
   - sensor.pv_power_w
load_power:
   - sensor.load_power
soc_kw:
   - sensor.bms_actual_kwh_remaining
soc_percent:
  - sensor.battery_soc
```
