# Heartbeat Documentation Open Codes Hackathon 2018

## Team Members
- Jannis Hörner _([salier89](https://github.com/salier89))_
- Patrick Piatkowski _([derpatrick](https://github.com/derpatrick))_
- Vitalij Selynin _([VitalijSelynin](https://github.com/VitalijSelynin))_
- Markus Spöri _([mspoeri](https://github.com/mspoeri))_

## Inspiration
Coming from the embedded health devices section, most of the team members shared one question: <br>
Is it possible to build cheap devices with acual technology for medical use? <br>
Can we build a cheap ECG (electrocardiogram) from scratch?

*But how to visualize the data?* <br>
Better question:<br>
_How to **perceive** it?_

The key is full perception through **music** and **data curves**. - *But how?* -> See next section

## What it does
A full stack implementation of an ECG monitor, 
beginning by the analog signals captured from your skin ending in a remote web monitor visualizing multiple ECG devices and making them audible.<br>
Heartbeat connects to one or more IoT devices recording an electrocardiogram to get health data from the users.
The health data is visualized in a web application.

The web application also uses the heart rate to play some music - literally the sound of your heart ;)

## How I built it
The Flow of our Heartbeat application roughly looks like this:

- The _ECG_ is an IoT device with soldered [copper coins](https://de.wikipedia.org/wiki/1-Cent-M%C3%BCnze) connected to a microcontroller. 
- The Microcontroller sends its data to the [mBed Cloud](https://www.mbed.com/)
- A [Spring](https://spring.io/) backend queries the data and applies filtering
- The filtered data is then queried by the [Angular](https://angular.io/) frontend
  - The frontend displays the data in a chart
  - Also the data is mapped to musical notes to play some nice tune :)

