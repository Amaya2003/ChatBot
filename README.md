Deploying the Chatbot on AWS Cloud
AWS Instance Setup:

I launched an AWS Linux or Ubuntu instance and performed the initial setup by updating the system and installing necessary packages with commands like sudo apt update and sudo apt install. I then cloned the project repository from GitHub to the instance and configured the environment by creating and editing a .env file to include the essential API keys for the application.

Running the Application:

I executed the chatbot application using Streamlit, which provided an interactive web interface for user interactions. The app processes PDF documents uploaded by users, extracting and analyzing text from these files. This text is divided into chunks and stored in a vector database, enabling efficient querying and retrieval.

Configuration and Security:

To ensure the chatbot was accessible from the web, I configured AWS security group rules to allow inbound traffic on port 8501, the default port for Streamlit applications. I adjusted the inbound rules in the AWS Management Console, setting up the necessary permissions to make sure the application was reachable from external networks.

Functionality:

Text Extraction: Users upload PDF files, and the chatbot extracts the text content from these documents.
Text Processing: The extracted text is split into manageable chunks and indexed using a vector store, facilitating quick and accurate search and retrieval.
Chat Interface: Users interact with the chatbot through a web-based interface provided by Streamlit. The chatbot answers questions based on the PDF content and handles general conversational queries.
Access:

After configuring the security settings, I accessed the Streamlit application via the public IP address of my AWS instance, appended with :8501 (e.g., http://<Instance_IP>:8501). This setup allows users to interact with the chatbot through a web browser, leveraging the AWS cloud resources for text extraction, indexing, and interactive responses based on the uploaded PDF content.
