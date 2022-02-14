# moddable
## Implementing Service Changed characteristic

iOS caches Bluetooth devices' data against the device address, so that many things may be out of date from connection to connection - if you are testing code and changing services and characteristics, this may result in problems.

For instance, I found annoying the name persistence even when modifying the GAP name, experimenting many different features in Moddable code.

There is a need to indicate to iOS that you are changing things, and you can do this by implementing the Service Changed characteristic.

As mentioned in the Apple Accessory Design Guidelines document: 

> **23.12.2 Generic Attribute Profile Service**
> 
> The accessory must implement the Service Changed characteristic only if the accessory has the ability to change its services during its lifetime.
> 
> The device may use the Service Changed characteristic to determine if it can rely on previously read (cached) information from the device. See the Bluetooth 4.0 specification, Volume 3, Part G, Section 7.1.
> 

It came out to be really easy in Moddable.

(https://developer.apple.com/forums/thread/120689)

(https://developer.apple.com/forums/thread/19381)
