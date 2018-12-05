Michael Knapp

CSC-596 2018

Geological Strike and Dip Device with Interfacing with an Android mobil
application.

Project Summary Author: Michael Knapp

Team Development Department Leaders:

>   Dr. Anthony Clark……. Computer Science Department; Missouri State University

>   Dr. Matthew MacKay…. Geological Department; Missouri State University

Under-Graduate Team Members:

>   Ali Solomon

>   Michael Knapp

This project dramatically improved my understanding of software development, not
only in the software side of science but it pushed me to go beyond the keyboard,
into areas of study that I found to be surprisingly very interesting, rocks!
This solidified my confidence in the computer science field of study, and also
gave me a new understanding of the importance of cross training with other
degree fields to find new innovative ways to apply current tech in new ways.
This project pushed the limits of my ability in several areas from hardware
development like Arduino, breadboard, Adafruit and Spark Fun IMU while
leveraging new programing languages like dart and C. Also understanding how
Bluetooth communication and serial communication work and implementing these
concepts with multiple out-of-the-box tools, programing languages and libraries
working in unison. To using a Mobil application framework like Flutter to help
speed up the development of the smart phone application side of the project.
Flutter is a framework that helps by simplifying code using Dart pre-packaged
code modules called Widgets that are templets to build features such as buttons
or easy layout designs for the smart phone application that is needed to
interface with the hardware.

The focus of this project was to create a new piece of technology to replace
analog strike and dip tools. This antiquated device used by Geologists to gather
survey information needed to make predictions of mineral or gas deposits
underneath the points being tested. The idea is to create a hardware or device
to replace the antiquated analog device being used. Our goal was to create a new
electronic version that must interface with a smart phone and must be able to
find true north without GPS or a compass (magnetometer). This would insure more
accurate measurements were being recorded and would eliminate the need for a
compass to achieve the same or improved results. There are several problems that
we encountered in developing this project from start to finish but with some
help and a lot of online research one by one we tackled these issues.

The first hurdle this team had to overcome was picking the correct hardware to
use in this specific project. This was really headed by Dr. Clark because as the
only one with previous experience working with these specific hardware devices
his expertise was valuable to make sure we were covering all the possible
variables needed in gathering Gyroscope and Accelerometer data as well as the
compatibility of all the hardware. We first used an older Arduino as the mother
board for the project, but we soon learned that the Arduino board was not as
suited as the Adafruit because this would eliminate the need for additional
Bluetooth hardware. It contained all the hardware as the Arduino but with he
added low energy Bluetooth chip that we needed to communicate with the
Flutter/Dart application. For me I wanted to point out that I found it
especially difficult to picture the layout or the sequence of the project
beforehand without much expertise in either geology, hardware design and
implementation or Mobil application design. I luckily had some advice given to
me from the team members that had some expertise in these areas which helped me
overcome these limitations. One thing that I had not used in the past that
helped visualize the whole layout of the hardware was helped by the Fritizg
Diagram that Dr. Clark made. I have never used this software before, but this
helped in understanding the project as well as speeding up the process of
soldering the hardware to the breadboard.

The second hurdle was to pick an application framework that would be best suited
for this problem. I again lucked out and had a partner Ali that picked up this
task with determination to get it solved. With just a few weeks we had a working
basic app that had a few basic widgets involved in reading the data and
displaying that data on another view we called infinite scrolling widget. One
specific problem I would like to point out with the Flutter framework is that if
you have a space in your user profile this framework will not run with that
profile. It was something that really caused me a problem in getting it to work
on my computer, so I thought it was worth mentioning. Flutter is a lot like
Angular in that it takes specific design process that you need to adhere to or
it will not compile correctly. Like I mentioned earlier Flutter framework uses
Dart. This can be very helpful when you are familiar with the syntax but can be
very frustrating if you only familiar with coding HTML and JavaScript. Still
unable to actually receive data over Bluetooth commination we had to stop with
further progress here. The team then turned back to the problem of connecting
all the desired hardware.

Now I would like to move the focus back to working on the hardware side of the
project the next thing was to assemble all the specific hardware to get a basic
protype sending data. I found it somewhat easy to connect and Sodder all the
hardware to a breadboard. Ali and I first started connecting the Adafruit to the
board then we added the stepper motor and then the first Gyro. After a lot of
set up and backtracking we then found a good design of combination of the
Adafruit and a Gyro that was compatible with all other hardware needed. The
libraries with interfaced the Adafruit with the IMU-9250 Gyro were not
compatible. However, the LSM9DS1 Gyro was compatible with the Adafruit so the
team decided it was just easier to replace the incompatible Gyro instead of
editing the IMU-9250 library to make it compatible. In future designs we have
talked about using more than one Gyro it would be important for the Team or
Team’s working on this project to only use the LSM9DS1 Gyro. After configuring
the Arduino IDE to working with the specific Adafruit board, stepper motor and
the third Gyro (LSM9DS1) we were able to use a modified version of the example
sketches that came with the configuration it worked. From this point we were
able to power up the device and send all the Gyro data across a serial port \#
2. We then saved this data using a python program to CSV format to use as
testing the accuracy and consistency of the stepper and the gyro.

The Third big hurdle was to have some of the hardware modified i.e. the stepper
motor. We must have the device rotate 180 degrees one direction back 360 degrees
and then forward 180 to the start point. We needed insure before testing that
the motor would stay in a fixed place why we rotated it in the directions needed
to gather that data. After this was finished some of the team built, for lack of
a better term a large protractor to test the consistency of our motor in
repeating this process with little or no errors in rotating the correct degrees
and ending at 0 after a thousand rotations. With the testing complete we decided
that it would be best for saving processing time and the amount of data on the
Adafruit board it would be best to just send the minimal amount of data the
process true north. Then that data would be sent to the flutter application then
we would do the necessary processing to predict truth north.

In the next few weeks the plan is to have this data received via low energy blue
tooth to the flutter application. This application is already set up to display
this data in a readable format. I think this will be a good stopping point for
the next semesters team to pick up and refine the program we developed. It is
hard for me to predict how much or how many more problems they will have to
overcome before they have a finished product, but I do wish I was going to be
part of seeing it through. This has really been a fun project for me to be apart
of and I am glad that I was given the opportunity to help build something new
and innovative like this. The experience that I gained from learning new types
of hardware and mobile application design was much more than I expected when
started this project. I addition this project expanded my knowledge in coding
problems for Mobil application frameworks like Flutter/Dart and libraries plus
other “out of the box” tools that I don’t think I would have received from
taking classes in these areas. I appreciate how much this project has helped my
understanding of how a project like this is developed from start of picking the
hardware to the software side of planning through development.

The next team I am sure will pick up with further development of the flutter
side of the project. One area that I would like to see more improvement with the
next team is the layout design of the flutter application. Right now, it is in
the early development stages of just getting the basic data displayed. I am sure
there will be a need for more features from calibration settings of the gyro to
exporting the data to other software that can provide the customer with a usable
from of the data we are getting from this device. I am not sure what features
that will need to be added but I assume just like in our progress so far
envisioning the path of design comes with changes and backtracking. A project
like this, making something new and innovative always comes with unexpected
problems, finding the design path that works better than its analog
counterparts.
