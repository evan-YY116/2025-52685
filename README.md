# 2025-52685

## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)
* [Screenshots](#screenshots)
* [Setup](#setup)
* [Usage](#usage)
* [Project Status](#project-status)
* [Room for Improvement](#room-for-improvement)
* [Acknowledgements](#acknowledgements)
* [Contact](#contact)
## General info
Project Title: Library Quiet Reminder Using Micro:bit
Author: Yiming Liu
Student ID: 14554378
Course: 52685 Working with Data & Code
Project Purpose

This project aims to design an interactive audio-visual quiet reminder system for the UTS Library, using LED displays and audio feedback to encourage students to remain quiet.

Problem Solved

Students are often disturbed by noise while studying in the library, and traditional "Keep Quiet" signs lack immediate reminder functionality.

This project aims to use simple interactive design to provide a more user-friendly, real-time reminder of noise.

Motivation

As a student who frequently studies in the library, I hope to improve the concentration and comfort of shared study spaces by combining programming and hardware.

## Technologies
Project is created with:
Micro : V1
Micropython
Makecode editor

## Features
Button A: In normal mode, displays a smiley face animation four times.

Button B: Sounds three times and displays a sad face, indicating excessive volume.

LED Animation: Flashes an image four times in a cycle to indicate prompt feedback.

Audio Prompt: A buzzer produces a melody to enhance the interactive experience.

## Screenshots
<img width="1288" height="822" alt="fcf4d875cb85edd251e66103496029d0" src="https://github.com/user-attachments/assets/e14b1c09-1e73-4c7f-bd64-ed9dc54c2156" />

## Setup
The hardware and environment required for this project are as follows:
BBC Micro:bit V1 development board
USB data cable (for connecting to a computer)
Internet-connected computer (for writing and downloading programs)
External buzzer (for playing prompt sounds)
Installation & Environment Setup
Open the MakeCode editor
Copy and paste the Micro:Bit-Test-12(2).hex file in this repository into the editor.
Connect the Micro:bit development board to the computer using a USB data cable.
Click "Download" and burn the program to the Micro:bit.
After the program runs, press the buttons to test the functions:
Button A → Display a smiley face animation
Button B → Play a prompt sound and display a sad face

## USage
Press the A button → the LED display will flash four times with a smiley face.
Press the B button → the melody will play and a sad face will appear.

def on_button_pressed_a():
    for index in range(4):
        basic.show_icon(IconNames.HAPPY)
        basic.pause(100)
        basic.clear_screen()
        basic.pause(100)
input.on_button_pressed(Button.A, on_button_pressed_a)

def on_button_pressed_b():
    music.play(music.string_playable("C5 - C5 - C5 - - - ", 120),
        music.PlaybackMode.UNTIL_DONE)
    for index2 in range(4):
        basic.show_icon(IconNames.SAD)
        basic.pause(100)
        basic.clear_screen()
        basic.pause(100)
input.on_button_pressed(Button.B, on_button_pressed_b)

def on_forever():
    pass
basic.forever(on_forever)
## Project status
complete

## Room for improvement
Potential Improvements:

Use the Micro:bit V2's microphone to record sound;
Displaying happy and sad faces is too boring; additional animations could be added.
Future Development Plans:
Simulate more animated expressions, including a more humorous way to say "keep quiet."
Provide user-defined modes (brightness, rhythm, and beeping sound).
## Acknowledgement
This project was inspired by the frustrations I encountered while learning about library science.
This project is based on this tutorial.
I would like to thank my instructor, Dr. Evangeline Aguas, for providing guidance and ideas, and Dr. Andrew Stapleton for providing all the teaching materials and simulation supplies.
## Contact
Created by Yiming Liu (yiming.liu-3@student.uts.edu,au)
```


$ cd ../lorem
$ npm install
$ npm start
```
