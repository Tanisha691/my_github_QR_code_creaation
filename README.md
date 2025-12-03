# my_github_QR_code_creaation
This project is a simple and efficient QR Code Generator built using Python. It can generate QR codes from any text, URL, or image link, and save them automatically as an image file.
🚀 Features

✅ Generate QR code from any text
✅ Generate QR code from any URL (website, Google Drive link, image link, etc.)
✅ Customizable box size, border size, error correction
✅ Saves QR code automatically as PNG
✅ Clean, beginner-friendly Python code
✅ Works on all operating systems (Windows, Linux, Mac)

🛠️ Technologies Used

Python

qrcode library

Pillow (PIL)

VS Code (optional)

📥 Installation

Install the required library using:

pip install qrcode[pil]

📜 Usage
 Generate QR Code from Text or URL
   import qrcode

img_data="https://github.com/Tanisha691"

# Create QR code object
qr = qrcode.QRCode(
    version=1,            # size of QR code (1–40), 1 is smallest
    error_correction=qrcode.constants.ERROR_CORRECT_H,
    box_size=10,          # size of each square
    border=4,             # border size
)

# Add data to QR
qr.add_data(img_data)
qr.make(fit=True)

# Create the image
img = qr.make_image(fill_color="black", back_color="white")

# Save image to file
img.save("my_github_code.png")

print("QR Code Generated Successfully!")
