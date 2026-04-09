  Made by: @srikardesu08 // srikardesu
  
  Repository link: https://github.com/bujjikai/Threefold-Repetition
  
  Total hours so far: 68

- [✔] I have a 3D printer or will be getting one before March 21st

# March 16 - April 4th

## Research Weeks 

### Approximate Hours: 65

Backstory:
I originally started the plan for this printer as a tool changing 3d printer with 2 tools as a way to enable cleaner model printing, as it would allow me to use alternate material for my supports. 

I even fleshed out a mostly complete BOM: https://docs.google.com/spreadsheets/d/1RauQnE8QFAjwqxIpCGbVFvZMdfIE6Xy7mC4uiU9PczM/edit?usp=sharing

But the price quickly started spiraling out of control, so even though I spent many hours on the design, I decided to cut my losses and switch to a completely different type of printer.

---

Inspired by the Voron v0 and the Trident printer, I decided to make a belt driven 3 point bed trammed 3d printer with a kinematic mount. This will allow for fully automated bed leveling and also give me the ability to program a dance sequence into the printer. I've done lots of research for this printer, and I will try to write most of it down here, but I am definitely going to forget about some key points, so I will be writing them down as I continue modeling the printer. This is a list of my current criteria and notes regarding them:

  I will be using 1515 and 2020 extrusions for my frame to maximize rigidity and minimize weight, and they will be connected using blind joints.
  I am using NEMA 17 stepper motors with low inductance to allow for fast accelerations that aren't limited by hardware.
  The bed will be mounted using a Maxwell Coupling to allow for a true kinematic motion system that (hopefully) won't cause any bending of motion components.
  Currently deciding between the Cartographer v3 and the zero-click bed leveling systems for my printer, as the cartographer is faster but may reduce my build space,
while the zero-click will make the calibration time much faster, since I want this to be a high-speed prototyping beast, I want to shave off as much start-up
time as well.
  MGN7 and MGN9 rails will be used for the motion system of the printer
  MJF Nylon or ABS/ASA will be used for all the structural parts of the printer
  A Sherpa mini will be paired with an NF Crazy hotend for high flow rates
  
Current BOM (It's a mess right now): https://docs.google.com/spreadsheets/d/1a8FgY6IiLnPJ6jmapHXnImGWi2A3qWeGx6_EeYZa9Co/edit?usp=sharing
  
Many, many, MANY hours were spent on sourcing the materials and calculating the tradeoff for buying cheaper parts, as I wanted to ensure I had the funding to build this printer before I spent lots of time designing. I spent lots of time on AliExpress and various 3d printing Discord servers talking to people to try to get good deals, and am currently aiming for a $400 final BOM.

I also spent lots of time reseaching mechanical stress, frame rigidity, motion system math and other the various other math that needs to be used, to build
a printer that can with stand high speeds.

Sources (Out of Order):
- Voron v0.2: https://github.com/voronDesign/Voron-0
- Tri-Zero: https://github.com/zruncho3d/tri-zero
- Hex-Zero: https://github.com/Alexander-T-Moss/Hex-Zero
- Trident: https://github.com/VoronDesign/Voron-Trident
- https://youtu.be/XERsgO5s7yI?si=-qPo9oev1F68Lrqf
- https://youtu.be/VEgwnhLHy3g?si=oO_b3xo6edVW-4YU
- https://youtu.be/ekUkI9iWUoM?si=jPAYymUBffeof3i1
- https://youtu.be/YQjE3ZRaNZ8?si=1Ow-52wCpzvYN2nW
- https://youtu.be/a9irK9rOUHY?si=-80xJulU_e7nC1yn
- https://youtu.be/gzBhTrHv0-c?si=S36YozkhWN4a3Lvr
- https://youtu.be/6tnqWVSE2tQ?si=isGhxAyJp6IRU2Si
- https://youtu.be/2dvbn0rWA60?si=hl5diNP-XYNxCVC_
- https://youtu.be/tV44UJmqM6Q?si=bQ4B1tJSWEa4PZTT
- https://youtu.be/QIbzbwEY7nU?si=NpLjWYR0JRqVnl7p
- https://youtu.be/89ZJjmjzL30?si=XIPvbClM01KEU63V
- https://youtu.be/jC5yuF9fMp8?si=qCWFCZ34UojYlLcT
- https://youtu.be/YijwkQCOBEA?si=DGMcbZO8D6kIBwIE
- https://youtu.be/1pMJQetyA4A?si=m8Bre4n7yc_jctYA
- https://youtu.be/_ramiM3KHYE?si=lIFp7r89vbLXX2E2
- https://voron.dozuki.com/Guide/Mechanics/68
- https://clevercreations.org/clean-repair-linear-guide-rails/

# April 5th

## Frame

### Approximate Hours: 3

I began assembling the main frame, heavily inspired by the Voron v0 and Hex Zero designs. The primary structure is now mated using blind joints for a clean finish.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/4cf6c871-7468-4d2a-932f-cc4dd007ab5d" />

I have also installed the frame rails and the electronics mounting rail; the final rail (not visible) will be integrated during the gantry assembly.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/8f68424e-f2c4-4212-9b24-f3387a957415" />

# April 6th

## Z Axis

### Approximate Hours: 3

I spent time figuring out where exactly to place the bed and the motors, as they need to be placed an off set very precisely in order to ensure the whole build plate can be reached by the tool head. I placed the motors a little offset from the frame above it so that it can be bolted into the frame above. I also learned how to use the width and parallel mates, which gave me much more flexibility instead of always using fastened mates like I always used to do earlier. 

<img width="500" alt="image" src="https://github.com/user-attachments/assets/13129201-b89b-4137-b29d-8cb8242dbf4f" />

The current plan is to use a belt system (instead of a lead screw) to move the bed up and down as it is a much cheaper alternative, but this has a downside
of resulting in the bed dropping when the printer is turned off (as the motors rest torque is rlly low). To combat this there are 3 options I am considering:
- Gear reduction to increase torque
- Add some sort of spring to pull the rail upward with enough force
- just add rubber bumpers for the bed to hit

I'm just not going to do anything for now but will look into this for the future. Also I'm realizing that I need a higher wattage psu that I planned for, due to a higher printer speed -> more current draw from the power source. I might go with a 200W psu instead of a 150W one, now I just need to figure out how to cram it into the space I have...

Current needs to reduce print time
- reduce start up time (~~AC Bed?~~) ------- NOTE: AC bed is a horrible idea due to the probability of a 120V shock, **NOT WORTH IT** for this build
- fast bed scanning
- fast printer (top speed and accelerations)
- high volumetric flowrate on hotend
- high melt rate filament

# April 8th

## Motion

### Approximate Hours: 










   
  
