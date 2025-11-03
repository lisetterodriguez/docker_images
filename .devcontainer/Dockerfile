FROM python:3.12

ARG PYTHON_ENV=my_env
ENV PYTHON_ENV=$PYTHON_ENV

WORKDIR /app

# Copy your requirements and setup script
COPY requirements.txt set_python_env.sh ./

RUN chmod +x set_python_env.sh

# Create the Python virtual environment and install deps
RUN ./set_python_env.sh $PYTHON_ENV

# Add venv to PATH so it's automatically active
ENV PATH="/opt/${PYTHON_ENV}/bin:$PATH"

WORKDIR /workspace
