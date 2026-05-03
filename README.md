# Beginner Python Project: Automated Security File Updater

## Overview
This is a beginner-level Python project designed to demonstrate fundamental skills in file handling and list manipulation. The script automates a common security task: updating an access control list (allow list) by removing unauthorized IP addresses based on a separate "remove list."

## Goal
The objective of this project was to create a reliable way to manage access to restricted files, reducing the risk of human error associated with manual updates.

## Core Concepts Applied
* **File I/O:** Reading from and writing to `.txt` files using `with open()`.
* **String Processing:** Using `.read()`, `.split()`, and `.join()` to prepare data.
* **Logic & Iteration:** Using `for` loops and `if` statements to filter data.
* **Refactoring:** Improving code to avoid modifying a list while iterating over it.

## How it Works
1. **Importing Data:** The script reads `allow_list.txt` and `remove_list.txt` into Python as strings.
2. **Data Cleaning:** These strings are converted into lists to allow for individual IP processing.
3. **Filtering:** The script iterates through the allow list and builds a new list containing only the addresses that are **not** on the remove list.
4. **Final Update:** The filtered list is converted back into a newline-separated string and saved back to the original file.

## Why This Approach?
Initially, the script used `.remove()`, but I refactored it to use a new list instead. This ensures the loop remains stable and all unauthorized addresses are caught, which is a key learning point for Python beginners regarding list behavior.
