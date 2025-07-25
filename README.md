Media Steganography Web App
A web-based Flask application that allows you to:

Hide secret text inside images (PNG), audio (WAV), or videos (AVI)

Hide a secret image inside a cover image (PNG)

Extract hidden text or images from stego media files

Features
🖼️ Image Steganography: Hide text or an image within a PNG image using LSB techniques

🎵 Audio Steganography: Hide text within WAV files

📹 Video Steganography: Hide text within AVI videos

🔎 Extraction: Extract secret text or image from stego media

🖱️ User-friendly web interface built with Flask and vanilla JS

Demo
<!-- Add screenshots/gifs here if possible -->
Getting Started
Prerequisites
Python 3.7+

pip install -r requirements.txt
Where requirements.txt includes:

text
flask
numpy
pillow
opencv-python
Run the App
bash
git clone https://github.com/yourusername/your-repo.git
cd your-repo
pip install -r requirements.txt
python app.py
The app runs by default at http://localhost:5000.

Usage
1. Hide Text or Image
Go to /encrypt

Select media type (Image, Audio, Video, or Image with Image)

Upload appropriate files:

For text steganography: upload cover file and enter text

For image-in-image: upload both cover and secret images (PNG)

Download your generated stego file

2. Extract Text or Image
Go to /decrypt

Select type (matching what was used for encoding)

Upload the stego file

For text-based stego: extracted text will appear in a textarea
For image-in-image: download and preview the extracted secret image

Project Structure
text
.
├── app.py                   # Main Flask web app
├── README.md
├── requirements.txt
├── static/
│   └── styles.css
├── templates/
│   ├── encrypt.html
│   └── decrypt.html
└── ...
How it Works
Text hiding: Stores each bit of secret text in the least significant bit (LSB) of each byte of the media file.

Image-in-image: Hides two most significant bits of each channel of the secret image into the two least significant bits of the cover image.

Security Note
This tool demonstrates basic steganography and is not robust against forensics or attacks. For secure communications, use cryptography together with steganography.

License
MIT License

Contributing
Pull requests and feature ideas welcome!

Author: BasanagoudaK







