# PaIA Computer Drums Kit for VCF Southwest
Welcome to the Computer Drums kit for VCFSW 2026

PaIA had an easy to build kit back in 1978 using LM3900 Quad Norton Comparators to make analog drum sounds. I ran across this kit perusing some old archives and reached out to PaIA to see if I could reissue the kit. Permission was granted by the late Scott Lee, but I was told there were no films left for producing more PCBs. They sent me a newer version of the documentation and I laid out a replacement PCB in KiCAD then ordered beta PCBs from JLCPCB.

I successfully interfaced this to the 20 pin expansion interface on the [VCF 8031 Show Computer](https://github.com/channelmaniac/VCF_8031/) built for a previous VCF Southwest show and included the information in the build guide I created for this kit.

The kit output will require external amplification.

Things I noticed during the build:

*	No mention of the requirement to use +15v outside of one small blurb in how the noise source was designed. No mention on the external connections to the PCB either.

*	The snare started with a popping noise before the hiss.

Things I learned:

* The kit required a noisy transistor to generate the static for the snare sound, provided the transistor, but didn't mention anything on how to choose one for folks who wanted to roll their own build.

* Not all transistors make noise, let alone a LOT of noise, and age doesn't matter as some of the older ones I had generated no noise at all.

*	Lifting a resistor and feeding the +15v into it for the noise source transistor produced a clean snare sound with no popping noise. I successfully lowered it to 12.0v and the snare sound was still clean with the transistor being used in that beta kit. 

*	The 1/8" audio output jack must be mounted so the body is at the edge of the PCB for cables to fit. Trimmed the cable on the beta test to make it fit.

* KiCAD doesn't like it when you change pins on a chip so you can do the layout like the original was in print.

* Bourns has different pin spacings on their trimpots on the same series parts but with a dfferent letter at the end. Next time I will skip those and go straight to cheap Chinese sourced 6mm pots. I have plent of 50K pots with small pin spacings to use in a future project. If you ever use Bournes pots, put both pin spacings on the PCB for each pot. It will save you headaches trying to find enough parts across multiple sources.

Things I did: 

*	I put some individual machine pin sockets on the PCB where the noise source transistor went and set about digging through every transistor in the shop, including all the old ones from a huge estate sale component haul, to find the ones that generated the most noise in circuit. I barely found enough after searching through about 1200 transistors to fulfil the 5 beta kits and the 100 production ones.

* Added a place on the PCB for the +15v power source.

* The production PCB was set up with a physical jumper to switch between the 9v source for testing and the 15v source for cleaner sound. I used a physical jumper instead of a solder jumper like used on the input logic level signalling to avoid possible solder shorts between the +9 and +15v sources.

* Adjusted the placement of the 1/8" jack on the production board to allow for a cable to be easily connected.

I offered the gerbers for this project to PaIA, but they have not expressed interest in them. My project gerbers will NOT be posted as this is still the IP of PaIA. Scott's son has taken over and continues to run the company after his father's passing.
