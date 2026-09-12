# Neural Style Transfer using AdaIN

A deep learning-based Neural Style Transfer application that combines the content of one image with the artistic style of another image to generate a stylized output image.

## 📌 Project Overview

This project implements **Neural Style Transfer using Adaptive Instance Normalization (AdaIN)** with PyTorch.

The application takes two images as input:

- 🖼️ **Content Image** – The image whose main structure and content are preserved.
- 🎨 **Style Image** – The image whose artistic characteristics are transferred.

The system extracts feature representations from both images using a pretrained VGG-based encoder. AdaIN then aligns the feature statistics of the content image with the style image, and a trained decoder reconstructs the final stylized image.

## ✨ Features

- 🖼️ Upload content and style images
- 🎨 Transfer artistic style using AdaIN
- 🧠 VGG-based deep feature extraction
- 🔄 Encoder-decoder based image reconstruction
- 🎚️ Control style intensity using the alpha parameter
- 🌐 Flask-based web interface
- 💻 Supports local execution on Windows

## ⚙️ How It Works

```text
       Content Image                 Style Image
             │                            │
             ▼                            ▼
       ┌────────────┐              ┌────────────┐
       │    VGG     │              │    VGG     │
       │   Encoder  │              │   Encoder  │
       └─────┬──────┘              └─────┬──────┘
             │                           │
             ▼                           ▼
      Content Features            Style Features
             │                           │
             └──────────┬────────────────┘
                        ▼
               ┌─────────────────┐
               │      AdaIN       │
               │ Style Statistics │
               │    Alignment     │
               └────────┬────────┘
                        │
                        ▼
                Stylized Features
                        │
                        ▼
                 ┌────────────┐
                 │   Decoder  │
                 └─────┬──────┘
                       │
                       ▼
                Stylized Image
```

### 1. Feature Extraction

A pretrained **VGG-based encoder** extracts deep feature representations from the content and style images.

### 2. Adaptive Instance Normalization

**AdaIN (Adaptive Instance Normalization)** transfers the style characteristics by aligning the channel-wise mean and standard deviation of the content features with the style features.

### 3. Image Reconstruction

The stylized feature representation is passed through a trained **decoder**, which reconstructs the final RGB image.

## 🛠️ Technologies Used

- **Python**
- **PyTorch**
- **Torchvision**
- **Flask**
- **NumPy**
- **Pillow**
- **HTML/CSS**

## 📂 Project Structure

```text
Neural-Style-Transfer-AdaIN/
│
├── Demo_IO_Images/
│
├── NST_Code/
│   ├── app.py
│   ├── train.py
│   ├── utils/
│   ├── templates/
│   ├── static/
│   ├── examples/
│   ├── experiment/
│   ├── content_data/
│   └── vgg_normalised.pth
│
├── code.ipynb
├── requirements.txt
├── README.md
├── Procfile.txt
└── .gitignore
```

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/aneeeshh/Neural-Style-Transfer-AdaIN.git
```

### 2. Navigate to the Project

```bash
cd Neural-Style-Transfer-AdaIN
```

### 3. Create a Conda Environment

```bash
conda create -n nst python=3.11
```

### 4. Activate the Environment

```bash
conda activate nst
```

### 5. Install Dependencies

```bash
pip install -r requirements.txt
```

## ▶️ Run the Application

Navigate to the application directory:

```bash
cd NST_Code
```

Run the Flask application:

```bash
python app.py
```

The application will start at:

```text
http://localhost:5000
```

Open the URL in your browser and upload a content image and a style image to generate the stylized output.

## 🧠 Model Components

### VGG Encoder

The pretrained VGG network acts as a feature extractor and converts images into meaningful deep feature representations.

### AdaIN

Adaptive Instance Normalization transfers the statistical characteristics of the style image to the content feature representation.

### Decoder

The decoder converts the transformed feature representation back into an image.

## 📚 Key Learning Outcomes

- Understanding Neural Style Transfer
- Understanding Adaptive Instance Normalization (AdaIN)
- Working with pretrained CNN architectures
- Feature extraction using VGG
- Understanding encoder-decoder architectures
- Image preprocessing using Pillow
- Tensor operations using PyTorch
- Integrating deep learning models with Flask
- Handling image input and output
- Running deep learning applications in a local environment

## 💻 Hardware Consideration

Neural Style Transfer is computationally intensive. The project is configured for local execution and can be used on CPU-based systems, although processing time depends on the available hardware and image resolution.

## 🔮 Future Improvements

- ⚡ GPU acceleration for faster processing
- 🖼️ Support for higher-resolution images
- 🎚️ More style-transfer controls
- 🎨 Support for multiple style images
- ☁️ Cloud deployment
- 📱 Improved responsive user interface

## 👨‍💻 Author

**Anish Mishra**

B.Tech CSE | Aspiring Data Analyst & AI/ML Engineer
