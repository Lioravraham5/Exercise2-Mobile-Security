# Survive Game - README
# Overview

Survive Game is a simple yet engaging Android game where players must overcome challenges and arrive at their city by following the correct steps based on their ID. 
The game contains a bug in the initial APK that needs to be resolved to play and win.

# Bug Description
The game retrieves data from a URL to determine the player's state. However, the URL string in the `strings.xml` file contains invisible characters that corrupt the URL. These characters prevent the app from fetching the necessary data for the game to function.

<img src="https://github.com/user-attachments/assets/8853ee48-b2e5-4a19-b7a4-accf369bfbac" alt="WelcomePage" width="75%" height="75%">

## How the Bug Was Resolved
1) Opened the `strings.xml` file in the decompiled project.
2) Located the corrupted URL under the key `<string name="url">`.
3) Removed the invisible characters from the URL.
4) The corrected URL is:
   ```https://pastebin.com/raw/T67TVJG9```
5) Recompiled the app and verified that the URL fetched the correct data, enabling the game to start.

# How to Play
1) Enter your unique ID in the text input field on the main menu screen.
2) Press the "Start Game" button to begin the game.
   - The game will fetch data based on the provided ID.
   - Your ID determines the sequence of steps you must follow.
3) Once the game starts, navigate through the challenges by pressing the arrow buttons.

## How to Win - Survive and Arrive at Your City
### 1) Understanding Your ID:
* Your ID determines the correct sequence of directions. Each digit corresponds to an arrow button:

  `0`: Left

  `1`: Right

  `2`: Up

  `3`: Down
  
* Example: If your ID is 209234673, the game will compute the sequence based on the digits modulo 4.
### 2) Understanding Your ID:
* The game presents a sequence of challenges. Press the arrow buttons in the order determined by your ID.
### 3) Complete the Levels:
* If all directions are followed correctly, a toast message will display:
  ```
  Survived in [Your City]
  ```
* If you make a mistake, the game will show:
  ```
  You Failed
  ```
# My Playthrough
**ID Entered:** 209234673

**City:** Washington

For ID 209234673, the steps are:
* 2 % 4 = 2 → Up
* 0 % 4 = 0 → Left
* 9 % 4 = 1 → Right
* 2 % 4 = 2 → Up
* 3 % 4 = 3 → Down
* 4 % 4 = 0 → Left
* 6 % 4 = 2 → Up
* 7 % 4 = 3 → Down
* 3 % 4 = 3 → Down

<img src="https://github.com/user-attachments/assets/ed015b84-7428-4e78-a50b-8db6b014e04f" alt="WelcomePage" width="25%" height="25%">
