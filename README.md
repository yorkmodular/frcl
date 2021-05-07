## FRCL - Fixed RC filter (low-pass)

Think of it as a buffered mult with an RC filter on each output, because that's basically what it is.


The outputs consist of a set of 1-pole RC filters - these roll off at 3dB/decade. You're not going to be getting shrieky resonance out of these, but they are good for 'tidying up' some sounds (lower frequencies are good at reducing the effects of high-frequency transients, aka 'pop'). Modules are cascadeable should you wish to increase the filtering effect.


The following are implemented, with their associated resistor/capacitor pairs in brackets should you feel the need to tinker.

* 63Hz (R3/C1)
* 250Hz (R4/C2)
* 500Hz (R5/C3)
* 1.5kHz (R6/C4)
* 3kHz (R7/C5)
* 5kHz (R8/C6)
* 8kHz (R9/C7)

The _exact_ cutoff frequency will depend on the accuracy of your components - pre-built modules will use E24 series resistors, although the BOM lists alternative values should you wish to do a DIY build using E96-series components instead. It's worth noting that the tolerances of capacitors are generally somewhat worse than those of resistors.

If you're DIYing, I recommend the use of polythene film capacitors on the filters - you can use ceramic capacitors in extremeis. Similarly, if you want high-pass filters instead just swap the appropriate resistors and capacitors (a high-pass version of the module is planned, though)

If you want to use completely different values, feel free - the filter calculator at [http://sim.okawa-denshi.jp/en/CRtool.php](http://sim.okawa-denshi.jp/en/CRtool.php) is a useful resource.

### Build notes

See above regarding the use of film capacitors and substitution of more precise resistor values. All components are through-hole. There's no reason you couldn't implement different filter cutoffs, but bear in mind that the markings on the faceplate won't correspond with reality.

Op-amp choice doesn't really matter - TL074/084 will work just fine.

Input and output jacks are PJ302-M or equivalent, and the power connector is on the top edge of the board.