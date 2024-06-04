# ChatX

ChatX is a versatile chat server project designed for easy setup and deployment, facilitating real-time communication with file sharing capabilities. By leveraging the power of Python and Ngrok, ChatX offers a seamless experience for both local and remote users. This project is ideal for developers, hobbyists, and small teams looking to implement a customizable chat solution.

## Features

* **Real-Time Messaging**: Supports real-time chat between multiple clients.
* **File Sharing**: Users can easily upload and share files within the chat.
* **Easy Setup**: Automated setup using shell scripts, with minimal configuration required.
* **Secure Connections**: Utilizes Ngrok for secure, tunnelled connections over the internet.
* **Portable**: Install and run the server from anywhere using the `chatX` command.

## Installation


1. Clone the repository:

   ```sh
   git clone https://github.com/yourusername/chatX.git
   cd chatX
   ```
2. Install dependencies:

   ```sh
   pip install -r requirements.txt
   ```
3. Run the setup script to create the `chatX` command:

   ```sh
   bash run.sh
   ```

## Setting Up Ngrok API Key

To use Ngrok with ChatX, you need to set up your Ngrok API key.


1. Sign up for an account on [Ngrok](https://ngrok.com/).
2. Once logged in, navigate to the [API Keys section](https://dashboard.ngrok.com/get-started/your-authtoken) in the Ngrok dashboard.
3. Copy your API key.
4. When prompted during the setup, enter your Ngrok API key. Alternatively, you can manually create a `credentials.json` file in the project directory with the following content:

   ```json
   {
       "api_key": "your_ngrok_api_key"
   }
   ```
5. The setup scripts will handle the rest, including generating and storing the authentication token.

## Usage


1. Start the chat server by running:

   ```sh
   chatX
   ```
2. The server setup is automated. Upon successful startup, the connection details will be provided in a `command.txt` file. Share the connection command with users to allow them to connect via Telnet.

## Files and Directories

* `chat_server.py`: Main server script handling client connections, messaging, and file uploads.
* `ngrok_setup.py`: Script to set up and manage Ngrok tunnels.
* `credchecker.py`: Utility to check and fix JSON formatting issues in credentials files.
* `auth.py`: Script for managing Ngrok API keys and authentication tokens.
* `bash_server.sh`: Shell script to automate server setup, start, and shutdown processes.
* `run.sh`: Shell script to create the `chatX` command for easy server start.
* `requirements.txt`: List of Python dependencies.

## Future Visions

* **Encryption**: Implement end-to-end encryption to ensure all messages and files are securely transmitted.
* **Enhanced File Handling**: Improve file inclusion and handling to make it more seamless and intuitive for users.
* **Rich Media Support**: Add support for sending and receiving rich media like images, videos, and audio files.
* **User Authentication**: Integrate user authentication to manage and secure user access.
* **Chat History**: Store and retrieve chat history so users can access previous conversations.
* **Improved Error Handling**: Enhance error handling to provide better feedback and recovery options for users.
* **Scalability**: Optimize the server to handle a larger number of concurrent users and larger file transfers.
* **Web Interface**: Develop a web-based interface for users who prefer not to use a Telnet client.

## Contributing

Contributions are welcome! Feel free to submit issues, feature requests, or pull requests to improve ChatX.

## License

This project is licensed under the MIT License.

## Additional Notes

* Ensure you have Python and Ngrok installed on your system.
* The `credentials.json` file is used to store your Ngrok API key and auth token. This file is automatically generated and managed by the scripts.
* To connect to the server, users will need to use a Telnet client and the connection command provided in `command.txt`.

With ChatX, creating a private chat server has never been easier. Join us in building a robust and user-friendly chat platform!