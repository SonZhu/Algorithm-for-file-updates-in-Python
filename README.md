# Algorithm for File Updates in Python

## Project Overview
In this project, I act as a security analyst for a healthcare company responsible for managing access to restricted subnetworks containing sensitive patient health records [cite: 5, 6]. Access is controlled via an allow list of IP addresses [cite: 7]. This algorithm automates the process of cross-referencing this allow list against a "remove list" of unauthorized employees and updating the file accordingly [cite: 9, 107].

## Scenarios and Goals
The primary goal is to ensure that only authorized employees have access to restricted content [cite: 5]. Manually updating these lists is prone to human error; therefore, this Python script provides an efficient, automated solution to maintain security protocols [cite: 110].

## Technologies Used
* **Language:** Python [cite: 1, 9]
* **File Handling:** `with open()` statements for reading and writing files [cite: 12, 86]
* **Data Manipulation:** String methods (`.read()`, `.split()`, `.join()`) and list operations (`.append()`) [cite: 23, 37, 84, 131]

## Algorithm Steps

### 1. Open and Read File Contents
The script begins by defining the file names for the allow list (`allow_list.txt`) and the remove list (`remove_list.txt`) [cite: 14, 15, 16]. Using `with` statements, the script opens both files in read mode (`"r"`) and uses the `.read()` method to convert the contents into strings for processing [cite: 12, 13, 23, 24].

### 2. Convert Strings to Lists
To iterate through the IP addresses, the strings are converted into lists using the `.split()` method [cite: 36, 37]. This splits the text based on whitespace, making individual IP addresses easier to manage [cite: 47, 48].

### 3. Iterate and Filter the Allow List
The algorithm iterates through the `ip_addresses` list. To follow best practices and avoid errors caused by modifying a list during iteration, a new list called `ip_address_match` is created [cite: 113, 115, 128]. 
* The script checks if each `element` in the allow list is **not** present in the `remove_list` [cite: 129, 130].
* If the IP address is not in the remove list, it is appended to the `ip_address_match` list [cite: 131].
* Finally, the original `ip_addresses` variable is updated with the filtered list [cite: 132].

### 4. Update the Original File
The revised list of IP addresses is converted back into a single string using the `.join()` method, with each IP address placed on a new line (`"\n"`) [cite: 84, 85, 134]. The script then opens the original `allow_list.txt` in write mode (`"w"`) and overwrites it with the updated content [cite: 86, 135, 136].

## Summary
This automated workflow significantly reduces the risk of manual errors in access management [cite: 110]. By leveraging Python's file handling and list manipulation capabilities, the company can ensure that patient records remain secure and accessible only to authorized personnel [cite: 110].
