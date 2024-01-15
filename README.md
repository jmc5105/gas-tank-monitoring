# Propane Tank Level Lovelace Card

This custom Lovelace card for Home Assistant allows you to visually monitor the level of your propane tank using different images based on the current level.

## Features

- Displays a visual representation of your propane tank level.
- Updates the image based on the current level of the tank.
- Easy to configure with your existing Home Assistant setup.

## Prerequisites

- Home Assistant installed and running.
- A sensor in Home Assistant that tracks the propane tank level.
- Images for different tank levels stored in the `www` folder of your Home Assistant configuration.

## Installation

1. **Prepare Images**: Place your tank level images (`full-tank.png`, `empty-tank.png`, `15-percent.png`, etc.) in the `www` folder of your Home Assistant configuration directory.

2. **Sensor Setup**: Ensure you have a sensor entity in Home Assistant that accurately reflects the gas tank level.

3. **Lovelace Card Configuration**: Add the custom Lovelace card configuration to your dashboard. Refer to the example YAML configuration provided.

## Configuration

Here's an example YAML configuration for the Lovelace card:

```yaml
type: vertical-stack
cards:

  - type: conditional
    conditions:
      - entity: sensor.gas_tank_level
        above: 80
    card:
      type: picture
      image: /local/full-tank.png

  # ... additional conditions and cards for each level ...

  - type: conditional
    conditions:
      - entity: sensor.gas_tank_level
        below: 1
    card:
      type: picture
      image: /local/empty-tank.png
```

## Usage

After setting up the card, it will automatically update to display the image corresponding to the current level of your propane tank as reported by the sensor. Ensure that the sensor entity is correctly configured and reporting accurate data.

## Support

For any issues or questions, refer to the Home Assistant community forums or documentation.

