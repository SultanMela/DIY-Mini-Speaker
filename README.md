# DIY-Mini-Speaker
I created a mini speaker using a broken Alexa Echo Pop speaker.

One morning, I woke up and found out that my Alexa Echo Pop had corrupted itself overnight, ikely due to a power outage while it was updating. Instead of throwing it away, I saw this as a great opportunity to build a DIY AirPlay speaker.

I was able to get a Raspberry Pi Zero 2W from my university for this project, and I also ordered a MAX98357A class D amplifier. The reason I choose the MAX98357A is because from my research I was able to find that it supported speakers up to 4 ohms 3 watts, and the salvaged Echo Pop speaker I measured to be 6 ohms, this made it the perfect fit. 

# Salvaging the speaker
I first started by finding the polarity of the speaker, I did this by supplying 1.5 volts to the speaker's connection, the way I knew the polarity was correct is when the speaker pushed out instead of in. Once I knew the polarity of the speaker, I soldered on corresponding red(positive) and black(negaitve) wires. Once that was done, I waited for my Max98357A to arrive. 

# Amp Setup
Once the amp had arrived I started by soldering on the pins, once I had done that I went through and did a continutiy test for both the amp and speaker to make sure everything was solid. I found out when I was doing the conunity test for the amp, that it was defective from the factory, after getting a replacement I was able to get continue.

# Wiring
Once I had that done, I started researching the wiring diagram for connecting the amp and the Raspberry Pi. I was able to use an decrapted guide from Adafruit (https://learn.adafruit.com/adafruit-max98357-i2s-class-d-mono-amp/raspberry-pi-usage) to figure out the correct wiring for the amp and the raspberry pi.

<img width="470" alt="Amplifier Wiring" src="https://github.com/user-attachments/assets/f04d6f7d-2fa6-4a76-8cb1-7781bc0b6ede" />

# Configuration and Shairport-Sync
I was able to edit the asound.conf file to define the speaker, I then also configured the boot configuration to have the raspberry pi recognize that he amp was connected. I then rebooted. Once the raspberry pi was on again, I procedded to install shairport-sync (https://github.com/mikebrady/shairport-sync/blob/master/BUILD.md) using the steps that they provide. 

Once shairport-sync was installed, I realized that I couldn't control the volume when I was airplaying to the speaker. To fix this, I decided to configure the shairport-sync configuration file to give it exclusive access to the speaker. Once this was done, I restarted and the issue was fixed.


# The completed product
The speaker was now working great without any problems, I am currently working make a case for it on Solidworks in order to safely house it. I have attached a picture below of the completed product.

<img width="459" alt="The finished product" src="https://github.com/user-attachments/assets/23b8c502-2085-4baa-b9e6-dcd133dddaf5" />



