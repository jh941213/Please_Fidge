## 1. Introduction  
To reduce food waste and promote various cooking activities by recognizing the contents of the user's refrigerator, recommending possible cooking menus and providing related cooking videos.\

**Expected Benefits**  
- Reduces food waste by efficiently utilizing the remaining ingredients in the refrigerator.
- Helps users easily try different dishes, adding interest and enjoyment to cooking.

---

## 2. Components  
**Raspberry Pi and the Pi Camera**    
Capture the contents of the refrigerator and use object recognition to identify ingredients.  

**Object recognition system**  
Use YOLOv5 to accurately recognize ingredients from images.  

**OpenAI API**   
Recommend possible dishes based on the recognized ingredients.  

**YouTube crawling module**  
Automatically search and fetch YouTube links to cooking videos related to the suggested menu.  

**Telegram notification system**  
Sends menu recommendations and YouTube video links to users in Telegram messages.  

---

## **3. HardWare Setting**
#### Respberry PI 

We utilized Raspberry Pi to power our AI model and create data.  

From the Raspberry homepage, you can save the Raspbian OS to an SD card, boot it, and install the necessary modules.  

#### Camera Module Setting  

You can install the camera module by following the link above.  

**Hardware connection**  

Enable the serial interface: Run sudo raspi-config and select 'Interfacing Options' > 'Serial' to enable hardware serial. 
Write Python code or other code that can send and receive data through the serial port.  
 

#### Raspberry PI Pico (W5100S-EVB-Pico)  


Pico communicates and receives the data inferred by Raspberry Pi 4, and utilizes Ethernet communication to make menu recommendations using chatGPT.  

Connect Ethernet, power and set up the UART to communicate with the Raspberry 4.  

 

#### Hardware connections  

> Connect GPIO pin 14 (TX) of the Raspberry Pi 4 to the UART RX pin of the Pico.  
> Connect GPIO pin 15 (RX) of the Raspberry Pi 4 to the UART TX pin of the Pico.  
> Connect the GND pins of both boards to each other.

## **4. Software Setting**
  
### YOLOv5  
![splash (1)](https://github.com/jh941213/Please_Fidge/assets/112835087/7c2910a7-38ec-4fe8-bcc9-8b1586c422fd)
```python
!git clone https://github.com/jh941213/Please_Fidge.git
cd RasberryPI4
!git clone https://github.com/ultralytics/yolov5.git
```
```python
#terminal
python camera.py
```
Open a terminal and run camera.py to detect objects. Once detected, press Ctrl + C to exit the terminal.

```

```
