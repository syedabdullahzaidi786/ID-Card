```markdown
# ID Card Generator

This Python-based ID card generator allows you to create professional ID cards with custom user information, including name, roll number, and more. The tool also supports adding user images, logos, and generating QR codes for additional details. 

![ID Card Sample](id_card_output.png)
## Features

- Add personal information like Name, Roll Number, City, Center, and more
- Include a user photo with a green border
- Add a logo to the ID card
- Automatically generate a QR code for additional information
- Customize the layout with an easy-to-modify script
- Outputs a high-quality PNG image with a green-bordered design

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Customization](#customization)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone this repository to your local machine:

```bash
git clone https://github.com/yourusername/id-card-generator.git
cd id-card-generator
```

2. Install the required Python libraries:

```bash
pip install -r requirements.txt
```

This will install the following dependencies:
- `Pillow` for handling images
- `qrcode` for generating QR codes

## Usage

1. Prepare the following items:
    - A user image (JPEG or PNG format)
    - A logo image (PNG format)

2. Modify the Python script `id_card_generator.py` with the user's details (e.g., Name, Roll Number).

3. Run the script:

```bash
python id_card_generator.py
```

4. After the script runs, an ID card image (`id_card_output.png`) will be saved in the project directory.

### Example

In the script, update the following fields to generate a custom ID card:

```python
name = "John Doe"
roll_no = "12345"
city = "Karachi"
batch = "61"
user_image_path = "path_to_user_image.jpg"
logo_image_path = "path_to_logo.png"
```

After running the script, the ID card will be generated and saved.

## Customization

### Fonts

By default, the script uses `arial.ttf` for text. You can replace the font files with any other font you prefer by updating the font paths in the script. Ensure that the `.ttf` files are uploaded or present in the working directory.

```python
font_large = ImageFont.truetype("arialbd.ttf", 40)
font_medium = ImageFont.truetype("arial.ttf", 30)
font_small = ImageFont.truetype("arial.ttf", 25)
```

### Image and QR Code Placement

You can adjust the positioning of images (logo and user photo) by modifying the following section of the code:

```python
img_x, img_y = 800, 100  # Coordinates for the user image
qr_image = qr_image.resize((150, 150))  # Resize QR code if needed
id_card.paste(qr_image, (800, 400))  # Position for QR code
```

## Project Structure

```bash
id-card-generator/
│
├── id_card_generator.py   # Main Python script for generating the ID card
├── requirements.txt       # Python package requirements
├── README.md              # Project documentation
├── sample_images/         # Directory for sample images (optional)
│   ├── user_image.jpg
│   └── logo.png
└── id_card_output.png     # Generated ID card output (created after running the script)
```

## Contributing

Contributions are welcome! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add a new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a Pull Request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---
