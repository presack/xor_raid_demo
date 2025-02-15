# XOR RAID Demonstration

This project provides an **interactive HTML** page that teaches how **XOR** (exclusive OR) can be used to generate **parity** in a RAID (Redundant Array of Independent Disks) system. It’s intended for both **individual learners** and **teachers** who want to demonstrate the fundamentals of XOR and RAID parity in a hands-on way.

---

## Features

1. **Generate Drives**  
   - Randomly creates 8 bits for Drive 1 and Drive 2.  
   - Lets you fill in a Parity Drive row, showing how XOR is used to ensure data redundancy.

2. **Check Parity Answers**  
   - Verifies if your manually entered parity bits match the actual XOR results.

3. **Simulate Drive Failure**  
   - Randomly fails either Drive 1 or Drive 2 (red flash animation).  
   - Shows the original bits of the failed drive in an “archived” row (blurred, with a hover-to-reveal eye icon if you choose to blur them).  
   - Replaces the main row bits with ‘X’ so the user can attempt to recover the drive.

4. **Check Drive Recovery**  
   - Once the user enters the recovered bits, a rolling highlight animation compares them to the archived bits, stepping one bit at a time.  
   - If correct, the row re-renders as a static success, and a big green message confirms successful recovery.

5. **Lesson / Info Toggle**  
   - Includes a lesson section describing XOR properties (e.g., x ^ x = 0, x ^ 0 = x) and the role of XOR in RAID.  
   - Displays references to further resources like Wikipedia articles or a linked video explanation.

---

## How It Works

1. **XOR-Based Parity**  
   - For each bit position, XOR the bits of Drive 1 and Drive 2 to compute the parity bit.  
   - When a drive fails, you can reconstruct its bits by XORing the surviving drive with the parity bits.

2. **UI Interaction**  
   - You can **generate** random drive data, then **enter** or **check** your parity.  
   - When a drive “fails,” the original bits are archived and partially blurred for demonstration purposes. The user manually attempts to re-enter the lost bits.  
   - Finally, the user checks the recovery. If correct, an animated highlight shows each bit is correct, culminating in a success message.

---

## Usage

1. **Clone or Download** this repository from GitHub:
   ```bash
   git clone https://github.com/presack/xor-raid-demo.git
  

## Motivation
   - Ideal for teachers wanting to demonstrate bitwise operations and data redundancy in a RAID system.
   - Great for self-learners to understand how simple XOR logic can restore data from incomplete sets.

## License
This project is licensed under the MIT License. See LICENSE for details.

You are free to use, modify, and distribute this code as you wish under the terms of the MIT license.

## Contributing
Contributions in the form of pull requests, bug reports, or feature suggestions are welcome! Whether you have an idea for a new animation, want to improve the UI, or have additional learning resources, feel free to open an issue or submit a PR.

Enjoy learning about XOR and RAID through this interactive demo!
