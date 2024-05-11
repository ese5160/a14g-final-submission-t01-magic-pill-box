

# Magic Pill Box --- You don't want to miss out!!
- Author:  Yu-Pin Yi, Haowei Chen
- GitHub Repository URL: [Link](https://github.com/ese5160/a14g-final-submission-t01-magic-pill-box)
- Public Website Page URL: [Link](https://ese5160.github.io/a14g-final-submission-t01-magic-pill-box/)

## 1. Video Presentation

- [Video Presentation](https://youtu.be/nQqyR8lDyXY?si=AE45nUH7O6IaNKej)

## 2. Project Summary

### Device Description

- The Magic Pill Box is designed to help elderly people who are not familiar with phone and tablet devices to aid their medication. The solution is using an IOT device and remote access.

### Inspiration

- My grandparents are diagnosed with high blood pressure and are taking medicine on a daily basis. However, they keep forgetting to take the pills. First, me and my parents would give them a call to remind them, and they still forget to take the pill after hanging up the phone. We eventually bought them a smart pill box, but they are not so familiar with the setup, and still not working as we expected. This is when I came up with the idea of Magic Pill Box.

### Device Functionality

- The Magic Pill Box is made with a few interesting functions. First of all, the safe lock function which is integrated with 3 electric magnets and a buzzer. When the buzzer is beeping, it reminds the user to take the pill and based on the number on the OLED screen, the user will need to take the pills from the corresponding compartment. Before taking the pills, the user needs to press the switch to open the compartment by unlocking the electric magnets. Once the user eats the pills and closes the lid, the lid will then press the button sticked inside the compartment and shut off the buzzer.

- The Magic Pill Box is also equipped with the temperature and humidity sensor, and the purpose is to monitor the storage condition. If there's an abnormal reading, the buzzer will start beeping and send the user a notification that the storage condition is dangerous to the medicine.

- The user can use the node-red system to set up the alarm schedule.

### Challenges

- There are many challenges during the development. The first challenge we ran into was debugging the hardware issue, which had something to do with the component on the circuit board. For example, we were stuck on the I2C device development for almost 2 weeks and turned out to be a pin mapping error. The second challenge was developing firmware. Since we needed to write all freeRTOS drivers to our sensors, it took us a while to test and debug. The last challenge was casework design. We spent a lot of time on modifying the 3D design of the casework and had to print multiple prototypes to test the device and ends up printing 2 version of the pill box.

### Prototype Learnings

- The biggest lesson I learned from this project was to start things early and avoid sudden changes in design. The other thing I think we can improve is start casework design based on the firmware, and not the other way around. I spent a lot of time on how to make a perfect casework to fit my hardware, and in the end, it turned out there were lots of things that needed to be modified.

### Next Steps

- In the future, I am planning a two-phase update on this device using Over-The-Air Firmware Updates (OTAFU). First, I want to add more information to the screen(time/temperature/humidity). Next, I will add a UI function in which the user can set the schedule and change the storage condition threshold directly on the user interface.

### Takeaways from ESE5160

- It is a class that really helped me getting more into the embedded system and IOT device. I really enjoyed the circuit board development process.

- [Node-Red UI Link](http://52.186.82.19:1880/ui/)

- [Altium Project Link](https://upenn-eselabs.365.altium.com/designs/2E1710E5-2220-46EC-B8F9-26C9D24CF3C1)

## 3. Hardware & Software Requirements

- For the I2C part, we hope to have 3 i2c devices at first. The temperature and humidity sensor (SHTC3) to measure the environment, the OLED screen to show information,and a weight sensor that detects whether the user have take or put something from the pill box. At last, we only finish up setting the SHTC3 and the OLED screen.

- At first, we hope to use the MCU to control the magnet. However, we mess up with the mosfet circuit that use to be act as a switch. At last, we come up with a solution by using an actual switch to control the magnet and a button embeded in the small pill box to detect the open and close case of the box.

## 4. Project Photos & Screenshots

### Casework

- ![Casework](img/casework2.jpg)
- ![Casework](img/casework1.jpg)

### a. The standalone PCBA, top

- ![PCBA Top View](img/board_front.jpg)

### b. The standalone PCBA, bottom

- ![PCBA Top View](img/board_back.jpg)

### c. Thermal camera images while the board is running under load 

- ![Thermal Image](img/heatgun.jpg)

### d. The Altium Board design in 2D view

- ![Ground Plane View](img/ground.png)
- ![Power Plane View](img/power.png)

### e. The Altium Board design in 3D view

- ![3D View](img/3dView.png)

### f. Node-RED dashboard

- ![Node-Red Dashboard](img/node_red_UI.png)

### g. Node-RED backend

- ![Node-Red Backend](img/node_red_backEnd.png)

### h. Block diagram

- ![Block Diagram](img/system_diagram.png)
- ![Block Diagram](img/block_diagram.png)
