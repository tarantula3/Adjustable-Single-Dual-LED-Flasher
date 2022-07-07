# Adjustable-Single-Dual-LED-Flasher
[![B1URFJywtcI](https://img.youtube.com/vi/B1URFJywtcI/0.jpg)](https://www.youtube.com/watch?v=B1URFJywtcI)

The 555 timer IC is an integrated circuit that is used in a variety of timer circuits, pulse generators and oscillator applications. The heart of the tutorial is the 555 timer IC that is wired as an astable multivibrator.


In this tutorial, I'll first blink "an LED" using the positive pulse generated by a "DIY 555 Pulse Generator Module" (video: https://youtu.be/bMAnipPOjFo), followed by "two LEDs" alternating and flashing at a regular interval. The output frequency of pulses can be adjusted using a potentiometer. The circuit can be operated from any voltage between 5 to 15 volt DC.

Watch this video for detailed step by step instructions on how to build this circuit and for a complete instruction on how the circuit works.

Video: https://youtu.be/B1URFJywtcI


# Items Required
![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjEbDvz79SJKI94praHSE-A_DDj3Z-TTaxglEytbpD5Y67e29j2J276YX2c_W5TMc6RDD32ZoyM1454S2ufThfquP0aofdDXrQ_Ykbx-QDLwG4LZw0r_8fnHvVQUF6IKkt0ant-_7UpA2heIleZi4-v7psyJKlR2KNfixUQx0Eqdo81s2vDHaneo6nfnA/w640-h360/03.png)

For this tutorial we need:

- 2 x LEDs
- 1 x 555 Timer IC
- 1 x 10µF Capacitor
- 1 x 220Ω Resistor
- 1 x 1kΩ Resistor
- 1 x 10kΩ Resistor and/or
- 1 x 10kΩ Potentiometer 


# Circuit Diagram
![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjckFiGYicp8o0M0UUD-_fDigOJmXHdpaltqEuyJ6W0gYscOFz3NjjH_42MqEVdXMZQBPk1cJBv8VzT_eSNXuTZg818p7ta6SMdvdBVmkLMLu91EdqJzcgMSC63ySitpX4G_jaNxSu1myhGSqbY-fkgQupGYIxF8cnC8xrFhfYP0kvU95ODxnnC-ib9uA/w640-h360/04.png)

The circuit is very simple.

By connecting Pin 2 and 6 of the 555 timer IC, we put the IC in astable mode. In astable mode, the 555 timer IC acts as an oscillator (re-triggering itself) generating square waves [PWM Signals] from the output pin no. 3.

By changing the values of R1, R2, and C1 we can change the frequency of the output pulses generated at pin number 3.

Alright, let me explain this with the help of an animation.


# How The Circuit Works
![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgsGdQW1O6GDDBN77tbNLSowCocaF6Mt5O11Lbp4-7-R0avZtE89L8JUiUC3u_vLj5E8sgTT8SMpO6GOJ0alma1b5Gb3K0Qu-9nXI5lzSBb3_kLHozLJxeQpT8a4JqQNiNFC3T7At7Z6JXKPG5ZhmzLvT_ZQYch4ZV9KioyORo_hFTYVmf3vXORDYfnFA/w640-h360/04.png)

- When Pin 2 of the IC detects voltage LESS than 1/3rd of the supply voltage, it turns ON the output.
- And, when Pin 6 detects voltage MORE than 2/3rds of the supply voltage, it turns OFF the output.
- When the output is OFF, the Discharge Pin (Pin7) gets internally Grounded.
This is how the trigger pin (Pin2) and the threshold pin (Pin6) of the 555 timer IC sense voltages and controls the output at Pin 3.

![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEggw-k7IlwDvJCjebAZlpBmaDZ7u3H9F241g8ENmrTeYqThhR7s5PK2stI53AqXFRJziM6yFWNavW7VJ6PXRdE0ko_xtMhtBlnrn-4aCdCPvDzlLxFIjiUI6ww0J8fqNy0FYTGZg-jQZg4qb8vEgypTttUh0B2QG_1suyo_ep5MrYk-t_hWkZIhcYViqg/w640-h360/05.png)

- Capacitor C1 will be in a discharged state immediately when we firing up the circuit. 
- So, the voltage at Pin 2 will be 0v which is less than 1/3rds of the supply voltage, this will turn ON the output on Pin 3.
- At the same time Pin 7 will internally disconnect from the GND and the Capacitor C1 will start changing via resistors R1 and R2.
- Once the voltage across capacitor C1 crosses 2/3rds of the supply voltage, Pin 6 turns OFF the output.
- At the same time Pin 7 will internally reconnect to the GND causing the capacitor C1 to discharge via resistor R1.

![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg-u65jZe6d_9LD_RGbArW3E4QO6l1hXWu1OmeajdENSfCa7PleXE1wY60fhFIMPBHXuUIbYcLm3CnUNPc8Xx0lPTzKy3LpUU6hfQ8jYB8l7ZXyrWIP-kx2hMir8fSyTOIJfNm-jQyoygrhtHDtD-TRVPAezKv_FBCMcxkm6_1bPHT7UCrfF8DBtXJ7iA/w640-h360/06.png)

- Once the voltage across the capacitor C1 falls below 1/3rd of the supply voltage, Pin 2 turns ON the output, and the above cycle keeps repeating itself.

You can hook up a multimeter to the circuit to measure the charging and discharging of the capacitor.

Since resistance R1 is involved in both charging and discharging of the Capacitor, increasing or decreasing its value will increase or decrease the duration of the OFF cycle and will decrease or increase the flashing rate of the LED, as the capacitor will take more time to charge and discharge.

By replacing the capacitor with a higher or lower value, you can also get a longer or shorter flashing rate.

By replacing the resistor R1 with a potentiometer the blinking rate of the LED can be dynamically adjusted.
![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh5aAMCtQ0L-2kuxqtpHPHqbQskaiCv-Ffle0AZ-3xIzSxSua8JC1r21xCfgnDaAVhZbPZ095MX5qSgR-K7GM1wG4JBIrRhtedVgnhOHzu1HGKrJDfUezzigRA9Bg90eX1DG8-5CRVfXqYJuhVUl0MAfvwE8WboK9kagQG6ZA8dfOisA0_NA_ovoIvwnQ/w640-h360/07.png)

Now, for the Dual LED flashing effect we need to connect a second LED with opposite polarity to the Pin 3 of the IC. That's it, as easy as that.


# Calculations
![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhItwdSPgFLgWZMX6fhEmn3n60dt_vtf-PjyMD43XbETlOk737lmR-shYH2QqcsspnXY4gxbnErtZWJbKfbhBgRznej1z8AfQCufqC_z_jLv5ZhDdP5hGjM0YL9XSGkxl5ZeYL5JPpsc-wJAFIIH9keOTtdfT4rE9tWrX3jUjI7EhqHcu1SCiIJnSrT-g/w640-h360/08.png)

Now, lets calculate the output frequency and the duty cycle of the output waveform. 

In my setup I have resistance R1 = 1kΩ, R2 = 10kΩ and capacitor C = 10uF

There are many online calculators to calculate this online. I will provide a link to one of the astable calculators in the description below: https://ohmslawcalculator.com/555-astable-calculator

Lets first calculate the value of t1 or the 'capacitor charge “ON” time which is 0.693(R1 + R2 ) * C1. Putting the values together we get 76.23 milliseconds. 

Now, for capacitor discharge “OFF” time or t2 we need to multiply 0.693 to R2 and C1, which then gives us a value of 69.3 milliseconds.
Next, the total periodic time T is equal to t1 + t2 which comes out to be 145.53 milliseconds.

The output frequency, ƒ is therefore comes out to be to 6.871Hz.

Which gives a duty cycle value of 52.38% 

If you want to have more control over the charging and discharging use a higher value for R2 (100K) and lower value for R1 (1K). That way you will have 99% control over the charging and discharging resistance in the circuit.

The maximum output current of this IC is 200mA therefore to drive a higher current load of up to 1A we have to use a transistor like the BD135.


# The Board
![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhDstXz0mrVPIW28nDmleRjdoIZwhx2CMa3IALXShGB6F-wKI8iloiGO9PMg0E-rVgSQDEA88VSVchfCYMBlNTc6h1jPH9DWwnWGhkF_XwBCObUWIVdw5osQIELW7tWNnGPu87ycj6tX4AXXGC7dVjE0OSQrSruqGjs_SrB3z3V6Nye5yuwBy3Tuc1dsg/w640-h360/10.png)

To make it easy for you guys, I have created this tiny little "555 Pulse Generator Module". After assembling the components, you just need to power this module by providing a voltage between 5v to 15v to get an oscillating output at the "Pulse" pin.

So, this is how my board looks like in 2D and 3D. There are 16 breakout boards in this 100cm x 100cm assembly. You can download the gerber file from the link provided in the description below and order it from PCBWay.


# Soldering
![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg39Svdw0j4gWAagepaH18PWsqhefGb-bDhM12QEgN94WeM7FvkGQuzcF13KHSrWvClTPWC83boAj25IYEGM2hktc_6Bb29PlAKzFhx7-D_XRnZT3Wi-bGCrjPk67HQSgJbxQJg9XR4s9hLGQfGvGm2BZE7JXbJWwnRK5FfReespSEMNtCKBJFM5tZQNA/w640-h360/09.png)

Before moving forward, let me quickly show you guys how to assemble the components to this custom made board.
Let's start by soldering the IC Base to the board. Then let's solder the potentiometer to the board. After that lets solder the 1kΩ (R1) resistor to the board followed by the 10µF capacitor (C1) to the board. Once done, let's insert the 555 timer IC to the IC base.
To conclude I have soldered 3 x Male pin headers to the board.


# Applications and Uses
![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgRqQRLZzj90261SjclXYFFFPCoAaaiElyoSaKxdYhg_nmslsYU9_JRWKnkTHpXobNznmOD4Ppoqp-CgPWlHNwUWEyOF9xp7s0E9LQOQUQ8zoP1tVHpTxC9xXUce7H8KyI0uXYuyNHMv6TbaDdtrPVvEARLppKzMt6FLsPpaI89nsFbzJZYKG2r5RlU9Q/w640-h360/10.png)

- This circuit can be used to control the speed of DC motors and Stepper motors
- It can be used to control windscreen wiper motors to generate a to-and-fro motion
- It can be used as square wave signal generator
- It can be used as an adjustable pulse generator for MCUs
- In Strobe lights and SoS signaling circuits 
- Telecommunications for encoding purposes
- In turning indicator circuits for all types of vehicles and bicycles
- To generate adjustable pulse (timing pulses) to control other circuits. As, in combination with the 4017 & 4026 ICs

![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEggr0BZj5BCg-YV6uG57OP_opFCjGSkUpbQDBrQqDbwElaCSpOuioTLC7ytWh0tu2Zuyo2p8I8FkDZoMClxWxHBM97ldJkc77ZaVb_tA3kmYOP-qMox7FnS1IFUGJX4fYPXYXYNr19ADgryIQEMUq9X1lN4P4AnQbH0xbprbCx511oH2MDr3Z6-a93lcA/w640-h360/11.png)

- I have used this IC in few of my other projects and tutorials like the:
-- DIY - Boba Fett Helmet With LED Chaser Circuit : https://youtu.be/vtO_GD0SS2s
-- LED Chaser Circuits Using IC4017 and Arduino : https://youtu.be/F6V1AjESWbU
-- DIY - LAN CABLE TESTER : https://youtu.be/PSK5Aa-byHA
-- 555 Pulse Generator Module : https://youtu.be/bMAnipPOjFo



# Thanks
[![B1URFJywtcI](https://img.youtube.com/vi/B1URFJywtcI/0.jpg)](https://www.youtube.com/watch?v=B1URFJywtcI)

Thanks again for checking my post. I hope it helps you.

If you want to support me subscribe to my YouTube Channel: https://www.youtube.com/user/tarantula3

Full Blog Post: https://diy-projects4u.blogspot.com/2022/07/555-Dual.html

Video: https://youtu.be/B1URFJywtcI

Related Videos
1. DIY - Boba Fett Helmet With LED Chaser Circuit : https://youtu.be/vtO_GD0SS2s
2. LED Chaser Circuits Using IC4017 and Arduino : https://youtu.be/F6V1AjESWbU
3. DIY - LAN CABLE TESTER : https://youtu.be/PSK5Aa-byHA
4. 555 Pulse Generator Module, How it Works : https://youtu.be/bMAnipPOjFo


Gerber File: https://drive.google.com/file/d/1YE5vznhAcQx2cmlXouRhn2yxZB3Lb2RK/view?usp=sharing

Calculator: https://drive.google.com/file/d/17dTw22opXIw8WI4-knUZu4rr6k-6zlxV/view?usp=sharing

Schema: https://drive.google.com/file/d/1K635sLu-J3UQzEibjANlfm8ywCgy4tJ0/view?usp=sharing



Support My Work
BTC:  1M1PdxVxSTPLoMK91XnvEPksVuAa4J4dDp

LTC:  MQFkVkWimYngMwp5SMuSbMP4ADStjysstm

DOGE: DDe7Fws24zf7acZevoT8uERnmisiHwR5st

ETH:  0x939aa4e13ecb4b46663c8017986abc0d204cde60

BAT:  0x939aa4e13ecb4b46663c8017986abc0d204cde60

LBC:  bZ8ANEJFsd2MNFfpoxBhtFNPboh7PmD7M2

Thanks, ca again in my next tutorial.

