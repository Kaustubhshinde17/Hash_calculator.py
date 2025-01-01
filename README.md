# Hash_calculator.py
**COMPANEY**: CODTECH IT SOLUTIONS
**NAME**: Kaustubh Dattatray Shinde
**INTERN ID**: CT08IFP
**BATCH DURATION**: January 10th, 2025 to February 10th, 2025.
**MENTOR NAME**: NEELA SANTOSH
#DESCRIPTION:
This Python program provides a simple interface for calculating the SHA-256 hash of either a file or a text input. It combines functionality for file handling, hashing, and a graphical user interface (GUI) using the hashlib and tkinter modules. The code starts by prompting the user to choose between two options: hashing a file or hashing a text string. Based on the selection, the program executes the relevant logic.

Hashing a File
If the user selects option 1, a tkinter-based GUI window appears, allowing the user to select a file from their system. The core of the file hashing function is calculate_hash, which reads the selected file in chunks of 8192 bytes. It uses the "walrus operator" (:=) to assign and check the result of the file reading in a single line. Each chunk is fed into the SHA-256 hashing algorithm using the hash.update method. Once all chunks are processed, the function returns the hexadecimal representation of the computed hash. If the file cannot be read (due to permission issues or other errors), the program gracefully handles the exception and notifies the user.

Hashing a Text String
If the user selects option 2, they are prompted to enter a text string via the console. The program passes this string to the calculate_string_hash function, which encodes the string in UTF-8 format and computes its SHA-256 hash. The resulting hash is displayed to the user as a hexadecimal string.

Tkinter Integration
For file selection, the program uses a tkinter GUI. The root window is initialized and configured to be small, centered, and always on top of other windows for better visibility. A label provides instructions, and a button allows the user to open the file dialog. Once a file is selected, the root window closes automatically. The file selection process integrates seamlessly with the hashing logic, ensuring a smooth user experience.

User Input Validation
**OUTPUT**: ![Screenshot 2025-01-01 162033](https://github.com/user-attachments/assets/be0e36cf-43ce-4257-8757-0df687e2c28e)
The program includes checks to ensure valid user input. If the user enters anything other than "1" or "2" at the initial prompt, the program outputs an error message and exits gracefully. Similarly, it handles cases where no file or text input is provided, avoiding crashes and improving robustness.

Error Handling
Error handling is a significant focus of the program. For file operations, exceptions are caught to handle scenarios like inaccessible files or invalid paths. This ensures that the program provides clear feedback rather than terminating unexpectedly.
