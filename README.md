10inch-player

A 10 inch width HiFi music player with 7.84 touchscreen.

## Introduction

I have an old set of Denon speakers that can only play CDs and tapes, which is outdated. This has inspired me to come up with an idea. 

I plan to use Volumio as a digital playback system and hope that the appearance is as good-looking as possible, while keeping the cost low.


This is the effect of placing the DIY finished product next to the Denon speaker. It looks pretty durable, doesn't it?

![10inch HiFi Player](./image/07.jpg ':size=400x')

## System Description

![10inch HiFi Player](./image/system.png ':size=400x')

## Rendering

![10inch HiFi Player](./image/rendering/10inch-player.49.jpeg ':size=400x')

![10inch HiFi Player](./image/rendering/10inch-player.50.jpeg ':size=400x')

![10inch HiFi Player](./image/rendering/10inch-player.51.jpeg ':size=400x')

![10inch HiFi Player](./image/rendering/10inch-player.52.jpeg ':size=400x')

![10inch HiFi Player](./image/rendering/10inch-player.53.jpeg ':size=400x')

![10inch HiFi Player](./image/rendering/10inch-player.54.jpeg ':size=400x')

## Case

The 10inch-Player case is made up of three materials: aluminum profile, acrylic, and 3D printed parts, along with some screws and foot pads.

![10inch HiFi Player](./image/03.jpg ':size=400x')

## Exploded-view

![10inch HiFi Player](./image/01.jpg ':size=400x')


## 7.84 Touchscreen

Purchase Link: [https://store.wisdpi.com/products/7-84inch-ips-long-strip-capacitive-touch-screen-lcd-400-1280-hdmi-ips-toughened-glass-cover-support-raspberry-pi](https://store.wisdpi.com/products/7-84inch-ips-long-strip-capacitive-touch-screen-lcd-400-1280-hdmi-ips-toughened-glass-cover-support-raspberry-pi)

At first I wanted to choose the waveshare screen, but then I found that the waveshare screen was not suitable for this structure and could not be used. Then I found this touchscreen from wisdPi. They use the same software. And this screen panel and driver board is independent, more suitable for diy installation

The 7.84-inch touch screen is glued to the 3D-printed bracket and then slid into the aluminum profile for fixation.

![10inch HiFi Player](./image/05.jpg ':size=400x')



## Internal circuit board

![10inch HiFi Player](./image/02.jpg ':size=400x')

### HDMI to MIPI board

This is the driver board for 7.84 LCD. It's a part of 7.84 Touchscreen.

### Raspberry Pi 3B+
For Volumio, I think RPi 3B+ is more suitable because it is much cheaper, has sufficient performance, and supports Bluetooth and 5G Wifi.

### wisdPi HiFi DAC 

Purchase Link: [https://www.amazon.com/wisdPi-Raspberry-PCM5122-Reduction-External/dp/B0C3CMCM7V/ref=sr_1_10?keywords=hifi+dac+hat&qid=1684993494&sr=8-10](https://www.amazon.com/wisdPi-Raspberry-PCM5122-Reduction-External/dp/B0C3CMCM7V/ref=sr_1_10?keywords=hifi+dac+hat&qid=1684993494&sr=8-10)

There are many HiFi DACs, but I choose the one from wisdPi.

This HAT has an active power noise reduction function, and I can use a cheaper power adapter.

Also it has an external power interface, next I will try to use a low power linear power supply to power the dac alone, which is cheaper than using a linear power supply to power the whole system. Also I can try to power the DAC directly with a battery.

### Sumolink Erhu RP2040

Purchase Link: [https://www.temu.com/sumolink-erhu-rp2040-pico-like-mcu-board-based-on-raspberry-pi-rp2040-chip-dual-core-arm-cortex-m0-processor-up-to-133-mhz-onboard-4mb-flash-usb-c-connector-g-601099517031753.html?top_gallery_url=https%3A%2F%2Fimg.kwcdn.com%2Fproduct%2FFancyalgo%2FVirtualModelMatting%2Ffb122f40434d42b9870f1c81445c1aa4.jpg&spec_gallery_id=25186241&refer_page_sn=10009&refer_source=0&freesia_scene=2&_oak_freesia_scene=2&search_key=rp2040&_x_sessn_id=ddb5whl7cr&refer_page_name=search_result&refer_page_id=10009_1684988061682_d35x5b6wwm](https://www.temu.com/sumolink-erhu-rp2040-pico-like-mcu-board-based-on-raspberry-pi-rp2040-chip-dual-core-arm-cortex-m0-processor-up-to-133-mhz-onboard-4mb-flash-usb-c-connector-g-601099517031753.html?top_gallery_url=https%3A%2F%2Fimg.kwcdn.com%2Fproduct%2FFancyalgo%2FVirtualModelMatting%2Ffb122f40434d42b9870f1c81445c1aa4.jpg&spec_gallery_id=25186241&refer_page_sn=10009&refer_source=0&freesia_scene=2&_oak_freesia_scene=2&search_key=rp2040&_x_sessn_id=ddb5whl7cr&refer_page_name=search_result&refer_page_id=10009_1684988061682_d35x5b6wwm)

To control WS2812 RGB strip and the power next step, I use an rp2040 mcu.

I used the rp2040 instead of the Raspberry Pi gpio because it was difficult for me to modify the volumio. And using an external mcu gives me more freedom and I can control more devices, such as the LCD brightness, RPi power on or power off.

Just because the price, I choose Sumolink Erhu RP2040, you can use any rp2040 mcu board as the same.

![10inch HiFi Player](./image/06.jpg ':size=400x')