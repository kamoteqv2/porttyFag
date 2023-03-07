## How to Use PorttyFag.exe for Face Recognition
### Overview
PorttyFag.exe is a tool that enables users to use facial recognition to trigger a specific output pin on any microcontroller that supports KMQ firmware. After running the program, a folder called "allow" will be created. This folder is where you should add any images that you want the webcam to recognize and trigger the pin if a match is found. Additionally, a screenshot of the captured image will be saved to a folder called "hit."

### Prerequisites
Before you begin, make sure you have the following:

Windows operating system
A camera connected to your network
A microcontroller that supports KMQ firmware
A command-line interface (CLI)

### Installation
Download the latest release of PorttyFag.exe from the official GitHub repository.
Extract the downloaded zip file to a directory of your choice.
Usage
Open your CLI.
Navigate to the directory where PorttyFag.exe is installed.
Execute the following command:

```
porttyFag.exe --url http://<camera_ip_address>/<api_path>/json/ --camindex <camera_index> --pinnum <pin_number> --facereco
```

Make sure to replace the following values:

<camera_ip_address>: the IP address of your camera
<api_path>: the API path of your camera, which is usually /deadbeeffeed
<camera_index>: the index of your camera
<pin_number>: the number of the pin you want to use
For example:

```
porttyFag.exe --url http://192.168.100.18/deadbeeffeed/json/ --camindex 1 --pinnum 7 --facereco
```

This command will execute PorttyFag.exe and connect to the camera at IP address 192.168.100.18 with an API path of /deadbeeffeed, using camera index 1 and pin number 7. The --facereco flag enables facial recognition.

After executing the command, a folder called "allow" will be created in the same directory as PorttyFag.exe. You can add any images that you want the webcam to recognize to this folder. If a match is found, the program will trigger the specified output pin on the microcontroller and save a screenshot of the captured image to a folder called "hit."

### Troubleshooting
If you encounter any issues with PorttyFag.exe, please refer to the official documentation or file a bug report on the official GitHub repository.

### License
PorttyFag.exe is released under the MIT License.

### Credit:

This application was developed by KMQ Tech TV (https://www.youtube.com/@kamoteqv2), a Youtube channel dedicated to teaching and promoting Free DIY technology.



