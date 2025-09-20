# Base Image with Jupyter Notebook
FROM jupyter/scipy-notebook:latest


# Set working directory
WORKDIR /home/jovyan/work


# Install system dependencies
USER root
RUN apt-get update && apt-get install -y git curl wget unzip build-essential libssl-dev libffi-dev && rm -rf /var/lib/apt/lists/*


# Install AWS CLI v2
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && unzip awscliv2.zip && ./aws/install && rm -rf awscliv2.zip ./aws


# Install Azure CLI
RUN curl -sL https://aka.ms/InstallAzureCLIDeb | bash


# Install VS Code server (for remote dev)
RUN curl -fsSL https://code-server.dev/install.sh | sh


# Switch back to non-root user (Jupyter default user)
USER ${NB_UID}


# Copy requirements and install Python dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt


# Expose ports
EXPOSE 8888 8080 9000

