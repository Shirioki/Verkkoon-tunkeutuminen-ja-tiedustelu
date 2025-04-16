# h3 Aaltoja harjaamassa

## x) Read and summarize.

### Hubacek 2019: Universal Radio Hacker SDR Tutorial on 433 MHz radio plugs

- In the video they use universal radio hacker (URH) to analyze different signals.

### Cornelius 2022: Decode 433.92 MHz weather station data

-  Explains how to decode 433 MHz ASK (Amplitude Shift Keying) signals, used in low-power communication devices like remote controls and alarms.
-  Basic principles about ASK modulation
  -  how to capture the signal using a software-defined radio.
  -  how to process the data to decode the transmitted information.

## a) WebSDR

To start i visited the website websdr.org and chose 

![image](https://github.com/user-attachments/assets/2e634255-ee9b-4179-8136-792a8c5f8d65)

When you open the website there will be a pop up saying Start SDR and after clicking this I heard muzzling noises. After a while when i was looking for better signal so that i could hear something other than the muzzling i found a strong signal which had chinese music playing even thought this is brazilian radio.

![image](https://github.com/user-attachments/assets/f66a7a7d-ffaf-49f0-87f8-9a9d63e51728)


## b) rtl_433

I opened terminal and with wrote a command sudo apt-get install rtl-433 


After installing rtl_433 i tried to open the software with command rtl_433 - h

<img width="896" alt="image" src="https://github.com/user-attachments/assets/927359ad-50c2-4b32-b2ed-64411a21517c" />

It works!

## c) Automaattinen analyysi

To start the next exercise first i downloaded the file that was given in the exercise. After this with command rtl_433 Converted_433.92M_2000k.cs8 the file should open in our software.

<img width="871" alt="image" src="https://github.com/user-attachments/assets/00da4682-b2df-46f1-a014-c73720afe72f" />

The ids that i found from the signals were 8785315 and models i found was KlikAanKlikUit-switch, Proove-security and nexa security. In the sample file devices receive signals or sends signals in channel 3. 
