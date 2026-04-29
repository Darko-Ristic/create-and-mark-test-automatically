# Automated Quiz Creation & Scoring Program

This project lets you automatically create and score test created using question from text file. It's made to help with grading multiple tests quickly and easily.

---

## Download and Installation

Go to  
[https://github.com/Darko-Ristic/create-and-mark-test-automatically/releases](https://github.com/Darko-Ristic/create-and-mark-test-automatically/releases)  
Download the latest zip file. Unzip all files into a folder on your computer. Run `main.exe` or one of `.bat` files.

---

## Individual Bat Files

- `napravi bc_jpg test od pitanja_txt.bat`
  → creates a test image `bc.jpg` from a list of questions.

- `oceni bc_jpg.bat`
  → scores a single marked `bc.jpg` test image.

- `oceni_sve.bat`
  → scans and scores all test images in the `testovi` folder automatically.

- All `.bat` scripts use `main.exe` behind the scenes — so you don't need to run this file yourself.

---

## How To Mark Multiple Tests At Once

- Place all your `.jpg` test with different names into the `testovi` folder.
- Run `oceni_sve.bat` to scan, score, and save results.
- Results for each test will appear as `.txt` files in the `out` folder.
- At the end, the script will show you the score of each each test.

---

## Folders and Files

- Batch files (.bat) let you run the different steps without typing commands.
- The main program is `main.exe` (you can pass it `--shouldGenJPG` to create new test from `pitanja.txt`).
- The `testovi` folder holds your input test `.jpg` files.
- The `out` folder gets new `.txt` files with detailed results for each test.

---

## CUDA and GPU Errors

If you have an NVIDIA GPU and see errors about missing CUDA libraries, you may need to:

- Install cuTENSOR using  
  `python -m cupyx.tools.install_library --cuda 12.x --library cutensor`  
  or download it from NVIDIA and place `cutensor.dll` next to `main.exe`.

- Install cuDNN with  
  `py -m pip install nvidia-cudnn-cu12`

---

## Visual C++ Redistributable Problems

If you are missing DLL files, install the [latest Visual C++ Redistributable for Windows (x64)](https://aka.ms/vs/17/release/vc_redist.x64.exe).

---

## Getting Help and Reporting Issues

If something doesn't work:
- Go to the [GitHub Issues page](https://github.com/Darko-Ristic/create-and-mark-test-automatically/issues).
- Click "New Issue" and describe what happened.
- Add any error messages.
