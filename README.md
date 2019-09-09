# Introduction

This repo contains bits for the Ferret Cam, part of the ferret tunnel project described here:

http://www.meades.org/ferrets/ferrets.html#Update_August_2019

Please refer to that link for more information.

# Off The Shelf Components

The camera itself was an [szbvcam](http://www.szbvcam.com/) purchased from [Amazon](https://www.amazon.co.uk/gp/product/B077K2TH1V/).  It consists of a small plastic module that is  the processing unit (connecting via Wifi), a high resolution camera on the end of a flat 10 cm cable, a LiPo rechargeable battery and an antenna.  A USB connection to the procesing unit enables the battery to be charged.

To power the camera from a mains supply a mains-to-5 Volt switched-mode power supply module was purchased, also from [Amazon](https://www.amazon.co.uk/gp/product/B073GPSY4T).

Then to mount the lot a waterproof [plastic enclosure](https://uk.rs-online.com/web/p/general-purpose-enclosures/7739607/), 230 mm x 125 mm x 60 mm, was purchased from RSOnline, plus a [waterproof high voltage tee panel connector](https://uk.rs-online.com/web/p/lighting-connectors/1369903/) and matching [cable-mounted tee socket](https://uk.rs-online.com/web/p/lighting-connectors/1369898/).

A pack of [Vishay 3 mm high-brightness white LEDs](https://uk.rs-online.com/web/p/leds/8184452/) were also purchased from RSOnline.

# 3D Printed Parts

3D printed parts were created to mount the camera and illuminating LED safely (safe from ferrets that is) and ease the mounting of the components inside the enclosure.

All of the 3D printed parts were designed in Blender 100 times larger than real life, so something 1 centimetre long would be 1 metre long in this Blender file.  For 3D printing the parts should be exported to STL with a scale factor of 10 (since in Blender a scale factor of 1000 would normally result in STL actual size).

There were 6 parts:

* the two parts of the stalk that holds the webcam and LED,
* a large washer,
* a spacer to go underneath the PSU to avoid it fowling some fixings inside the enclosure,
* a mount for the webcam processing module,
* a partition to sit between the PSU, with its high voltage input. and the rest of the components.

The stalk should be printed at 0.1 mm resolution (with supports added in the slicer program) while the spacer, webcam processing module holder and partition should be printed at 0.2 mm resolution (no supports required).  I used black ASA for these parts since I had it lying around but PLA is perfectly acceptable.  The large washer was printed in flexible PLA at 0.2 mm resolution and a nice slow 15 mm/s print speed.

# Construction

A 12 mm hole was drilled in the centre of the floor of the plastic enclosure for the 3D printed stalk to enter and a matching 20 mm hole was drilled in the centre of the Osma screw-top hatch cover of the ferret tunnels.

A 270 ohm series resistor and solid-core leads were soldered to a high-brightness LED.  The leads were covered with heat-shrinkable sleeving so that the LED could be held neatly inside the 3D printed stalk.

The LED and the camera were threaded through the hole in the centre of the plastic enclosure, through the large 3D printed washer, between the two halves of the 3D printed stalk and into place.  The top of the 3D printed stalk was then wiggled-up through the hole and the bottom of the stalk was pushed down through the hole in the centre of the Osma screw-top hatch cover.  Two narrow cable ties were used to hold the two halves of the 3D printed stalk together, one positioned at the bottom between the LED and the camera, another positioned inside the enclosure right at the top of the stalk; the stalk is only held loosely to the enclosure, the large 3D printed washer will do most of the work.

Inside the enclosure the 3D printed spacer beneath the PSU, the 3D printed webcam processing module holder and the 3D printed partition were all glued into place with Araldite.  Holes were drilled in the enclosure for the tee panel power connector and the Wifi antenna.

Velcro sticky patches were used to keep the PSU in place on its spacer and the LiPo battery in place in the lid of the enclosure.  An old micro-USB cable was chopped-up to connect the USB socket on the webcam processing module to the 5 Volt terminals of the PSU.  Some mains cable from an old pond pump was re-purposed to connect the lot, via the cable-mounted tee socket, to a 3 Amp fused plug and hence a mains supply.

# Viewing

The camera offers an MJPEG stream at URL http://IP_ADDRESS/video/livesp.asp# but this only updates a few times a second.  Much better is an ASF stream which contains both an H264 video stream and mono 8 kHz ADPCM audio at URL http://IP_ADDRESS/videostream.asf?user=admin&pwd=&resolution=32.  However there doesn't seem to be an ASF plug-in for web browsers, you have to view the stream with something like [VLC Player](https://www.videolan.org/vlc/index.html).

To allow devices outside your home LAN  to see the video feed, convert your broadband provider's dynamic IP address into a static one using a free service from the likes of [www.no-ip.com](www.no-ip.com), quote that address on your web page, then use Port Forwarding to get your wireless router to forward incoming HTTP requests to the camera.