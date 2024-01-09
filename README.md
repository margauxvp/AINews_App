# AI News App

This Streamlit-based app allows you to interact with OpenAI's GPT model for getting summaries of recent AI news. Ask any question about AI, and the model will provide you with a summary based on information from Azure Cognitive Search. The source of data that is used for this app is the following URL: https://techcrunch.com/category/artificial-intelligence/

https://github.com/margauxvp/OpenAIonURL_App/assets/33750077/1c472854-ec53-411c-909f-8d3d0b77d1ab

## Setup

1. **Create Azure AI Search Index**: This can be done very easily using oai.azure.com, where you use the UI to fill an index that supports hybrid search (full-text + vector) for your chosen URL data. It will execute data pre-processing (e.g. chunking) and the vectorization steps with indexation for you. For more information. Read: https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/use-your-data?tabs=url-web#ingesting-your-data. The full code repository can be found here: https://github.com/microsoft/sample-app-aoai-chatGPT/tree/main

   <img width="1168" alt="image" src="https://github.com/margauxvp/AINewsApp/assets/33750077/02fa4e01-6f43-45dd-922f-32838aabf036">

2. **Clone the Repository**: Clone this repository to your local environment.

    ```bash
    git clone https://github.com/your-username/ai-news-chat.git
    ```

3. **Create a Virtual Environment**: Create a virtual environment for the project and activate it.

    ```bash
    python -m venv venv
    ```
    
4. **Environment Variables**: Create a `.env` file in the project directory with your API keys.

    ```plaintext
    OPENAI_API_KEY=your_openai_api_key
    SEARCH_KEY=your_azure_search_key
    ```

5. **Azure OpenAI Configuration**: Customize the parameters in the code:

    ```python
    openai.api_base = "your_azure_openai_endpoint"
    deployment_id = "your_deployment_id"
    ```

6. **Azure AI Search Configuration**: Provide your Azure AI Search information:

    ```python
    search_endpoint = "your_search_endpoint"
    search_index_name = "your_search_index_name"
    ```

7. **BYOD (Bring Your Own Data)**: If using your own data, configure the `setup_byod` function by providing your deployment ID. This step allows you to use data sources when sending questions to OpenAI.

## Running the App

1. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

2. Run the Streamlit app:

    ```bash
    streamlit run your_script_name.py
    ```

    Replace `your_script_name.py` with your Python script containing the provided code.

3. Access the app in your web browser by opening the displayed URL.

## Usage

1. **Input**: Paste your AI news-related question in the text input.

2. **Ask Button**: Click "Ask about recent AI News" to interact with the GPT model.

3. **Result**: The GPT model's response will be displayed with a styled background.

<img width="560" alt="image" src="https://github.com/margauxvp/OpenAIonURL_App/assets/33750077/53f31a05-9a46-4300-a3fc-3cbaaa3c0f41">

Feel free to explore and chat about the exciting world of AI news! 🤖

