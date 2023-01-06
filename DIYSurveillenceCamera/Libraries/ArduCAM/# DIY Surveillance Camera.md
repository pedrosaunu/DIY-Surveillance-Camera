# DIY Surveillance Camera

## Materials:

- ESP8266 microcontroller: $5
- Power bank or wall adapter: free
- Arducam OV2640 2MP camera: $30
- Female-female jumper wires: $2
- Box: free
- Micro USB cable: free

**Total cost: $22**

## Software needed:
- Arduino IDE

## Files needed:
- Zipped folder with code file and required libraries

## Instructions:

### 1. Connecting the ESP8266 and Arducam

#### Pin mapping:
![image of pin mapping](https://cdn.awsli.com.br/600x450/535/535286/produto/24837717/9fc4b7faa6.jpg)

| Arducam OV2640 2MP | ESP8266 |
| ------------------- | ------  |
| VCC                | 3.3V    |
| GND                | GND     |
| SDA                | D2      |
| SCL                | D1      |
| PWDN               | D6      |
| RESET              | D8      |
| XCLK               | D0      |
| VSYNC              | D5      |

### 2. Installing the Arduino IDE
![image of Arduino IDE download page](https://cdn.awsli.com.br/600x450/535/535286/produto/24837717/9fc4b7faa6.jpg)

### 3. Installing the ESP8266 board files
![image of Arduino IDE Preferences window](https://cdn.awsli.com.br/600x450/535/535286/produto/24837717/9fc4b7faa6.jpg)

- In Arduino IDE, go to File > Preferences.
- In Additional Boards Manager URLs, enter "http://arduino.esp8266.com/stable/package_esp8266com_index.json".

![image of Arduino IDE Boards Manager](https://cdn.awsli.com.br/600x450/535/535286/produto/24837717/9fc4b7faa6.jpg)

- In Arduino IDE, go to Tools > Board > Boards Manager.
- In Boards Manager, search for "esp8266" and install the package.

### 4. Installing the required libraries
![image of Arduino IDE Sketch menu](https://cdn.awsli.com.br/600x450/535/535286/produto/24837717/9fc4b7faa6.jpg)

- In Arduino IDE, go to Sketch > Include Library > Add .ZIP Library.

![image of Arduino IDE Add .ZIP Library window](https://cdn.awsli.com.br/600x450/535/535286/produto/24837717/9fc4b7faa6.jpg)

- Select the downloaded zipped folder, and click "Open".
- In Arduino IDE, go to Sketch > Include Library, and select "ArduCAM", "UTFT4ArduCAM_SPI", and "ESP8266-Websocket".

### 5. Editing the WiFi credentials
![image of code file with WiFi credentials](https://cdn.awsli.com.br/600x450/535/535286/produto/24837717/9fc4b7faa6.jpg)

- In the code file, find the ssid and password arrays.
- Replace the default values with your own WiFi credentials.

### 6. Uploading the code
- In Arduino IDE, go to File > Open.
- Select the code file from the downloaded zipped folder and click "Open".
- In Arduino IDE, go to Tools > Board and select "NodeMCU 1.0 (ESP-12E Module)".
- In Arduino IDE, go to Tools > Port and select the port to which the ESP8266 is connected.
- In Arduino IDE, click the Upload button.

### 7. Connecting the power source
- Connect the ESP8266 to a power source using a micro USB cable.
![image of micro USB cable connected to ESP8266](https://cdn.awsli.com.br/600x450/535/535286/produto/24837717/9fc4b7faa6.jpg)

### 8. Accessing the camera
- Connect to the same WiFi network as the ESP8266.
- Access the camera's video stream at http://192.168.23.12/stream.
- Access the camera's photo capture at http://192.168.23.12/capture.
![image of video stream accessed through web browser](https://cdn.awsli.com.br/600x450/535/535286/produto/24837717/9fc4b7faa6.jpg)

## Additional notes:
- The camera's video stream and photo capture can only be accessed within the same WiFi network as the ESP8266.
- The ESP8266 can be powered by a power bank or a wall adapter.
- The code file can be modified to add more WiFi credentials or to change the static IP of the camera.
- The code file can be found in the downloaded zipped folder, inside the "src" folder.
- The required libraries can be found in the downloaded zipped folder, inside the "libraries" folder.
- The Arduino libraries folder is usually located in Documents/Arduino/libraries. If you have trouble installing the libraries, you can copy the "ArduCAM", "UTFT4ArduCAM_SPI", and "ESP8266-Websocket" folders from the downloaded "libraries" folder into the Arduino libraries folder.

