---
title: 'Snom PA1 als extra bel'
published: true
date: '24-07-2020 22:51'
---

De PA1 van Snom is een systeem waarmee VoIP techniek aan een (bestaand) analoog omroepsystemen gekoppeld kan worden. Dit is handig om ouderwetse analoge techniek toch te kunnen blijven gebruiken.

In bepaalde gevallen is het nodig om een extra bel aan te sluiten. De PA1 is hier eigenlijk niet voor gemaakt maar leent zich er toch goed voor.

Volgens de FAQ kan een Snom PA1 gebruikt worden in combinatie met een luidspreker:  
[FAQ/Can my snom PA1 be used as a loudspeaker ringer?](http://wiki.snom.com/FAQ/Can_my_snom_PA1_be_used_as_a_loudspeaker_ringer%3F)

    Answer
    In some VoIP environments, such as snom One, we have been able to create one identity in the snom PA1 to work as a 'Paging' extension and configure a second identity to play a 'ringer' over the loudspeaker.

    Set the snom PA1 to the following configuration using the Web User Interface:

    Under Preferences:

    Set 'Use Headset Device:' to <RJ Connector>
    Set 'Ringer Device for Headset:' to <Use Headset>

    Under the 'non-paging' Identity:

    Under the SIP 'tab', turn off 'Auto-Answer'

    The snom PA1 is not designed for this purpose, so it is recommended that the Identity not be shared with other endpoints. The 'loudspeaker ringer' identity should be set into a group to represent the extension(s) that require the 'loudspeaker ringer'.

Wat mij opviel is dat de eerste optie niet (meer) beschikbaar is in de laatste firmware. Op het moment van schrijven gaat het om firmwareversie 8.7.5.75.  

Dit betekent dat de bovenstaande oplossing niet meer werkt. Gelukkig blijkt de nieuwe oplossing niet ingewikkeld. Via het supportsysteem van Snom had ik binnen 10 minuten een reactie en werd uitgelegd dat ik onder "Identities" - "SIP Settings" de optie "Auto Answer" uit moest schakelen.

Onderaan de documentatie van deze instelling staat de standaardwaarde. Deze waard is "uit" voor alle toestellen maar "aan" voor de PA1.

* Helpdesk ticket: https://helpdesk.snom.com/support/tickets/38726
* USER_AUTO_CONNECT: https://service.snom.com/display/wiki/user_auto_connect
