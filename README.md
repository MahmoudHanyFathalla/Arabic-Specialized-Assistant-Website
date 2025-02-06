# Arabic Specialized Assistant Website

## Overview
This project is a web-based AI assistant built using FastAPI and OpenAI's API. The assistant processes user queries, interacts with OpenAI's language model, and provides intelligent responses. It uses Jinja2 for templating and serves static files to create a seamless user experience.

## Features
- **FastAPI-based web framework**: Provides a high-performance backend.
- **OpenAI Assistant API Integration**: Interacts with OpenAI's AI model to process and respond to queries.
- **Jinja2 Templating**: Uses Jinja2 to render dynamic HTML content.
- **Static File Support**: Serves static assets such as CSS, JavaScript, and images.
- **Ngrok Support**: Enables public access to the local server for testing and development.

## Prerequisites
Before running this project, ensure you have the following installed:
- Python 3.8+
- FastAPI
- Uvicorn
- Jinja2
- OpenAI Python SDK
- Ngrok (optional for remote access)

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repo/arabic-specialized-assistant-website.git
   cd arabic-specialized-assistant-website
   ```

2. Create and activate a virtual environment:
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```

## Configuration
1. Set up OpenAI API credentials.
2. Update the `assistant_id` in the script with your OpenAI assistant ID.
3. Optionally, configure Ngrok:
   ```sh
   ngrok config add-authtoken YOUR_NGROK_AUTH_TOKEN
   ```

## Running the Application
Start the FastAPI server:
```sh
uvicorn main:app --host 0.0.0.0 --port 8000
```

For public access via Ngrok:
```sh
ngrok http 8000
```

## API Endpoints
- **GET /**: Serves the main HTML page.
- **POST /ask/**: Processes user input, queries OpenAI, and returns responses.

## Project Structure
```
arabic-specialized-assistant-website/
│── static/              # Static files (CSS, JS, images)
│── templates/           # Jinja2 templates
│   ├── index.html       # Main UI template
│── main.py              # FastAPI application script
│── requirements.txt     # Project dependencies
│── README.md            # Project documentation
```

## Future Enhancements
- Implement user authentication.
- Improve error handling and logging.
- Add database integration for chat history.

## License
This project is licensed under the MIT License. Feel free to use and modify it according to your needs.
