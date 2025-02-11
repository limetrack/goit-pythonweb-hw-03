## Overview

This application is a simple Python web app that includes routing for:

A home page (index.html)

A message submission page (message.html)

A read page (read.html), which displays saved messages

The app can be run locally without Docker or within a Docker container.


## Running the App with Docker

### Build the Docker Image:

```docker build -t fullstack-web-app .```

### Run the Docker Container:

```docker run -d -p 3000:3000 -v $(pwd)/storage:/app/storage fullstack-web-app```

-p 3000:3000 maps port 3000 in the container to port 3000 on your host machine.

-v $(pwd)/storage:/app/storage ensures that the data.json file persists outside the container.


### Running the App Without Docker

Set Up a Virtual Environment (Optional):

```python -m venv venv```

Activate the Virtual Environment:

On Linux/macOS:

```source venv/bin/activate```

On Windows:

```venv\Scripts\activate```

Install Required Dependencies:

```pip install -r requirements.txt```

Run the Application:

```python main.py```


### Access the App:

Home Page: http://localhost:3000
<img width="1439" alt="Screenshot 2024-12-22 at 20 09 29" src="https://github.com/user-attachments/assets/77284f75-ffc4-43f2-bcf3-54a5c5dd748c" />

Message Page: http://localhost:3000/message
<img width="1440" alt="Screenshot 2024-12-22 at 20 09 45" src="https://github.com/user-attachments/assets/98ef6174-7ef0-47c8-a675-3722edccccf7" />

Read Page: http://localhost:3000/read
<img width="1439" alt="Screenshot 2024-12-22 at 20 10 05" src="https://github.com/user-attachments/assets/d0097fa8-8f8a-4c7e-99a5-260bbe7ce291" />


