# Hoymiles Cloud Integration for Home Assistant

This custom integration for Home Assistant is based on https://github.com/Philra94/homeassistant-hoymiles-cloud and allows you to monitor and read your Hoymiles solar inverter systems via the Hoymiles Cloud API. It was optimized for monitoring without controls.

## Installation

### HACS (Recommended)

1. Make sure you have [HACS](https://hacs.xyz/) installed
2. Go to HACS → Integrations → Plus Icon → "Add Custom Repository"
3. Enter the URL: `https://github.com/BerndeDGF/ha-hoymiles-cloud`
4. Select category: "Integration"
5. Click "Add"
6. Find and install "Hoymiles Cloud"
7. Restart Home Assistant

### Manual Installation

1. Download this repository
2. Copy the `custom_components/ha_hoymiles_cloud` directory to your Home Assistant `custom_components` directory
3. Restart Home Assistant

## Configuration

1. Go to Home Assistant → Settings → Devices & Services → Add Integration
2. Search for "Hoymiles Cloud"
3. Enter your Hoymiles Cloud login credentials (same as used in the S-Miles Cloud app/website)
4. Click "Submit"

## Usage

After configuration, the integration will create:

- A device for each Hoymiles station with sensors for power, energy, and battery levels
- Controls for battery mode and reserve capacity settings

The sensors will update every minute by default, but this can be changed in the integration options.

## Notes

- Password encryption/hashing is simplified in this version. For production use, it should be properly implemented according to the actual encryption method used by Hoymiles.
- Error handling is basic. The integration will log errors but may not handle all error cases gracefully.
- API endpoints and data structures are based on the observed behavior of the official Hoymiles Cloud API as of 2023-2024.

## Contributing

Contributions are welcome! If you have recommendations, improvements, or additions to this repository, please feel free to:
- Open an issue with your suggestions
- Create a pull request with your changes
- Share your feedback on what could be improved

Please note that this code was developed with the assistance of AI, which may explain why some parts are not always the prettiest or most straightforward. Your help in improving and refining the codebase would be greatly appreciated.

## Troubleshooting

- Check Home Assistant logs for details about any errors
- Verify your Hoymiles Cloud credentials
- Ensure your Home Assistant instance has internet access to reach the Hoymiles Cloud API

## Support

For bugs or feature requests, please [open an issue on GitHub](https://github.com/BerndeDGF/ha-hoymiles-cloud/issues).

## Disclaimer

This integration is not affiliated with, endorsed by, or connected to Hoymiles Power Electronics Inc. This is a third-party integration developed for personal use. 