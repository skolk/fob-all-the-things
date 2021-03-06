# Fob-All-The-Things
access management for maker spaces

Fob all the things (known as FATT) has the goal of of creating an open source package of hardware and software to allow maker spaces and community groups to install access points with minimal hardware and coding knowlege (nothing outside of a terminal command prompt)
***
# Directory
- [Status](#Status)
- [History](#History)
- [Resources](#Resources)
- [Branches](#Branches) 
- [Outline](#Outline)


# Status
There are several groups working on FATT forked projects, with their own hardware and software, feel free to contribute. 

## Where this project is now:
FATT is active in at least 4 maker spaces running slightly different frameworks and hardware.

## Where we want to go:
Beyond the bottle neck that most maker spaces get tripped up at.

# History
FATT was conceived when maker spaces realized they were continually re-inventing the wheel to sove the same problem; groups would consistently get to the same point; have the same frustrations, and either crash and burn or move on to a proprietary system.

at Nomcon 2019; Ace Monster Toys created a presentation to demonstrate their progress on with FATT and created a working group in slack, landing website page, and several git repos.

***
# Resources
- [Ace Monster Toys presentation at NomCon-2019](https://www.acemonstertoys.org/fatt-at-nomcon/)
- [slide presentation](https://docs.google.com/presentation/d/1t7AaRWNNl93JGzS-Eg19WnUrunBbh1UaYufZjOnOvw4/edit#slide=id.p)
- [A Fob All The Things Landing Page](https://foballthethings.org/ ) where you can order dev kits
- [The 2019 working version for the presentation](https://github.com/acemonstertoys/fatt-nomcon-2019)
- [Nom Com Dashboard](https://nomcon.foballthethings.org/)  
- [wiki organizing](https://www.makerhappen.org/fatt)
- [Join the Slack](https://fatt-slack-auth.herokuapp.com/)
## Branches 
- [AMT FATT] Ace Monster Toys FATT setup
- [DanDudes version](https://github.com/DanDude0/MakerAccessControl)
- [Milwaukee Maker Space](https://github.com/DanDude0/MilwaukeeMakerspacePiFobReader)
- [Maker Space Controll Access Project page](http://koljawindeler.github.io/macs/)[Github]
(https://github.com/KoljaWindeler/macs/tree/master/website) 
- [NOVA PASS system](https://drive.google.com/file/d/1nC3Tc5U4PZIDftUa86jNpgwb28R_OMqJ/view) 


***
# Outline
The FATT framework's design intent is to be a platform to allow different code bases, hardware, and oversight for communities to grant access and track user resources; this is determined by establishing core use cases; divergent points, and convergence points.

## Hardware:
At the core of FATT is the key fob, a RFID tag that communicates with a Raspberry Pi 3B. How everything else happens is to support the space ensuring that the system is reliable and secure.

Because Raspbarry Pi's communicate on 3.3v logic, and the majority of industrial system are based on 12V or higher a logic stepper is necessay to engage with both electro mechanica system, the RFID communication, and Relays invovled. 

## Software
The local Raspberry pi's job is to interface with the RFID, check if the resource has permissions and then recored the request. The Acess point must store it's database either locally or remotly; and check the database. CUrrently the systme is set up to ping the data base every 100ms to ensure up to date resources.

## Backend
The user database and permissions can either be accessed via ssh on or held remortly in a systme such as AWS, Microsoft Azure, or some thing else. The Goal of this project is to be a good pipe. How that data based system is updated (apercot?)

## Admin interface
- [Apercot](https://www.wildapricot.com/) is a potential membership resource. 
- [ wooo ](https://woocommerce.com/)  for ATM door access

# Existing BOM for DEV Kit BOM's:
- [MMS Kit](https://docs.google.com/spreadsheets/d/1saBPHnn_E8FyzVhVKWeM24Enc3zIGl8CUS3w7r8rCs0/edit#gid=0)
- [FATT Dev Kit](https://docs.google.com/spreadsheets/d/19eD3aGPXen2XFFg_nxeCvd6DRHfIHloh1Acnxarrmks/edit?usp=sharing)
