# PeaceSign

PeaceSign is a web application built for the [Code Without Barriers](https://codewithoutbarriers.devpost.com/) hackathon, 
designed to bridge communication gaps for the hearing-impaired by translating speech into sign language.

<p align="center">
  <img width="250" src="https://user-images.githubusercontent.com/58766039/171401680-1bda23d1-460f-43eb-9d80-3a0ef6bd3e87.png">
</p>

---

## Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![Azure](https://img.shields.io/badge/Microsoft_Azure-0089D6?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![Maintenance](http://unmaintained.tech/badge.svg)

> Note: The application requires valid Azure subscription keys in `keys.py` to function. 
> Replace all entries with your own keys from the Azure Portal.

---

## Features

**Speech-to-Text Transcription**
Accepts audio input and transcribes speech into text using Azure Cognitive Services. Supports 
both short-form audio and continuous speech from long-form video files.

**Sign Language Translation**
For each character in the transcription, the application retrieves the corresponding hand sign 
image and compiles the results into a downloadable output.

**Audio and Video Input Support**
Handles both direct audio recordings and video files by extracting and processing the audio 
stream for transcription.

---

## Architecture

| Component | Technology |
|---|---|
| Web framework | Flask |
| Speech transcription | Azure Cognitive Services (Speech SDK) |
| Sign image classification | Azure Custom Vision (earlier iteration) |
| Frontend templating | HTML, JavaScript |
| Form handling | forms.py (WTForms) |

> Note: Azure Custom Vision integration was part of an earlier iteration of the project. 
> The current version handles sign image retrieval differently. Refer to previous commits 
> for the original Custom Vision API request references.

---

## Demo

![Audio Demo](https://user-images.githubusercontent.com/58766039/168831788-59d49e22-e661-4a48-8337-ae2b99a72cc9.gif)
![Video Demo](https://user-images.githubusercontent.com/58766039/167899593-868e5258-6b80-4be3-9945-bdf8b5d9092d.gif)

---

## Getting Started

**Prerequisites:** Python 3.x, Git

```bash
# Clone the repository
git clone https://github.com/mlemxy/PeaceSign

# Create and activate a virtual environment
py -m venv .venv
.venv\scripts\activate

# Install dependencies
pip install -r requirements.txt

# Add your Azure subscription keys in keys.py

# Run the application
flask run
```

---

## License

MIT
