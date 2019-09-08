# Introduction

This repo contains bits for the Ferret Cam, part of the ferret tunnel project described here:

http://www.meades.org/ferrets/ferrets.html#Update_August_2019

Please refer to that link for more information.

# Off The Shelf Components

The camera itself was an (szbvcam)[http://www.szbvcam.com/] purchased from (Amazon)[https://www.amazon.co.uk/gp/product/B077K2TH1V/].  It consists of a small plastic box containing the processing unit (which connects via Wifi), a high resolution camera on the end of a 10 cm flexi, a LiPo rechargeable battery and an antenna.  A USB connection to the box enables the battery to be charged.

To power the camera from a mains supply a mains-to-5V switched-mode power supply module was purchased, also from (Amazon)[https://www.amazon.co.uk/gp/product/B073GPSY4T].

Then to mount the lot a waterproof (plastic enclosure)[https://uk.rs-online.com/web/p/general-purpose-enclosures/7739607/], 230 mm x 125 mm x 60 mm, was purchased from RSOnline, plus a (waterproof high voltage tee panel connector)[https://uk.rs-online.com/web/p/lighting-connectors/1369903/] and matching (cable-mounted tee socket)[https://uk.rs-online.com/web/p/lighting-connectors/1369898/].

A pack of (Vishay 3 mm high-brightness white LEDs)[https://uk.rs-online.com/web/p/leds/8184452/] were also purchased from RSOnline.

# 3D Printed Parts

All of the 3D printed parts were designed in Blender 100 times larger than real life, so something 1 centimetre long will be 1 metre long in this Blender file.  For 3D printing the parts should be exported to STL with a scale factor of 10 (since in Blender a scale factor of 1000 would normally result in STL actual size).

There were 6 parts:

* the two parts of the stalk that holds the webcam and LED,
* a large washer,
* a spacer to go underneath the PSU to avoid it fowling some fixings inside the enclosure,
* a piece to hold the webcam processing module,
* a partition to go between the PSU and the rest of the components.

The stalk should be printed at 0.1 mm resolution (with supports added in the slicer program) while the spacer/module holder and partition should be printed at 0.2 mm resolution (no supports required).  I used black ASA for these parts since I had it lying around but PLA is perfectly acceptable.  The large washer was printed in flexible PLA at 0.2 mm resolution and a nice slow 15 mm/s print speed.

# Construction

A 12 mm hole was drilled in the centre of the floor of the plastic enclosure for the stalk to enter.

A 270 ohm series resistor and solid-core leads were soldered to a high-brightness LED.  The leads were covered with heat-shrinkable sleeving so that the LED could be held inside the 3D-printed stalk without shorting.

The large 3D printed washer was pushed over the top of the two halves of the 3D printed stalk then the LED and the camera were threaded through the hole in the enclosure and between the two halves of the stalk and into place.  A narrow cable tie was used to hold the two halves of the 3D printed stalk together, situated between the LED and the camera.

Inside the enclosure the spacer beneath the PSU, the webcame module holder and the partition between the PSU and the rest of the components were all glued into place with Araldite.  Holes were drilled in the enclosure for the tee panel connector and the Wifi antenna.

Velcro sticky patches were used to keep the PSU in place on its spacer and the LiPo battery in place in the lid of the enclosure.

To fit the lot into the ferret tunnels a 20 mm hole was drilled in the centre of the Osma screw-top hatch cover.