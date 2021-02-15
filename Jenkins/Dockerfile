# base image 
FROM alpine

# Install python and pip 
RUN apk add --update python3 

# Base workspace 
WORKDIR /usr/src/app/

# Install python modules 
COPY requirements.txt .
RUN pip3 install --no-cache-dir -r ./requirements.txt 

# Copy other files 
COPY app.py .
COPY templates/index.html ./templates/

# Expose port 
EXPOSE 5000

# Run the application 
CMD ["python3", "/usr/src/app/app.py"]