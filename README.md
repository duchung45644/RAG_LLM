
# RAG LLM Chatbot

## Setup and Running the Application on Google Colab

1. **Open file [RAG_LLM_Chainlit.ipynb](https://github.com/duchung45644/RAG_LLM/blob/main/RAG_LLM_Chainlit.ipynb "RAG_LLM_Chainlit.ipynb") in Google Colab**.

2. **Get your ngrok authtoken**:
    - Go to [ngrok](https://dashboard.ngrok.com/get-started/your-authtoken) and sign up.
    - After logging in, you will find your authtoken on the dashboard.
    - Copy your authtoken.

3. **Add your ngrok authtoken** by running the following code block in a cell. Replace `<your_ngrok_authtoken>` with your actual ngrok authtoken:

    ```python
    !pip install pyngrok -q
    from pyngrok import ngrok

    !ngrok config add-authtoken <your_ngrok_authtoken>
    public_url = ngrok.connect(8000).public_url
    print(public_url)
    ```

4. **Run each cell in the notebook sequentially**.

5. **Run the Chainlit application** by running the following code block in a cell:

    ```bash
    !chainlit run app.py
    ```

6. **Access the application** using the public URL provided by ngrok. The URL will be printed in the output of the ngrok code block.

## Notes

- Replace `<your_ngrok_authtoken>` with your actual ngrok authtoken.
