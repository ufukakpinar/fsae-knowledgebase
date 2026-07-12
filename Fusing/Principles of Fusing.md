## Fusing 
Fusing is integral to the safety considerations of any electrical system. In this document we will discuss the main aspects of fusing.

A fuse regardless of its design or construction aims to fulfill a simple purpose: If the current flowing into the circuit exceeds the rated current of the fuse it will interrupt the flow of current therefore protecting the wires or circuitry.

The 3 most important elements of fuse design are as follows:
  1. Current Rating/Blow Time
  2. Voltage Rating
  3. Iterrupt Rating

## Current Rating

The current rating of a fuse is the maximum current it can pass continously without blowing. While this rating is often a single number it is crucial to understand that the blow time of the fuse and its fusing curve directly determine its effectiveness in protecting the wires and componenents you want to protect. A fast acting 20A fuse might trip faster than a slow acting 15A fuse and that can mean the difference between a burnt wire/trace or the fuse fulfilling its duty.

The curve pictured below belongs to a fast acting high current fuse for solar/EV applications. You will notice the different curves for each variant of the fuse. Another notable observation is that the fuse has a nonlinear behaviour. Because the ohmic heating of the material is related to the square of the current flowing over it, fuse graphs are usually represented in a log-log graph. This means that the fusing behaviour is close to straight lines when represented on the log-log chart. The consequence of this is that while 20A fuse might not trip at its rated current for many hours, a marginally higher current can trip it in seconds or miliseconds which is what makes fuses very effective. 

<img src="https://github.com/ufukakpinar/fsae-knowledgebase/blob/58bcefd0b1c954a84807009d47db8d0bc5d684a6/Fusing/assets/L70S100%20Time%20Curve.png">

Another thing that can be observed is that the fusing behaviour is slightly different for low overcurrent vs very large overcurrent for this fuse. This can be attributed to the impact of cooling effects as with low overcurrent faults the fusing element will dissipate heat which will increase the blow time, while very high overcurrents blow the fuse in a very short time therefore making the effects of thermal loss negligible.

## Voltage Rating

Another important safety aspect of our fuse is its ability to prevent arcing over the blown fuse path therefore ensuring that the circuit will not be unintentionally reenergized. Especially for high voltage DC or AC systems the voltage rating of the fuse is critical to ensure the fuse behaves appropriately in its appliciation. The gap created by the molten or vaporized metal when the fuse is tripped must be wide enough so that the circuit voltage cannot arc over that gap.

## Interrupt Rating

Interrupt rating determines the maximum fault current the fuse is designed to handle without failing catasthropihicaly. This puts a practical limit to how much fault current can be safely contained by the fuse. If this rating is exceeded the fuse might phyically break apart or the effects of the violent melting might cause a conducting or arcing path to form after the fuse trips.

## eFuses

With recent developments in power electronics it is becoming much more popular to use eFuses which are in simple words integrated packages comprised of power MOSFETs and precise current sensors which can detect the current flowing over the MOSFETs and switch the current path off when the boundary conditions are exceeded. These types of fuses come with the obvious advantage of being reusable as they usually have a way of resetting the internal control system to allow current to flow again when the fault condition is resolved.

for more information you can refer to documentation created by LittelFuse: https://www.littelfuse.com/assetdocs/fuse-fundamentals-at-the-heart-of-electrical-systems-fuses-keep-operations-live?assetguid=55d2e833-b53b-467f-a0c2-f15ff2316db3
