# E-bike with 12V-6Ahr-Lithium-Ion-Capacitor
How to design an e-bike battery using 45 3.2V 800F LICAP batteries with 1.6Whr each

the lightest [e-scooter](https://en.wikipedia.org/wiki/Razor_(scooter)) batteries are around 6Ah. Lithium ion capacitor density is 6x less that of lithium polymer. (these are ok for flat roads, not bumpy ones with lots of rough terrain and potholes). They are not really powerful enough for a seated e-bike. I may update this repository with an analysis on a more powerful e-bike battery, such as a 24V or 36V scooter.

This 800F one is 1.6Whr:
![image](https://github.com/user-attachments/assets/f1393e3e-2825-4c4a-b9bb-9745075b1a58)

https://www.richardsonrfpd.com/ep-insights/3-8-v-800-f-lithium-ion-capacitor-cell-from-licap-technologies/

Cornell-Dubilier has a [220F](https://www.digikey.com/en/products/detail/cornell-dubilier-knowles/VMF227M3R8/13665371) which is around 250mWh, which seems less dense than the Licap one- 880F is only 1Whr, compared to 1.6Whr on the Licap for 800F. They are quite pricey, around $19.79 for one on Digikey and $15.83 for 50 ($791.76 @ 12.5Whr, which also means it could run a 12V motor at 1.04 Amps for 1 hour, or a 12V motor at 6amps  for... 10 minutes?)- thus, not a budget e-bike category yet. But an interesting one, which will be explained later in the fender section. 

Alternatively, one could purchase the even less dense Vinatech [250F](https://www.newark.com/vinatech/vel13353r8257g/lithium-ion-capacitor-250f-3-8v/dp/38AJ2231) LIC, which costs 

1+	$6.93
10+	$6.60
25+	$5.71
50+	$5.28

and are 90mAh each. 50 of them would provide 4.5Ah of power.  A $264 bike battery is not unheard of on luxury bikes, but this is not enough range for even an e-scooter without a seat. But it could be done. 67 250F batteries would be needed for 6Ahr, 12V. for 10 minutes.  

The LICAP website has a "Request pricing" so I am going to guess they cost more than $20 each :) :
https://www.licaptech.com/lithium-ion-capacitor-cells
https://www.licaptech.com/pdfs/datasheets/lithium-ion/LICAP_LIC_Summary.pdf

It's also unclear which one has a higher continuous Amp hour discharge rate- it could be the Cornell one, whereas the other one may be designed more like a super cap- for short bursts. https://4donline.ihs.com/images/VipMasterIC/IC/CDUB/CDUB-S-A0014419427/CDUB-S-A0014512062-1.pdf?hkey=6D3A4C79FDBF58556ACFDE234799DDF0

12V x 6Amps in one hour is is 72Whr.

So If I designed a parallel battery array of 45 x1.6Whr 800F LiCAP lithium ion capacitors, I would have 72Whrs. It seems like  200F LICAP can be plugged in to a 18650 slot without running wires. and 800F uses  Size 32650 Cell Size, a form factor I was not aware of (see pdf):
 32x65mm
https://lynxbattery.com/products/stocked-in-usa-lynx-battery-32650-3-2v-6-5ah-lithium-iron-phosphate-lifepo4-rechargeable-cell not as large as I worried. But...

65mm times 45 (perhaps 9x5) is 160mm x 585 mm or 23 inch battery x 6.2 inches (could be more square like too) 

Here are 45 (pictured for array purposes- these are LiFEPO4, but LICS would look the same using 32650 format): 
![image](https://github.com/user-attachments/assets/b301c28c-4596-4c94-81b2-2bd12fdb3603)


If I were using the Cornell Dubilier , I would need four 220F (250mWh x 4)x 72, or _288_ Cornell-Dubilier lithium ion capacitors to get a 6Ahr 12V battery. That would be way huger than those batteries. Seems like my calculation is a bit off. Or maybe not.
250 CD batteries would cost $3958.80 for a 62.5Whr battery. With better efficiency on a [Gallium Nitride](https://www.eenewseurope.com/en/iqe-interview-the-geopolitics-of-gan/) power converter, 62.5Whr might actually be ok- in that it can have the same range as a larger battery that is typically required- or a power conversion loss that is typically associated with a higher watt hour battery (one of the two- I am new to this :).

 6Ahr batteries are used for e-bikes with less than 250W motors. but some of those are 36V and 48V. Anyways, 

I suppose it could fit under a bike but it might be a bit large, or some other arrangement perhaps doubling them up- that doesn't look like two feet to me- I might have counted them length wise in a line rather than standing up. 

Someone on Linkedin last week designed a 12V 100A Gallium Nitride power converter

![image](https://github.com/user-attachments/assets/449b145c-1145-4ff0-bcd8-117a97d09d21)
1.4kW/cubic inch.

https://www.semiconductor-today.com/news_items/2024/mar/epc-010324.shtml

https://en.wikipedia.org/wiki/Efficient_Power_Conversion
 www.epc-co.com

With A GaN transistor it might use less power, and thus result in greater range, plus the battery would last longer with more cycles.  

A company in India developed the first GaN charger for ebikes: 
https://wise-integration.com/wise-integration-and-savoy-group-introduce-worlds-first-embedded-gan-charger-with-e-bike-battery/

https://epc-co.com/epc/about-epc/events-and-news/news/artmid/1627/articleid/3148/shrink-motor-drives-for-ebikes-robots-and-drones-with-100-v-gallium-nitride-gan-fets-from-epc

Solar Fender
--
LICS would be lighter than LiPo (one of the benefits of having a less dense battery), but larger in overall size. That said, 9x5 32650 Cells could fit under a bike seat. And you could install a solar panel as a fender. The LICAP is rated for 100,000 charges. So with a highly efficient solar panel (whether it's [Perovskite](https://www.yahoo.com/tech/supercomputer-simulations-groundbreaking-discovery-potential-090000854.html) or a monocrystalline, you could theoretically recharge your battery several times while you bike or use a golf cart with a canopy.

![image](https://github.com/user-attachments/assets/04e1f8a5-9a75-4f00-abc5-d32cb0837d7f)

LICAP also makes 2200F LICs, but I made these calculations before I read that, and I will will assume they cost way more, have less ubiquitous support than with 32650 formats, and while might need fewer than 30 batteries, might be a bit less easy to transport (maybe even safety issues) 

![image](https://github.com/user-attachments/assets/778069b7-8dbf-4bfd-94c2-cd71b9753a03)
 
These are 4.4Whr batteries, which means installing _fifty_ of them would provide 220Watts of power for 1 hour. That is the minimum to propel an e-bike with a seat. The battery bank would also be around 2.75x larger, which may or may not fit under your bike... :)

Update: There are even 3000F LICS: https://www.licaptech.com/pdfs/datasheets/lithium-ion/LC3000-380-ASW.pdf which provides 6Whrs.. 

https://www.licaptech.com/pdfs/datasheets/lithium-ion/LC0200-380-ASW_Datasheet.pdf compared to the 250F Vinatech, this 200F is 270mAh-400mAh, more than 3x as dense at 50F less...



