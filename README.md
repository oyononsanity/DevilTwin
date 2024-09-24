# DevilTwin

![DevilTwinLogo](https://github.com/user-attachments/assets/a33fdfe6-80a0-4047-8104-9c987f20a9c7)

                                      ![68747470733a2f2f666f7274686562616467652e636f6d2f696d616765732f6261646765732f6d6164652d776974682d632d706c75732d706c75732e737667](https://github.com/user-attachments/assets/f632a9c4-060c-433f-a0f9-dce05c93ffe1)

ESP8266 EvilTwin &amp; deauther all-in-one WiFi pen-testing tools Easy to modify, customize captive portal, and integration with 0.96 inch OLED


About The Project

This project is a development of existing projects such as ZiFi, and M1z23R with the addition of 0.96 inch OLED Display integration, RSSI (received signal strength indication), several changes to captive pages, some fixing and adjustments to the ESP8266 Boards Manager to avoid errors when deauthing, and fixed other issues like the captive portal not opening automatically.

The name of this project is inspired by Zero Two from Darling In The Franxx

Disclaimer
IMPORTANT:

This tool is for testing and educational purposes
Please use this tool for pen-testing purposes on your own network or a network that you have permission for
All consequences of using this tool are the user's responsibility, so DWYOR (Do With Your Own Risk).
I don't take any responsibility for what you do with this program in the future

Conclusion

![ZTDeauth](https://github.com/user-attachments/assets/7bed5373-98f6-4dfd-922a-720bb6ff2b9b)

This tool utilizes the deauth attack, which is used to disconnect devices from their WiFi network. After the client disconnects, this tool creates a clone SSID of the target WiFi.
After that EvilTwin will do his job.

Getting Started

Here are some steps on how to compile this project and a guide for using it.

Untuk intstruksi dalam Bahasa Indonesia silahkan buka halaman ini.

Prerequisites
Here are the things you need to prepare:

ESP8266 Development Board (NodeMCU, Wemos D1 Mini, etc)
Arduino IDE
OLED 0.96” I2C Display (optional)
Project board and some jumper cables (optional)
Installation
Open your Arduino IDE and add Deauther ESP8266 Boards URL in the Additional Board Manager (File > Preferences > Additional Board Manager URLs), then add/paste this URL https://raw.githubusercontent.com/SpacehuhnTech/arduino/main/package_spacehuhn_index.json
or you can refer to the Spacehuhn Deauther ESP8266 Boards installation wiki
Go to Tools > Board > Boards Manager, search deauther and install Deauther ESP8266 Boards
Go To Tools > Board > Deauther ESP8266 Boards (make sure it's Deauther ESP8266 Boards) and select your board.
Because I using NodeMCU, so I choose NodeMCU
Download this ZeroTwin projects, and open the ZeroTwin v1.0.ino - English with Arduino IDE
Go To Tools > Manage Libraries, then type Adafruit SSD1306 in the search box and install the library. (make sure the library is Adafruit SSD1306 by Adafruit)
Choose the correct COM port, click "Upload" to start the compiling process, and upload the source code to the ESP8266 board.
You are done!

Usage

If you don't want to integrate with OLED, you can skip the following step

Diagram

![image](https://github.com/user-attachments/assets/1512cf03-3d6d-4eb0-b1b8-df678a48ee6f)
Or you can use the following table as a reference

Wiring

OLED PIN	ESP8266
VCC	3.3V
GND	GND
SCL	D1
SDA	D2


How to use
After completing the steps above, connect to the SSID named ZeroTwin v1.0 with password zero8888 (you can customize it later)
Wait until the portal page automatically opens, if not opening automatically, go to 192.168.4.1 in your favorite browser
Select the target SSID
Look on att4ck panel and click Start Deauth
After a while, click Start Evil-Twin
The AP's mode will stopped and starting Evil-Twin mode

![image](https://github.com/user-attachments/assets/84be1f82-8716-4137-b714-6faab7858e3a)

The OLED display will show the log and captured events of the tools. If the password entered in the captive portal is true, the clone SSID will disappear, and deauth automatically stop. Then connect to Zero Twin v1.0, the result will appear at the bottom of the pages.
![image](https://github.com/user-attachments/assets/08d0cb36-eef8-48ab-917f-1590e053e9bb)

Customization
You can easily find some variables at the top of the source code, you can doing something such as changing the default SSID and password, customizing the captive portal, etc.

