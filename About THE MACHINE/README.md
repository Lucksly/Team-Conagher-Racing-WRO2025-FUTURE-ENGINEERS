About THE MACHINE
====
V. Juan:

This little goofy guy is V. Juan, our first robot for the WRO Future Engineers category.

<img height="256" width="520" src="V. Juan pictures/IMG_1598.jpg">

He's on some sick 52 mm by 26.4 mm 7 spoke rims for 1/10 scale rc cars off Aliexpress which can be bought here (https://www.aliexpress.com/i/1005010007257755.html P.S. DON'T BUY REAL CAR RIMS FROM ALIEXPRESS THEY WILL SHATTER ON YOU):
<img src="V. Juan pictures/IMG_1600.jpg">

He measures in at 8.8 cm in height, 19.2 cm in width and 28.8 cm depth and weighs in at 793.78 grams
<table>
    <tr>
        <td>
            <img src="V. Juan pictures/IMG_1599.jpg"> Front
        </td>
        <td>
            <img src="V. Juan pictures/IMG_1601.jpg"> Right Side
        </td>
                <td>
        <img src="V. Juan pictures/IMG_E1619.JPG"> Rear
        </td>
    </tr>
    <tr>
        <td>
            <img src="V. Juan pictures/IMG_1602.jpg"> Left Side w/ measurements
        </td>
        <td>
            <img src="V. Juan pictures/IMG_1603.jpg"> Top Down w/ measurements
        </td>
                <td>
        <img src="V. Juan pictures/IMG_1604.jpg"> Bottom Up
        </td>
                <td>
        <img src="V. Juan pictures/IMG_1606.jpg"> Chasis without electronic components    
    </tr>
</table>

He's composed of the following electronic parts:
<table>
    <tr>
        <td>
            <img src="component images/S.P. Hub.png"> Lego Spike Prime Hub
        </td>
        <td>
             Placed at the back of THE MACHINE atop the differential, it's the heart of our MACHINE.
        </td>
                <td>
        </td>
    </tr>
    <tr>
        <td>
            <img src="component images/Battery.png"> Lego Spike Prime Hub Battery
        </td>
        <td>
            A lithium ion recharable battery that powers the entire robot at 7.3v for 2100mAh or 15.4Wh which we have found as enough for now
        </td>
                <td>
    </tr>
    <tr>
        <td>
            <img src="component images/Large Technic Motor.png"> Lego Spike Prime Large Motor
        </td>
        <td>
            Placed in the middle of THE MACHINE to drive it via a technic axle connected to the differential, according to Lego, it generates 8 Ncm of torque at 135 RPM and consumes 430 mA at "maximum efficiency", thanks to the 20 tooth gear at the end of the Technic axle and the 28 tooth gear on the differential, this create an increase in torque at the expense of speed which results in the wheels getting 11.2 Ncm of torque at 96.42 RPM. 
        </td>
                <td>
    </tr><tr>
        <td>
            <img src="component images/Medium Motor.png"> Lego Spike Prime Medium Motor
        </td>
        <td>
            This motor is placed at the front of THE MACHINE, atop the steering arms and is used for steering, it generates 3.5 Ncm of torque at 135 RPM and consumes 280mA according to Lego
        </td>
                <td>
    </tr><tr>
        <td>
            <img src="component images/Color Sensor.png"> Lego Spike Prime Color Sensor
        </td>
        <td>
            Placed at the front of THE MACHINE below the front Ultrasonic distance sensor it's meant to identify the obstacles up to 4 to 6 cm from our testing and a sample rate of 100hz to relay that information to the hub to then decide what to do.
        </td>
                <td>
    </tr><tr>
        <td>
            <img src="component images/ultrasonic distance sensor.png"> Lego Spike Prime Ultrasonic Distance Sensor
        </td>
        <td>
            One placed at the front and one at both left and right sides for wall detection and obstacle avoiding, it can detect objects for 200 cm and has a sample rate of 100 Hz
        </td>
                <td>
    </tr>
</table>
Source: https://education.lego.com/en-us/product-resources/spike-prime/downloads/technical-specifications/ 

V. Chew:

This, is THE MACHINE'S evolved state, V. Chew, the changes are few but practical, mainly, he's shorter and is now programed in micropython via pybricks.

<img height="250" width="520" src="V. Chew pictures/IMG_E1810.JPG">

He measures in at 24.5 cm long, 19.5 cm wide and 10.5 cm tall he's equiped with the same wheels and electronic components as V. Juan, so they aren't that different from one another.

<table>
    <tr>
        <td>
            <img src="V. Chew pictures/IMG_E1811.JPG"> Front
        </td>
        <td>
            <img src="V. Chew pictures/IMG_E1812.JPG"> Right Side
        </td>
                <td>
        <img src="V. Chew pictures/IMG_E1813.JPG"> Rear
        </td>
    </tr>
    <tr>
        <td>
            <img src="V. Chew pictures/IMG_E1814.JPG"> Left Side 
        </td>
        <td>
            <img src="V. Chew pictures/IMG_E1815.JPG"> Top Down 
        </td>
                <td>
        <img src="V. Chew pictures/IMG_E1816.JPG"> Bottom Up
        </td>  
    </tr>
</table>

V. Chew Upgrades
===
The measurements haven't changed, although some components have been changed:

Wheels:
    
We now use 3d printed Enkei RPF1 rims for weight saving purposes which can be found [here](https://cults3d.com/en/3d-model/game/1-10-rc-rim-rpf1)

Electronics:

We have removed the Lego Spike Color Sensor due to its limited range, in its place originally there was going to be a [Cytron Maker Pi RP2040](https://www.cytron.io/p-maker-pi-rp2040-simplifying-robotics-with-raspberry-pi-rp2040) but the one we had sourced from our coach had a missing grove port, and we had attempted to use a different grove port to have [UART](https://docs.micropython.org/en/latest/reference/glossary.html#term-UART) but the GP0 pad started lifting from the side that was connected to the trace so we decided to instead use a [Raspberry Pi Pico 2](https://www.raspberrypi.com/products/raspberry-pi-pico-2/) provided by our coach, which we might mount to the robot using Cytron's [Robo Pico](https://www.cytron.io/p-robo-pico) but also means that THE MACHINE'S full name is now S.P.P2. V. sChew, but we just call him V. Chew cause why not. Currentlly in testing we've been using the Pico2 with a [APDS-9960](https://learn.sparkfun.com/tutorials/apds-9960-rgb-and-gesture-sensor-hookup-guide/all) conmected via [I2C](https://docs.micropython.org/en/latest/library/machine.I2C.html) which was also provided by our coach although we are considering a camera so we can have higher accuracy for detecing obstacles and the parking.

Prototype:

V. Chew R(udolf), in this version of V. Chew, we have managed to get the Lego Spike Hub to communicate effectively with the [Cytron Maker Pi RP2040](https://www.cytron.io/p-maker-pi-rp2040-simplifying-robotics-with-raspberry-pi-rp2040), which now rests under the Hub, hopefully, will give it a chance at revival as a part of our machine. This version still uses our new color sensor, the [APDS-9960](https://learn.sparkfun.com/tutorials/apds-9960-rgb-and-gesture-sensor-hookup-guide/all). Besides that, we've called this prototype version of V. Chew, V. Chew R(udolf) 'cause the [APDS-9960](https://learn.sparkfun.com/tutorials/apds-9960-rgb-and-gesture-sensor-hookup-guide/all) color sensor, which is RED, is placed right in the front of our distance sensor, makin' it look like a Rudolf's nose. The reason we put the color sensor there is to make use of the distance sensor's LED light to further increase our color sensor's accuracy.