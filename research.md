# Research Document for mag60lp
My main inspiration for this project is my want for a nice portable keybard that I can take everywhere, that will hopefully last years to come.
## Required Wants
- 60% keyboard, at this point I have realized I don't use the F row keys or numpad, or arrow keys much (and these keys can be on a layer under if i need them.)
- Split keyboard
- Via support
- Low profile (maybe make a normal profile in the future, but current focus is on portability)
- Stores in a way that keys are not exposed
- Quiet (put in required b/c should be easy enough)
- PCB not hand wired, mainly for the experience of designing a pcb
- Probably going to go with soldered switches for longer term reliability
### Hopeful Wants
- Clear/Translucent Case (Either smokey black or smokey pruple, but clear is fine)
- Foam to be quieter but only if the case is opaque
- Caps-lock light (maybe num-lock and scroll-lock too)
    - Or even better an OLED screen (however, I'm hesitant to add potentially fragile components)
- The storage mechanism uses magnets to  lock in place
- physical switch that can change layers
### No longer want
- Ortholinear (decided against b/c I want something more familiar for my first, but I'll consider it in the future)
## What I need to do
I'm currently working on this and decided that I will move this to the [README.md](./README.md), so the tasks and status's here will no longer recieve updates.
| |Task | Status | Notes |
|-|-|-|-
|Designing| Layout | Researching | 60% Split
| | PCB | Researching | Split 
| | Plate | Researching | 
| | Case | Not started | seems simple enough except for the magnetic mechanism I want
| | Plate and PCB mounting mechanism | Not Started | Gasket seems really popular nowadays
| | Bill of parts | Not Started | screws, heat inserted standoffs, magnets, diodes, microcontrollers, trrs connectors, etc.
| Choose | Switches | Not Started | Low Profile Kailh Choc V2 Switches
| | Plate Material | Not Started | Want Quiet
| | Case Material | Not Started | Want Quiet and possible transparent
| | Case Foam | Not Started | Optional, but not if transparent case
| | Microcontroller | Researching | Between Pro Micro and Elite C
| | Other hardware (TRRS, CapsLock LED, possible OLED screen, diodes) | Not Started | Connect the two halves
| | Stabilizers | Not Started | ... do low profile have stabs?
| | Keycaps | Not Started | Is it possible to get stepped capslock? also want something uniform or blank so I don't have to look at qwerty and also so I only have a single height to think about while designing the case closing mechanism, better be some nice double shot if it has legends on it.
| | Button for reset switch for flashing firmware easier | Not Started | Just to make it easier if anyone actually builds this.
| | Cables | Not Started | Keep in mind cable length and maybe color match or something.
| Assemble | Lube switches | Not Started | ... can you lube low profile switches?
| | Diodes on PCB | Not Started | probably test too
| | put more soldering tasks here later
| | Heat inserted threads/standoffs for the case | Not Started
| Program | Basic Firmware | Not Started | lowkey scared
| | Via Compatability | Not Started | Desperately want
## Software to Accomplish this
- KiCad
    - Common for open source keyboard designing but not the most beginner friendly
    - support for kailh choc v2 switch footprint
- erogen
    - can be used alongside KiCad
    - generate layouts, and define layouts via YAML file

## Resources Used
### Joe Scotto has a video on designing the PCB in kicad
https://youtu.be/8WXpGTIbxlQ?si=De-9pDI-k79aXWpj
- in the video he has a compilation of libraries for kicad
    - https://github.com/joe-scotto/scottokeebs/tree/main/Extras/ScottoKicad
    - this is nice because it includes parts for keyboards so I don't have to create them myself (switches, oled, microcontrollers, trrsr etc) 
### KiCad defaults
My defaults for KiCad were missing so I ran the following
``` bash
git clone https://gitlab.com/kicad/libraries/kicad-symbols.git
git clone https://gitlab.com/kicad/libraries/kicad-footprints.git
git clone https://gitlab.com/kicad/libraries/kicad-packages3D.git
```
