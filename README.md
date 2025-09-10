# AI Model Comparison Website

A modern web application that allows users to compare responses from multiple AI models simultaneously using OpenRouter API.

## Features

- **Multi-Model Comparison**: Compare responses from GPT-5, Claude 4 Sonnet, Gemini 2.5, and DeepSeek
- **Real-time Responses**: All selected models respond simultaneously
- **Best Response Selection**: Mark and copy the best response from any model
- **Universal Message Box**: Send the same message to all selected models at once
- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Secure API Key Management**: API keys stored locally in browser

## Supported Models

- **GPT-5** (OpenAI) - Latest GPT model with advanced reasoning capabilities
- **Claude 4 Sonnet** (Anthropic) - Advanced reasoning and analysis capabilities
- **Gemini 2.5** (Google) - Fast and efficient reasoning model
- **DeepSeek** (DeepSeek) - Specialized in coding and technical tasks

## Prerequisites

- Node.js (version 16 or higher)
- npm or yarn
- OpenRouter API key (get one from [https://openrouter.ai/keys](https://openrouter.ai/keys))

## Installation

1. **Clone or download the project**
   ```bash
   cd ai-model-comparison
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   ```

4. **Open your browser**
   Navigate to `http://localhost:3000`

## Setup Instructions

1. **Get an OpenRouter API Key**
   - Visit [https://openrouter.ai/keys](https://openrouter.ai/keys)
   - Sign up for an account
   - Generate a new API key

2. **Configure the API Key**
   - When you first open the application, you'll be prompted to enter your API key
   - Enter your OpenRouter API key in the input field
   - Click "Save Key" to store it locally

3. **Select Models**
   - Choose which AI models you want to compare
   - You can select multiple models at once

4. **Start Comparing**
   - Type your message in the universal message box
   - Press Enter or click "Send to All Models"
   - View responses from all selected models simultaneously

## Usage

### Basic Workflow

1. **Configure API Key**: Enter your OpenRouter API key when prompted
2. **Select Models**: Choose which AI models to compare (1-4 models)
3. **Send Message**: Type your message and send it to all selected models
4. **Compare Responses**: View all responses side by side
5. **Pick Best**: Click the star icon to mark the best response
6. **Copy Response**: Use the copy button to copy any response to clipboard

### Features

- **Model Selection**: Click on model cards to select/deselect them
- **Universal Input**: One message box sends to all selected models
- **Real-time Loading**: See loading indicators while models generate responses
- **Error Handling**: Clear error messages if any model fails
- **Token Usage**: View token usage statistics for each response
- **Best Response**: Mark and easily copy the best response

## Project Structure

```
ai-model-comparison/
├── src/
│   ├── components/
│   │   ├── ApiKeyInput.jsx      # API key configuration
│   │   ├── ModelSelector.jsx    # Model selection interface
│   │   ├── MessageInput.jsx     # Universal message input
│   │   └── ModelResponse.jsx    # Individual model response display
│   ├── utils/
│   │   └── openrouter.js        # OpenRouter API integration
│   ├── App.jsx                  # Main application component
│   ├── main.jsx                 # React entry point
│   └── index.css                # Global styles
├── package.json                 # Dependencies and scripts
├── vite.config.js              # Vite configuration
├── tailwind.config.js          # Tailwind CSS configuration
└── README.md                   # This file
```

## Technologies Used

- **React 18** - Modern React with hooks
- **Vite** - Fast build tool and dev server
- **Tailwind CSS** - Utility-first CSS framework
- **Axios** - HTTP client for API calls
- **Lucide React** - Beautiful icons
- **OpenRouter API** - Unified access to multiple AI models

## API Configuration

The application uses OpenRouter API to access multiple AI models through a single endpoint. The API configuration includes:

- **Base URL**: `https://openrouter.ai/api/v1/chat/completions`
- **Authentication**: Bearer token (API key)
- **Headers**: Required headers for OpenRouter compliance
- **Models**: Pre-configured model IDs for each AI provider

## Security

- API keys are stored locally in browser localStorage
- No API keys are sent to our servers
- All API calls are made directly to OpenRouter
- HTTPS is used for all API communications

## Customization

### Adding New Models

To add new models, edit `src/utils/openrouter.js`:

```javascript
export const AVAILABLE_MODELS = {
  'new-model': {
    id: 'provider/model-id',
    name: 'Model Name',
    provider: 'Provider Name',
    description: 'Model description',
    color: 'bg-color-class'
  },
  // ... existing models
};
```

### Styling

The application uses Tailwind CSS for styling. You can customize:

- Colors in `tailwind.config.js`
- Component styles in `src/index.css`
- Individual component styling in their respective files

## Troubleshooting

### Common Issues

1. **API Key Not Working**
   - Ensure you have a valid OpenRouter API key
   - Check that you have sufficient credits in your OpenRouter account
   - Verify the API key is correctly entered

2. **Models Not Responding**
   - Check your internet connection
   - Verify the model IDs are correct in the configuration
   - Check OpenRouter status page for any service issues

3. **Build Errors**
   - Ensure Node.js version is 16 or higher
   - Delete `node_modules` and run `npm install` again
   - Check for any missing dependencies

## Contributing

Feel free to contribute to this project by:

1. Forking the repository
2. Creating a feature branch
3. Making your changes
4. Submitting a pull request

## License

This project is open source and available under the MIT License.

## Support

For issues or questions:

1. Check the troubleshooting section above
2. Review OpenRouter documentation
3. Open an issue on the project repository

---

**Note**: This application requires an OpenRouter API key to function. Make sure to get your API key from [https://openrouter.ai/keys](https://openrouter.ai/keys) before using the application.
