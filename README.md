# Chainlit with Gemini AI

This project integrates **Chainlit** with Google's **Gemini AI** (gemini-2.0-flash) using OAuth authentication.

## Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Jawadgem/Chatbot_Auth.git
   cd Chatbot_Auth
   ```

2. **Create a virtual environment (optional but recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install dependencies**
   ```bash
   pip install chainlit google-generativeai python-dotenv
   ```

4. **Set up environment variables**
   - Create a `.env` file in the project root.
   - Add the following environment variable:
     ```env
     GEMINI_API_KEY=your_google_gemini_api_key
     ```

5. **Run the application**
   ```bash
   chainlit run main.py
   ```

## Code Overview

### `oauth_callback` Function
Handles GitHub OAuth authentication, returning the user object upon successful authentication.

### `handle_chat_start` Function
Initializes the user session and welcomes the user.

### `handle_message` Function
Processes user messages, maintains a session history, formats the input for Gemini, and returns AI-generated responses.

## Dependencies
- `chainlit`
- `google-generativeai`
- `python-dotenv`

## Notes
- Ensure you have a valid **Google Gemini API key**.
- Use **Python 3.8+** for compatibility.
- The session history is stored in `cl.user_session` to provide context-aware responses.

## Future Improvements
- Implement additional authentication methods.
- Enhance session management with persistent storage.
- Optimize response formatting for better interactions.

