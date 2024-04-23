# Gravity-Waves-Analysis-Tool


## Introduction

Hello, thank you for using the Gravity Wave analysis tool. This tool was created in a semester-long project course called CSC 380 at Suny Oswego University. This tool was also made with the help form Dr.Barber,
Dr.Kanbur and Dr.Tenbergen at Suny Oswego University and Dr.Gong at the NASA Goddard Space center. This tool is great for quick analysis of Radiosonde Data to get a set list of parameters from GDL, and a set list
of Graphs. These results will be placed into a PDF which you can then download onto your computer for use outside of our website.

## How to Access
This Website has been graciously been hosted for free, by the Suny Oswego Computer Science department and Dr.Tenbergen at http://moxie.cs.oswego.edu:10761/

However if for some reason the link does not work or you wish to setup this website on your computer or a server below is a guide to deploy the website.

## Authors

This tool was created by:
Thomas Marten Email: marten.j.th@gmail.com, [Github](https://www.linkedin.com/in/thomas-marten-080b4b234/), [LinkedIn](https://www.linkedin.com/in/thomas-marten-080b4b234/)

Daniel Maslowski Email: dpmaslowski@gmail.com, [Portfolio](https://danpmas.github.io/)

Duncan Zaug Email: zaugboys@gmail.com, [Github](https://github.com/Offhornet28/Duncan-College-Projects)

Justyce Countryman: countrymanjustyce2002@gmail.com, [Github](https://github.com/lljustycell999) [LinkedIn](https://www.linkedin.com/in/justyce-countryman-391b40294/) [Portfolio](https://lljustycell999.github.io/JustyceCountryman.github.io/)

Tim Dube [Portfolio](https://timmydube.vercel.app/) 

###### Special Thanks to
Dr.Barber for suggesting such great additions and features and helping us with all the science behind this tool. 

Dr.Kanbur for meeting with us and connecting us with Dr.Gong and helping orientate ourselves when this project started. 

Dr.Gong for being our lighthouse and giving us the code needed to run GDL. Your work and effort put into that code has made this project possible and for visiting us at suny oswego.

Dr.Tenbergen for helping us be the best we could be and for pushing us to work hard everyday. This project would have long ago failed if it was not for your constant guidance, support and teaching that you do everyday. Keep being awesome. 


## How to deploy

### How to un-deploy

### Important Notes on docker

## Miscellaneous Information

### What is GDL?
GDL (GNU data language)  is an open source free to use version of IDL (Interactive data language). 
We used GDL since IDl licenses are expensive upwards of 2000 dollars, and we wanted this product to be free and easily usable by users. 

### What Parameters and Graphs are generated?

The graphs created are as listed:

- Weather Balloon Travel Path 
- Temperature vs. Altitude
- Temperature Perturbation
- Hodograph
- Ascension rate
- U wind component vs. Altitude
- V wind component vs. Altitude
- U’ wind component Perturbation
- V’ wind component Perturbation

Every Graph will be produced twice once for Troposphere and once for Stratosphere

The Parameters created are as listed:

- Zbot (km) (Start Altitude) 
- Ztop (km) (End Altitude)
- Horizontal Wavelength (km)
- Vertical Wavelength (Km)
- Mean Phase Propagation Direction (deg)
- Upward Propagation Fraction
- Zonal Momentum Flux (m^2/s^2)
- Meridional Momentum Flux (m^2/s^2)
- Potential Energy (J/Kg)
- Kinetic Energy (J/Kg)
- Intrinsic Frequency (s^-1)
- Coriolis Parameter (J/Kg)
	
These Parameters are repeated twice, once for the Troposphere and one for the Stratosphere. The estimated height for the tropopause is also provided in kilometers. 


## Trouble Shooting
