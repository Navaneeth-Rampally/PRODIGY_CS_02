# PRODIGY_CS_02
This is the second task in the internship program

Task2: "Pixel Manipulation for Image Encryption"

Key Features:

Encryption: Encrypts an image by applying a user-defined key to each pixel's red, green, and blue (RGB) components.
Decryption: Decrypts the encrypted image using the same key, reversing the encryption process.
User-Friendly: Accepts the image path and encryption key as input for easy customization.
Clear Output: Prints confirmation messages upon successful encryption and decryption.

Installation:

Ensure you have Python installed on your system (https://www.python.org/downloads/).

Open a terminal or command prompt and install the required library:

Bash
pip install Pillow

Usage:

Save the code: Create a Python file (e.g., image_encryption.py) and paste the code into it.
Replace the image path: Modify the image_path variable in the example usage section with the absolute path to your image file.
Set the encryption key: Choose a desired integer value for the encryption_key variable.
Run the script: Execute the Python script using your preferred method (e.g., from the terminal: python image_encryption.py).
Explanation:

Import Library:

from PIL import Image: Imports the necessary Image class from the Pillow library for image processing.
encrypt_image Function:

Parameters:
image_path (str): The path to the image file to be encrypted.
key (int): The encryption key (integer value).
Process:
Opens the image using Image.open().
Loads the pixel access object using img.load().
Retrieves the image dimensions (width and height) using img.size.
Iterates through each pixel using nested loops:
Extracts the red, green, and blue (RGB) components using r, g, b = pixels[x, y].
Applies the encryption operation: r = (r + key) % 256, g = (g + key) % 256, b = (b + key) % 256.
The addition modulo 256 ensures the result stays within the valid range (0-255) for RGB values.
Updates the pixel value with the encrypted RGB components: pixels[x, y] = (r, g, b).
Saves the encrypted image as encrypted_image.png using img.save().
Prints a confirmation message indicating successful encryption.
decrypt_image Function:

Parameters:
encrypted_image_path (str): The path to the encrypted image file.
key (int): The encryption key (same key used for encryption).
Process:
Opens the encrypted image using Image.open().
Loads the pixel access object using img.load().
Retrieves the image dimensions (width and height) using img.size.
Iterates through each pixel using nested loops:
Extracts the red, green, and blue (RGB) components using r, g, b = pixels[x, y].
Applies the decryption operation (reversing the encryption): r = (r - key) % 256, g = (g - key) % 256, b = (b - key) % 256.
Updates the pixel value with the decrypted RGB components: pixels[x, y] = (r, g, b).
Saves the decrypted image as decrypted_image.png using img.save().
Prints a confirmation message indicating successful decryption.
Example Usage:

Sets the image_path variable to the path of your image file.
Defines the encryption_key variable with your chosen integer value.
Calls the encrypt_image function to encrypt the image.
Calls the `decrypt
