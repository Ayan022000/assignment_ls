###Assigment :Implementing Simplified MLops for a Machine Learning Project

---> Objective: The objective of this assignment is to set up a simplified MLops pipeline for a basic machine learning project using essential tools. You will demonstrate your ability to version control,automate testing, and deploy a model.

---> step 1 : Version Control
        Initialized the repository with a README file.
        Made an simple machine learning code and pushed it to this repository.

---> Step 2 : Dockerfile for My Application


This Dockerfile is used to create a Docker image for running "My Application." The Docker image is based on the official Python 3.8 image and sets up the necessary environment for running the application.

Usage
To build the Docker image, navigate to the directory containing this Dockerfile and run the following command:

bash
Copy code
docker build -t my-application-image .
After building the image, you can run a container based on the image using the following command:

bash
Copy code
docker run -p 5000:5000 my-application-image
Directory Structure
The Dockerfile is placed in the root directory of your application.
Building the Image
The Docker image is built by executing the following steps within the container:

Copies all files from the current directory into the /app directory in the container.
Sets the working directory to /app.
Installs the Python dependencies specified in requirements.txt using pip.
Running the Application
The Docker image is configured to run the application using the following command:

bash
Copy code
CMD python app.py
This command starts your Python application, and you can access it through the exposed port (in this case, port 5000) as specified when running the container.

Also pushed the Docker Image to DockerHUB . you can pull the iamge with this link : docker pull ayan0209/assignment_ls:latest


---> Step 5: Monitoring and Logging(In NOtebook )

MLflow Integration
In this project, we have integrated MLflow, an open-source platform to manage the end-to-end machine learning lifecycle. MLflow provides tracking capabilities for metrics and parameters, artifact logging, and model management.

Metric Tracking
We utilize MLflow to monitor and track key metrics during the training and evaluation of machine learning models. The following metrics are tracked:

R2 Score (R-squared): A metric that measures the goodness of fit of a regression model. It indicates how well the model's predictions match the actual data. Higher R2 scores indicate a better fit.

Mean Squared Error (MSE): A metric that quantifies the average squared difference between the actual and predicted values. Lower MSE values represent more accurate predictions.

Mean Absolute Error (MAE): A metric that calculates the average absolute difference between the actual and predicted values. It provides a measure of prediction accuracy.

Model Tracking
We also use MLflow to log and manage trained machine learning models. This includes:

Logging the Model: The final trained model, including all its parameters and configurations, is logged using MLflow. This allows for easy model versioning and retrieval.
Accessing MLflow UI
You can access the MLflow user interface to explore tracked runs, metrics, and models. To view the MLflow UI, follow these steps:

Ensure you have MLflow installed or create a virtual environment with MLflow installed:

bash
Copy code
pip install mlflow
Start the MLflow server by running the following command in the project directory:

bash
Copy code
mlflow server
Open a web browser and navigate to http://localhost:5000 to access the MLflow UI.

Exploring Metrics and Models
In the MLflow UI, you can explore the tracked runs, compare metrics across runs, and view the logged models. This provides valuable insights into model performance and allows you to select the best model for deployment.

 
