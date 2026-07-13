# 🐧 Day 4 - Mastering Vim Editor

## 🎯 Objective

Learn the fundamentals of the Vim Editor and practice essential commands for editing files efficiently in a Linux environment.

## 📘 What is Vim?

Vim (Vi Improved) is a powerful terminal-based text editor available on most Linux systems. It is widely used by Linux administrators, DevOps engineers, and developers for editing configuration files, scripts, and application code.

## 📘 Why Learn Vim?

* Lightweight and fast
* Available on almost every Linux server
* Efficient keyboard-based editing
* Essential for remote server administration
* Widely used in DevOps and Cloud environments

## 💻 Commands Practiced
### 📝 Modes & File Operations

* i – Enter Insert mode
* Esc – Return to Normal mode
* :wq – Save changes and exit
* :q – Quit Vim
* :q! – Quit without saving changes

### 🔍 Search & Replace

* /word – Search forward for a word
* ?word – Search backward for a word
* :5 – Jump to line number 5 (replace 5 with any line number)
* :5s/old/new – Replace the first occurrence on a specific line
* :5s/old/new/g – Replace all occurrences on a specific line
* :%s/old/new/g – Replace all occurrences throughout the file
* :noh – Clear search highlights

### 🧭 Navigation & Editing

* gg – Go to the first line
* Shift + G (G) – Go to the last line
* :set nu – Show line numbers
* :set nonu – Hide line numbers
* u – Undo the last change
* Ctrl + r – Redo the last undone change
* yy – Copy (yank) the current line
* dd – Delete the current line
* p – Paste below the cursor
* Shift + P (P) – Paste above the cursor

## ✅ What I Practiced

* Opened and edited files using Vim
* Switched between Insert and Normal modes
* Saved and exited files
* Searched for words inside files
* Performed search and replace operations
* Navigated quickly using Vim shortcuts
* Copied, deleted, pasted, undo, and redo operations
* Enabled and disabled line numbers

## ❌ Mistakes I Made

* Wrong Command :q
* Error No write since last change (add ! to override)
* Correct Command :wq or :q!

Another Mistake
* Wrong Command :set number
* Correct Command-:set nu

## 💡 Key Learnings

* Vim works with different modes, and understanding them is essential.
* Search and replace commands save a lot of time while editing configuration files.
* Keyboard shortcuts improve editing speed significantly.
* Vim is an essential tool for Linux administration and DevOps.

## 📸 Outputs
<img width="1920" height="1080" alt="Screenshot 2026-07-13 214844" src="https://github.com/user-attachments/assets/7755d64c-eef8-4b97-92cb-09577d48166e" />
<img width="1920" height="1080" alt="Screenshot 2026-07-13 215218" src="https://github.com/user-attachments/assets/8229cd88-175d-4a04-ad7a-74bb057415e2" />
<img width="1920" height="1080" alt="Screenshot 2026-07-13 215605" src="https://github.com/user-attachments/assets/079ae0b6-c60c-46b2-9584-1365461c4032" />


