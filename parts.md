
Note: I am very much an amateur in this area, and I don't really know what I'm doing.
These pages are mainly a place for me to organize plans and links in my tinkering and
building a modular synth which I'm only just getting started with.  Don't count on any
of the information found here to actually be correct.

Note about yusynth circuits: http://electro-music.com/forum/topic-39693.html

Yusynth:

	"Some can be used directly in 12V :
	VCA, mixer, ADSR, most of the VCF, Gate delay, pulse delay, glide, Nois&SH, saw animator, logical, random gates, FFB, VC-LFO

	Some can't and need important modifications :
	VCO, CV-STANDARD"

	Additionally the minimoog filter needs different resistor values as noted.


This site has some good tips: https://dintree.com


Power supplies
--------------


Frequency Central power supply

* http://www.frequencycentral.co.uk/wp-content/uploads/2018/03/FC-Power-Build-Doc.pdf

(What the fuck do I have to do to make markdown recognize a fucking list?)

* 1x PCB https://www.ebay.co.uk/itm/253819427984
* 3x 1K 1/4 W resistor: https://www.taydaelectronics.com/resistors/1-4w-metal-film-resistors/10-x-resistor-1k-ohm-1-4w-1-metal-film-pkg-of-10.html
* 2x 100nf capacitor: https://www.taydaelectronics.com/0-1uf-100v-5-polyester-film-box-type-capacitor.html
* 3x 100uf capacitor 35V :  https://www.taydaelectronics.com/100uf-35v-105c-radial-electrolytic-capacitor-6x11mm.html
* 6x 4700uf capacitor 25V: https://www.taydaelectronics.com/4700uf-25v-105c-radial-electrolytic-capacitor-16x26mm.html
* 1x 7812 +12V 1.5A voltage regulator: https://www.taydaelectronics.com/l7812cv-lm7812-l7812-voltage-regulator-ic-12v-1-5a.html
* 1x 7912 -12V 1.5A voltage regulator: https://www.taydaelectronics.com/l7912cv-lm7912-l7912-7912-voltage-regulator-ic-12v-1-5a.html
* 1x 7805 +5V 100ma voltage regulator: https://www.taydaelectronics.com/l78l05acz-l78l05-78l05-5-volts-100ma-voltage-regulator-ic.html
* 6x 1N4004 1A 400V diode: https://www.taydaelectronics.com/1n4004-diode-1a-400v.html
* 3x 3mm red LED: https://www.taydaelectronics.com/led-3mm-red.html
* 2x heatsink: https://www.taydaelectronics.com/heatsink-to-220-4-fins-aluminium.html
* 1x 2x40 2.54mm double row pin header strip: https://www.taydaelectronics.com/connectors-sockets/pin-headers/2x40-pin-2-54-mm-double-row-pin-header-strip.html
* 2x M3 bolt (to connect heatsinks to voltage regulators)

1x 3A 12V AC/AC wall wart power supply (hard to find 3A).

* https://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=10428&pa=10428PS
* https://www.allelectronics.com/category/815/wall-transformers/1.html

* Triad magnetics:
  * https://www.digikey.com/product-detail/en/triad-magnetics/WAU12-2500/237-1882-ND/4915296&?gclid=EAIaIQobChMIwvizsLzF3wIVF1qGCh1XaQmaEAQYASABEgJs0fD_BwE



VCO
---

https://www.lookmumnocomputer.com/cem-3340-diy-simple/

* 1x strip board 46x24
* 1x 10k trim pot
* 1x 100k pot
* 1x 8 leg IC socket
* 1x 16 leg IC socket
* 2x 470R resistor
* 1x 620R resistor
* 1x 1K8 resistor
* 1x 5K6 resistor
* 1x 24K resistor
* 2x 100K resistor
* 1x 1M5 resistor
* 1x 1nf ceramic capacitor
* 1x 10nf ceramic capacitor
* 1x CEM3340 or AS3340
* * 1x TLO72 opamp
* 3x 1/4 inch jack sockets

There is also a PCB + surface mount components version of this LMNC VCO described here,
with an associated github repo with kicad files:

* https://hackaday.io/project/161548-modular-synthesizer/log/153776-vco-module-first-pass
* https://github.com/xxv/modular-vco


Another, more complicated VCO:
http://skullandcircuits.com/the-oscillator-one/


VCA
---

* http://familjenronnberg.se/~niklas/diy/eurorack/vca/
* http://dintree.com/#D100


Envelope Generator
------------------

* AR: https://www.youtube.com/watch?v=JsRMtJcfESI
    * http://familjenronnberg.se/~niklas/diy/eurorack/ar/

* ADSR: http://familjenronnberg.se/~niklas/diy/eurorack/adsr/

* Another ADSR: http://www.yusynth.net/Modular/EN/ADSR/index_latest.html  (Note: yusynth is +15/-15V, not eurorack)

* http://dintree.com/#D101

VCF
---

* Some here: http://www.yusynth.net/Modular/index_en.html (needs different resistor values for eurorack)

MIDI to CV/Gate
---------------

Probably need to do this as a kit, as the voltage needs to be very precise.

here is a usb powered one: https://janostman.wordpress.com/cheap-diy-usb-midi-to-cv-interface/

here is a teensy based one: https://hackaday.com/2017/09/30/midi-to-cvgate-the-easy-way/


LFO
---

https://noisehackerspace.com/build-lfo-eurorack-relaxation-oscillator/

Seems to be a very slow oscillator (20s to 2 min) so RC values will need
adjusting to get this into a more "normal" LFO range.

Here's another LFO (This is not voltage controllable though):
* http://www.davidhaillant.com/wp/wp-content/uploads/LFO-1.1-BOM-doc-20161215.pdf
* https://www.youtube.com/watch?v=k3BoGHwYfZY

VCLFO
-----
* https://www.youtube.com/watch?v=i-YMkeIz8ak
* http://synthdiy.com/files/2008/lfo5a.pdf

Another one:
* http://www.yusynth.net/Modular/EN/LFO/VC-LFO1.html  (not eurorack power though)


level converter (line level to/from modular level)
--------------------------------------------------

Useful for getting audio out of the modular, or getting, e.g. guitar (with DI box) into the modular.

https://www.reddit.com/r/synthdiy/comments/aa338w/updown_a_simple_module_for_shifting_signal_levels/

* 2x LM741 opamp (is 741 good choice here? Why not eg. TL07xx for lower noise, better frequency response?)
* 4x 4K7R resistor
* 2x 470R resistor
* 2x 1K resistor

Passive Multiple
----------------
* http://familjenronnberg.se/~niklas/diy/eurorack/passive_multiple/


Buffered Multiple
-----------------
* http://familjenronnberg.se/~niklas/diy/eurorack/multiples/


Mixer
-----
* http://familjenronnberg.se/~niklas/diy/eurorack/muxiple/
* http://dintree.com/#D102


Reverb:
-------
* http://dintree.com/#D103


Voltage source:
---------------
* http://dintree.com/#D104

CV mixer
--------
* http://dintree.com/#D105

Slew (for e.g. portamento)
--------------------------
* http://dintree.com/#D107


Kosmo to/from Eurorack
----------------------

Just get a bunch of 3.5mm and 1/4 inch jacks and wire
them together to facilitate patching back and forth between
eurorack and Kosmo

BASS DRUM
---------

* http://electro-music.com/wiki/pmwiki.php?n=Schematics.HipBassDrumByCraigAnderton

Should work ok with 12V power supply according to this: http://electro-music.com/forum/topic-28447.html

Here is a strip board layout: http://electro-music.com/forum/phpbb-files/hip_bass_drum_01_strip_178.gif from here: http://electro-music.com/forum/topic-28447.html

Stripboard layout may contain mistakes. Some people had trouble with it, and
there are these comments: "Be careful if you make the stripboard version,
2N3904 are upside down. They need to be inverted, Emitter goes to GND. Pot
wiring is inverted too.  Cheers it sounds really awesome for a little circuit."

SUB OSCILLATOR
--------------

* https://www.youtube.com/watch?v=Wc1HdbsepTg
* https://electricdruid.net/a-study-of-sub-oscillators/

