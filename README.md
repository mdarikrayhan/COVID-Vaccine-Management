# COVID Vaccine Management

An offline, menu-driven console program in C for registering citizens for COVID-19 vaccination, screening them, recording their first and second doses and keeping track of vaccine stock. The program calls itself "Vaccine Regulation". It was a group mini project for CSE-2104 Data Structures and Algorithms-I at BAUET, submitted in September 2021. The idea was a registration system that works without an internet connection, for places where online registration is hard to reach.

## Features

- **Main menu:** shows the current date and time and the total number of vaccine doses in stock.
- **Registration:** records a citizen's name, gender, date of birth (`DD-MM-YYYY`), zip code, national ID (NID) number and phone number.
- **Take vaccine:**
  - finds the citizen by NID and asks five screening questions: underlying medical conditions, allergies, pregnancy or breastfeeding, a positive test in the past 28 days, and fever;
  - a citizen who answers "No" to all five chooses a vaccine from the stock list;
  - the program then saves the vaccine name and the first-dose date, takes one dose off that vaccine's stock and shows a date for the next dose;
  - at the second visit it shows which vaccine to take and records the second-dose date.
- **Vaccine information:** show, add, update and delete vaccines (name and quantity).
- **Citizen list:** all citizens, those with a first dose, those with a second dose, or citizens of a given age; update or delete a citizen.
- **Search:** find a citizen by NID or phone number, with their age and vaccine.
- **Storage:** citizens are kept in `record.bin` and vaccines in `vaccine.bin`, both binary files in the working directory.

## Tech stack

C, built with MinGW in Visual Studio Code on Windows. The program uses `conio.h` and `windows.h` for `getch()` and cursor positioning, so it runs on Windows only.

## Getting started

On Windows with MinGW:

```
gcc Vaccine_Regulation.c -o Vaccine_Regulation.exe
Vaccine_Regulation.exe
```

Run it from the repository folder. The main menu reads `vaccine.bin` on start-up, so that file must be in the working directory; the one in this repository holds a small sample stock. `record.bin` holds five sample citizens from our tests, with their birth dates, zip codes, IDs and phone numbers blanked; the program creates the file if it is missing.

## Project structure

```
Vaccine_Regulation.c      the whole program
vaccine.bin               sample vaccine stock
Vaccine_Regulation.pptx   project presentation slides
Script_Final.txt          speaker notes for the presentation
```

## Team

Md Arik Rayhan, Fathma Khatun Mim, Samia Rahman Nova, Sadia Haq Tamanna and Md Tanvir Ahmed Tagim.

## Author

Md Arik Rayhan — [mdarikrayhan.com](https://mdarikrayhan.com)
