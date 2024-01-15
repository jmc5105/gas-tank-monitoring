# Home Assistant Propane Tank Level Card

This custom Lovelace card for Home Assistant allows you to visually monitor your propane tank levels. It displays a vector image of a propane tank that changes color from green to red as the tank level decreases.

## Features

- Visual representation of propane tank levels
- Color changes from green (full) to red (empty) based on the tank level
- Customizable vector image for the tank

## Prerequisites

- Home Assistant installation
- A sensor in Home Assistant that tracks the propane tank level

## Installation

1. **Prepare the Vector Image:** Create or find a vector image of a propane tank. Place this image in the `www` folder of your Home Assistant configuration directory.

2. **Create the Custom Card:** Use the provided code template to create a custom Lovelace card. Modify the code as necessary to suit your setup.

3. **Integrate with Home Assistant:** Add the custom card to your Lovelace dashboard by editing your dashboard configuration.

## Configuration

- **Sensor Entity:** Replace `'sensor.gas_tank_level'` in the script with the entity ID of your propane tank level sensor.
- **Customization:** Adjust the dimensions, colors, and other styles in the CSS to match your preferences and setup.

## Usage

Once installed and configured, the card will display the current level of your propane tank. The visual representation will update automatically based on the sensor data.

## Customization Tips

- You can modify the gradient colors and transition points in the CSS to better represent the tank levels.
- Adjust the update interval in the JavaScript code to control how often the card updates.

## Troubleshooting

If the card is not displaying correctly:

- Ensure that the sensor entity is correctly configured and reporting data.
- Check that the vector image path is correct and the image is accessible.
- Verify that the custom card code is correctly integrated into your Lovelace dashboard.

## Support

For support, please refer to the Home Assistant community forums or the documentation for custom Lovelace cards.

## License

This project is open-source and available under the [MIT License](https://opensource.org/licenses/MIT).