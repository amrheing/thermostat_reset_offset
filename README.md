# thermostat_reset_offset
Resets the Thermostat offset in Problems

sometimes the offset will not set correct - no idea why at this time

then you can call this script manual as automation and it will be resetted to Offset 0.

in behavior of the need for set_offset script there will also set the temp data to 0.

```yaml
- id: 'schlafzimmer_thermostat_reset_offset'
  alias: Schlafzimmer Thermostat Reset Offset 
  description: ''
  trigger: []
  condition: []
  action:
  - service: python_script.thermostat_reset_offset
    data:
      climate_entity: climate.thermostat_schlafzimmer_rechts
      current_offset: input_number.sz_current_offset_rechts
  mode: single
  ```
