# Use Jupyter's base image with Python and Jupyter pre-installed
FROM jupyter/base-notebook:latest

# Set working directory inside the container
WORKDIR /home/jovyan/work

# Copy your notebook and .env file into the container (adjust the file names as needed)
COPY Page_Rank_NoNLPmodel_Docker_Checkpoints.ipynb ./
COPY .env .env

# Install required Python packages
RUN pip install --no-cache-dir numpy pandas matplotlib unidecode beautifulsoup4 requests

# Expose the Jupyter Notebook port
EXPOSE 8888

# Start Jupyter Notebook (without token for easy remote access — set one for security!)
CMD ["start-notebook.sh", "--NotebookApp.token=''", "--NotebookApp.password=''", "--NotebookApp.allow_origin='*'", "--NotebookApp.ip='0.0.0.0'", "--NotebookApp.open_browser=False"]
