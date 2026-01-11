# AlphaX Attendance System Introduction

This is a IOT based Attendance System meant to replace traditional registers used in schools and colleges. It has a dedicated attendance module which has ESP32S3 at its core, the modules has a 1602 LCD panel 
and a Keypad module (4x4) and a RFID (RC522) for access control. The module has capability of saving the students records onboard and also directly upload it to cloud database. Currently Supabase is being used
as the Cloud Database and Backend. There is a pairing website for viewing the attendance records and also downloading them. 

This project implements a **complete end-to-end pipeline**:

> **Embedded System → Cloud Backend → Web Dashboard**

---

## Features

### ESP32 Attendance Module
- ESP32-S3 based standalone attendance device  
- 16×2 LCD display with startup splash (**AlphaX**)  
- 4×4 keypad for marking attendance:
  - `A` → Absent  
  - `B` → Present  
- Automatic roll-by-roll navigation  
- Attendance upload to Supabase using HTTP REST API  
- Student list stored in ESP32 SPIFFS (`students.csv`)  
- Serial debug logs for diagnostics
- Currently the RFID module is disabled due to hardware glitches 

---

### Cloud Backend (Supabase)
- PostgreSQL database  
- Auto-generated REST API  
- Timestamped attendance records  
- Easily extensible for sessions, periods, subjects  

---

### Web Dashboard
- Pure **HTML + CSS + JavaScript**  
- No frameworks (lightweight & fast)  
- Register-style attendance table  
- One column per attendance session  
- Color-coded:
  - **P** → Present (green)  
  - **A** → Absent (red)  
- Automatic attendance percentage calculation
- Option for downloading the entire Attendance Record in csv format

---

## Author: Dhritiman Roy 



