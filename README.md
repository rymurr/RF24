# Arduino driver for nRF24L01 2.4GHz Wireless Transceiver

Design Goals: This library is designed to be...

* Maximally compliant with the intended operation of the chip
* Easy for beginners to use
* Consumed with a public interface that's similiar to other Arduino standard libraries
* Built against the standard SPI library. 

Please refer to:

* [Documentation Main Page](http://maniacbug.github.com/RF24)
* [RF24 Class Documentation](http://maniacbug.github.com/RF24/classRF24.html)
* [Source Code](https://github.com/maniacbug/RF24)
* [Downloads](https://github.com/maniacbug/RF24/archives/master)
* [Chip Datasheet](http://www.nordicsemi.com/files/Product/data_sheet/nRF24L01_Product_Specification_v2_0.pdf)

This chip uses the SPI bus, plus two chip control pins.  Remember that pin 10 must still remain an output, or
the SPI hardware will go into 'slave' mode.

added by rymurr:
My goal is to clean up the code and make it more useable. I also want to test it better and verify everything is working correctly. I am also planning on extending this to work with the raspberry pi and other boards (see https://github.com/stanleyseow/RF24/) but in a more sane/clean/extendable way. Hopefully I can get rid of code duplication and align the interfaces better. Good luck to me!

So far I have:
* added a cmake based build system
* build and check sizes of all examples
* annotated source code

What I want to do:
* start rewrite of code
* track size of examples to ensure not huge growth
* find a way to test better, avoiding regression tests
* make some tests and integrate them into build system
* extend to other platforms (notably rpi)
