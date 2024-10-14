\page esp32_upload Uploading Code to ESP32-S3

## Suggested Prerequisites

- VSCode IDE
- PlatformIO VSCode Extension
- Optional: Git

## Downloading the Code

- Download the code from the [GitHub repository](https://github.com/ricardo2000y/VLC-with-encryption-esp32.git) and unzip the folder to your desired location
- Or clone the repository using Git by running the following command in your terminal:

```bash git clone https://github.com/ricardo2000y/VLC-with-encryption-esp32.git ```

## Suggested Uploading Method

1. Connect your ESP32-S3 to your computer
2. Open VSCode on the project folder, or select the project in the PlatformIO home screen
3. Select the correct port
4. Click 'Upload' in the PlatformIO toolbar (or use the shortcut `Ctrl+Alt+U`)

\note Ensure your ESP32-S3 is in bootloader mode before uploading.

## Troubleshooting

If you encounter issues:
- Check your cable connection
- Verify the correct port is selected
- Change the port being used in the ESP32-S3 if necessary (applies to some boards, that have UART and USB ports)
- Verify if the dependencies for the PlatformIO extension are correctly installed