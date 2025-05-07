## Instagram-AI-Agent 🌸

Instagram-AI-Agent is an AI-powered automation tool designed for **Instagram** to automate social media interactions such as posting, liking, and commenting. It leverages advanced AI models to generate engaging content, automate interactions, and manage Instagram accounts efficiently.

Before using the automation features, you can personalize the agent by training with the following, including:
https://www.instagram.com/dreamlandofficial_1?igsh=NTZvcHRkNjlhYzhp
- **YouTube Video URL** 🎥
- **Audio File** 🎙️
- **Portfolio or Website Link** 🌐
- **File Formats Supported**: PDF, DOC, DOCX, TXT 📄

## Features

- **Instagram Automation**: Automatically log in, post photos, like posts, and leave thoughtful comments.
- **AI-Powered Content Generation**: Use Google Generative AI to create engaging captions and comments.
- **Proxy Support**: Use proxies to manage multiple accounts and avoid rate limits.
- **Cookie Management**: Save and load cookies to maintain sessions across restarts.

**Upcoming Features:**

- **Twitter Automation**: (Coming soon) Automatically tweet, retweet, and like tweets.
- **GitHub Automation**: (Coming soon) Automatically manage repositories, issues, and pull requests.

## Installation

1. **Clone the repository**:

   ```sh
   git clone https://github.com/david-patrick-chuks/Instagram-AI-Agent.git
   cd Instagram-AI-Agent
   ```

2. **Install dependencies**:

   ```sh
   npm install
   ```

3. **Set up environment variables**:
   Rename the [.env.example](http://_vscodecontentref_/1) file to [.env](http://_vscodecontentref_/1) in the root directory and add your Instagram credentials. Refer to the [.env.example](http://_vscodecontentref_/2) file for the required variables.
   ```dotenv # Instagram credentials
   IGusername=your_instagram_username
   IGpassword=your_instagram_password 
   
   Xusername= #Twitter username
   Xpassword= #Twitter password

   MONGODB_URI= #MongoDB URI
   ```

## MongoDB Setup (Using Docker)

1. **Install Docker**:
   If you don't have Docker installed, download and install it from the [official website](https://www.docker.com/products/docker-desktop/)
2. **Run MongoDB using Docker Container**:

    **Option 1:**
      ```sh
      docker run -d -p 27017:27017 --name instagram-ai-mongodb mongodb/mongodb-community-server:latest
      ```
    **Option 2:**
      ```sh
      docker run -d -p 27017:27017 --name instagram-ai-mongodb -v mongodb_data:/data/db mongodb/mongodb-community-server:latest
      ```   
      (Option 2: use this if you want to have like a permanent storage in you so your data won't be lost or remove if you stop or remove your Docker container)
3. **Modify the MONGODB_URI in the .env file**:
   ```dotenv
   MONGODB_URI=mongodb://localhost:27017/instagram-ai-agent
   ```
4. **Verify the connection**:
   Open a new terminal and run the following command:
   ```sh
   docker ps
   ```
   You should see the MongoDB container running.

   Docker Commands (Additional Info):
   - To stop the MongoDB container:
     ```sh
     docker stop instagram-ai-mongodb
     ```
   - To start the MongoDB container:
       ```sh
       docker start instagram-ai-mongodb
       ```
   - To remove the MongoDB container:
      ```sh
      docker rm instagram-ai-mongodb
      ```
   - To remove the MongoDB container and its data:
      ```sh
      docker rm -v instagram-ai-mongodb
      ```

## Usage

1. **Run the Instagram agent**:
   ```sh
   npm start
   ```

**Upcoming Features:**

- **Run the Twitter agent** (Coming soon):

  ```sh
  npm run start:twitter
  ```

- **Run the GitHub agent** (Coming soon):
  ```sh
  npm run start:github
  ```

## Project Structure

- **src/client**: Contains the main logic for interacting with social media platforms like Instagram.
- **src/config**: Configuration files, including the logger setup.
- **src/utils**: Utility functions for handling errors, cookies, data saving, etc.
- **src/Agent**: Contains the AI agent logic and training scripts.
- **src/Agent/training**: Training scripts for the AI agent.
- **src/schema**: Schema definitions for AI-generated content and database models.
- **src/test**: Contains test data and scripts, such as example tweets.

## Logging

The project uses a custom logger to log information, warnings, and errors. Logs are saved in the [logs](http://_vscodecontentref_/3) directory.

## Error Handling

Process-level error handlers are set up to catch unhandled promise rejections, uncaught exceptions, and process warnings. Errors are logged using the custom logger.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgements

- [Google Generative AI](https://ai.google/tools/) for providing the AI models.
- [Puppeteer](https://github.com/puppeteer/puppeteer) for browser automation.
- [puppeteer-extra](https://github.com/berstend/puppeteer-extra) for additional plugins and enhancements.
