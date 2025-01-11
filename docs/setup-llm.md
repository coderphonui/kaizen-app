# LLM setting

Prepare an environment file (.env) at the same location of the docker-compose.yml file. You can copy the file .env_example and rename it to .env file/
Then, replace the correct values for the LLM section

```shell
GEMINI_PROJECT_ID=<gemini-project-id>
GEMINI_LOCATION=<gemini-lication>
GOOGLE_APPLICATION_CREDENTIALS=/app/user-data/google-credentials.json
OPENAI_API_KEY=<openai-api-key>
GROQ_API_KEY=<groq-api-key>
ANTHROPIC_API_KEY=<anthropic-api-key>
OLLAMA_BASE_URL=http://host.docker.internal:11434

```

# Special notes for Google LLM integration

To have the GOOGLE_APPLICATION_CREDENTIALS, you need to create a service account in Google. 
You must grant the service account the role: Vertex AI Service Agent so it can use Vertex AI API.

Then setup the API key -> download the json file. Then, change the file name to google-credentials.json and put it under the user-data folder.
