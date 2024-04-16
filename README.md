# Lexicon AI

# Built for [GreenLexicon](https://github.com/GunaPalanivel/GreenLexicon.git)

Experience the simplicity of Lexicon AI, a minimalistic web interface designed to enhance your communication needs.

Explore the live version here: [Lexicon AI](https://lexicon-ai-umber.vercel.app/)

#### Deploy with Docker

To deploy using Docker, utilize the following command:

```bash
docker run --name geminiprochat \
--restart always \
-p 3000:3000 \
-itd \
-e GEMINI_API_KEY=your_api_key_here \
babaohuang/geminiprochat:latest
```

Ensure your GEMINI API key replaces `your_api_key_here`.

This command initiates the _geminiprochat_ service, available at http://localhost:3000.

## Configuring Environment Variables

Configure the operation of Lexicon AI through the following environment variables:

| Name              | Description                                                                                                                    | Required |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------ | -------- |
| GEMINI_API_KEY    | API Key for GEMINI services. Obtainable [here](https://makersuite.google.com/app/apikey).                                      | _✔_      |

## Local Development Setup

### Prerequisites

1. **Node.js**: Ensure Node.js v18 or higher is installed. Use [nvm](https://github.com/nvm-sh/nvm) for managing versions.

   ```bash
   node -v
   ```

2. **PNPM**: Use [PNPM](https://pnpm.io/) for efficient dependency management. Install it globally if not already installed:

   ```bash
   npm install -g pnpm
   ```

3. **GEMINI_API_KEY**: Obtain your API key from [Google API Console](https://makersuite.google.com/app/apikey).

### Getting Started

1. Install dependencies:

   ```bash
   pnpm install
   ```

2. Prepare your environment file. Start by copying `.env.example` to `.env` and populate it with your GEMINI API Key:

   ```bash
   cp .env.example .env
   echo "GEMINI_API_KEY=your_api_key" >> .env
   ```

3. Run the application locally. By default, it will be accessible at http://localhost:3000:

   ```bash
   pnpm run dev
   ```

## How to Contribute

Contributions are welcome! If you would like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/new-feature`.
3. Make your changes and commit them: `git commit -m 'Add new feature'`.
4. Push to the branch: `git push origin feature/new-feature`.
5. Submit a pull request.

## License

This project is licensed under the MIT License.
