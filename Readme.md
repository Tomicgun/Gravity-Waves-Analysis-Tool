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
Thomas Marten Email: marten.j.th@gmail.com, [Github](https://github.com/Tomicgun/Portfolio), [LinkedIn](https://www.linkedin.com/in/thomas-marten-080b4b234/)

Daniel Maslowski Email: dpmaslowski@gmail.com, [Portfolio](https://danpmas.github.io/)

Duncan Zaug Email: zaugboys@gmail.com, [Github](https://github.com/Offhornet28/Duncan-College-Projects)

Justyce Countryman: countrymanjustyce2002@gmail.com, [Github](https://github.com/lljustycell999) [LinkedIn](https://www.linkedin.com/in/justyce-countryman-391b40294/) [Portfolio](https://lljustycell999.github.io/JustyceCountryman.github.io/)

Tim Dube [Portfolio](https://timmydube.vercel.app/) 

###### Special Thanks to
Dr.Barber for suggesting such great additions and features and helping us with all the science behind this tool. 

Dr.Kanbur for meeting with us and connecting us with Dr.Gong and helping orientate ourselves when this project started. 

Dr.Gong for being our lighthouse and giving us the code needed to run GDL. Your work and effort put into that code has made this project possible and for visiting us at suny oswego.

Dr.Tenbergen for helping us be the best we could be and for pushing us to work hard everyday. This project would have long ago failed if it was not for your constant guidance, support and teaching that you do everyday. Keep being awesome. 


## How to Deploy
There is only one dependency for this tool that is not included with our code and that is Docker. You will need to install and set up docker on your computer to host this website. 
Please follow this [Link](https://www.docker.com/get-started/) to do that first. If you are setting this up on a server or a different machine please reach out to the server manager or machine manager and ask them to set up docker. 
If you are the manager please follow this [Link](https://docs.docker.com/engine/install/), and this [Link](https://docs.docker.com/compose/install/#:~:text=Docker%20Desktop%20includes%20Docker%20Compose,CLI%20which%20are%20Compose%20prerequisites.). Once the docker engine and or docker desktop is installed and running on your server/computer follow the steps below. 

For deploying this website on a computer or laptop follow these instructions:
1. Please click this link [Link](https://github.com/Tomicgun/Gravity-Waves-Analysis-Tool) to the public repository containing this guide and the code.
2. Copy the docker-compose.yaml file to your computer you can do this by using the github command line, if you are familiar with it, or use this [link](https://github.com/Tomicgun/Gravity-Waves-Analysis-Tool/releases/tag/v1.0) and click on the file shown bellow
![alt text](https://github.com/Tomicgun/Gravity-Waves-Analysis-Tool/blob/main/Images/Screenshot%202024-04-24%20095515.jpg)
4. Open up docker desktop and press ctrl+k or command+k on mac. Then type in this command dzaug/csc380_back_end_image then press the pull button just to the right of it.


![alt text][Image1]


5. Repeat step three but instead of typing in dzaug/csc380_back_end_image type in dzaug/csc380_front_end_image.
6. Open up the terminal for your machine and using the cd command to traverse your directory structure to where ever you downlaoded or copied the docker-compose.yaml file. If you use the download button in the github repo then it should be in your C:\Users\$username$\Downloads (windows)
7. Once the terminal is at the folder where the docker-compose.yaml then type this command docker compose up or docker-compose up (if on older docker engine version). This will spin up the two previously pulled images into containers and stored on your local machine.
8. open up docker desktop and click the containers tab where the two containers should now show up. Click on the containers.


![alt text][Image2]


9. Then click on the 10761 number which will open the website


![alt text][Image3]


10. There you go you should have the containers setup and running on your pc

For deploying this website on a server follow these instructions:
1. Open up the server termianl run these two commands docker pull dzaug/csc380_back_end_image and docker pull dzaug/csc380_front_end_image
2. Copy the docker-compose.yaml file onto the server
3. Traverse to the folder that contains the docker-compose.yaml file
4. run this command docker compose up or docker-compose up (if on a older version of docker engine)
5. You should now have it running on your server this program defualts to port 10761 if you need to change the port please look at the important notes section.

### How to Un-deploy
1. Open up your server/computer command line traverse directories until you are at the directory that contains the docker-compose.yaml file.Then run the docker compose down command or docker-compose down (if on a older version of docker engine)
3. If you are on a computer, open up docker desktop and open the volumes tab and delete the csc380_pdf-out and the csc380_text-in. If you are on a server then run these two commands docker volume rm csc380_pdf-out and docker volume rm csc380_text-in


![alt text][Image4]


4. That's it you have now taken down the two containers and cleaned up the volumes. 

### Important Notes

- If you wish to change the default port from 10761 to something else simply go into the docker-compose.yaml file and change line 12 from 10671:5000 to [desired port number]:5000. The structure is [server port]:[container port]. Save these changes and un-deploy the containers then re-deploy them for the changes to take effect.


- If you intend to make changes to the source code provided, please make sure to either edit a fork or make a copy of the code, you cannot edit the orgional code on this github repository. **We cannot guarantee changes made to code will not break certain features; you do this at your own risk**. Any changes made to the source code must be updated in the docker images, you can make copies of the images we have provided, but you will need to rebuild these images on your local machine.


- If you want to rebuild the frontend docker image you will have to create and activate the python virtual environment before building it in order for the frontend to run. Follow these steps/commands in order to do so:
  Within the directory containing all the frontend code and dockerfiles run:
    1. `python3 -m venv venv` to create the virtual environment 
    2. `. venv/bin/activate` to activate and go into the virtual environment
    3. `pip3 install flask` within the virtual environment to install flask
    4. Then close the terminal instance that is within the virtual environment.
  You are now ready to build the frontend image.  


## Miscellaneous Information

### What is GDL?
GDL (GNU data language)  is an open source free to use version of IDL (Interactive data language). 
We used GDL since IDL licenses are expensive upwards of 2000 dollars, and we wanted this product to be free and easily usable by users. 

### What Parameters and Graphs are Generated?

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


## Troubleshooting

### Common Problems/Solutions
#### Quality Control Data

**Most Errors occur due to bad data in the radiosonde file please make sure that all radiosond files clean up these issue:**
- Remove sections of data where radiosonde altitude drops unexpectedly
- Replace invalid data values with one of the following: "999999", "1000002", "-", "--", "999999.0", "999999.00", "999999.000", '-999.9', "-9999.9"
- Ensure radiosonde data includes both troposphere and stratosphere (each graph utilizes the  tropopause which requires data from entire atmosphere to calculate)

#### Known Errors
1. If you get a Insecure/SSL error on chrome pleasse follow this [link](https://support.google.com/chrome/answer/2392709?hl=en&co=GENIE.Platform%3DDesktop) and its instrctuions
2. If the UI looks cut offed or the buttons are cut off from the edge of the screen press ctrl +  or ctrl - to rezie the UI to proper proportions.
3. If it gives you a error file could not be processed please re-upload the sumitted file.
4. if it gives a no file part no file was provided in the file upload please re submitte the file.

#### How to submit a GitHub issue

1. Click this [link](https://github.com/Tomicgun/Gravity-Waves-Analysis-Tool/issues)
2. Then click the green issue button in the right upper corner
3. Please describe your error in as much detail as you can and give the exact error code given by the website
4. Click the submit new issue, we the authors will see these issues and can address them
   


## Credits Page
1. Dr.Dong Jie Gong (2009):Characteristics of Two Gravity Wave Sources in the US High Vertical-resolution Radiosonde Data,PhD. thesis
2. Dr. Kanbur
3. Dr. Barver
4. Dr. Tenbergen

[Image1]: https://github.com/Tomicgun/Gravity-Waves-Analysis-Tool/blob/main/Images/Screenshot%202024-04-21%20172442.jpg
[Image2]: https://github.com/Tomicgun/Gravity-Waves-Analysis-Tool/blob/main/Images/Screenshot%202024-04-21%20173852.jpg
[Image3]: https://github.com/Tomicgun/Gravity-Waves-Analysis-Tool/blob/main/Images/Screenshot%202024-04-21%20174000.jpg
[Image4]: https://github.com/Tomicgun/Gravity-Waves-Analysis-Tool/blob/main/Images/Screenshot%202024-04-22%20223515.jpg
