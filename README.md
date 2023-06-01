**Data Transformation Application**

This Python application performs data transformation and cleansing operations on a CSV file, calculates totals for grid_purchase and grid_feedin by hour and writes the transformed data to an output file.

**Folder Structure**

README : Please read through this file to be able to run the date transformation application
dockerfile : This text file is used to build the docker image
measurments.csv: Input dataset provided to work on.
output.csv: The transformed data with the added boolean column
python_application.py: The python code of carrying on the required cleansing and transformation
requirements.txt: Dependincies and packages used in python app and used by docker to build the docker image
Documentation.pdf: Application documentation and output screenshots

**Prerequisites**

Python 3.9 or higher installed on your local machine.
Required Python packages: pandas, pandasql.
Docker installation on the local machine

**Getting Started**

Clone the repository or download the application code locally.

You can run the python application directly from the terminal or using Docker.

**Python**

Open the terminal and navigate to the cloned folder
Install the required Python packages using pip:
 > pip install pandas pandasql

Run the application:
 > python python_application.py

**Dockerization**

To run the application within a Docker container, follow these steps:

In the terminal or command prompt, navigate to the project directory containing the Dockerfile.
Build the Docker image using the following command
 > docker build -t data-transformation-app .

After the Docker image is successfully built, run the following command to start a container from the Docker image:
 > docker run --name data-trans-cont data-transformation-app

After the container finishes running, access the output file output.csv by copying it from the container to your local machine:
 > docker cp data-trans-cont:/app/output.csv ./output.csv
