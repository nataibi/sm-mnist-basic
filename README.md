# LAB1: Overview Of SageMaker Studio
 ![alt text](imgs/w.png)
# learning outcome from this lab
- Navigate Sagemaker studio and familiarise yourself with all the necessary functionalities for completing today's labs
- Making a Binary Prediction of Whether a Handwritten Digit is a 0

## 0. Creating a Sagemaker Studio instance
- In the console, go to the search bar at the top and type Sagemaker
- Click on Amazon SageMaker.
- Under **Get Started**, click on Sagemaker Studio
- Under **User Profile** , type your name in the **Name** field
- Under **Default Execution Role**, click on **Create a new role**
- A **Create an IAM Role** window pops up, change to **Any S3 bucket**, leave the rest as default and click **Create Role**
- Save and create the studio, this step will take few mins, notice the **Pending** status
- Once the sutudio is ready, under **Launch App** dropdown box, choose **Studio**
- The studio will take 2-4 mins to launch 
- 
## 1. Amazon SageMaker Studio UI Overview
- Take 5 mins to read what each UI section means: [here](https://docs.aws.amazon.com/sagemaker/latest/dg/studio-ui.html#studio-ui-browser ) 
- Explore the Left sidebar
- File and resource browser
- Main work area
- Settings


## 2. Simple Tasks to carry out
### 2.1 Upload a file
- Create a plain text file with your name on it and title it **"your_name.txt"**, store it on your desktop, content of the file should just be your email address.
- Upload the file **"your_name.txt"** from your Desktop by:
- - On the left sidebar, choose the File Browser icon ( ![alt text](imgs/3001.png) ).
- - On the file browser, choose the Upload Files icon ( ![alt text](imgs/3002.png) ).
- - Select the **"your_name.txt"** and then choose Open.
- You should now have this directory structure (name will be different) (after completing pre-req step 0)
 ![alt text](imgs/3004.png)
- Double-click a file to open the file in a new tab in Studio.
### 2.2 Clone a git repository
- On the left sidebar, choose the File Browser icon ( ![alt text](imgs/3001.png) ).
- Make sure your file **"your_name.txt"** is visible
- On the left sidebar, choose the Git icon ( ![alt text](imgs/3003.png) ).
- Choose Clone a Repository.
- Enter the URI for the SageMaker examples repo https://github.com/nataibi/sm-mnist-basic.git
- Choose CLONE.
- Wait for the download to finish. After the repo has been cloned, the File Browser opens to display the cloned repo.
- Double click the repo to open it.
- Choose the Git icon on the left side bar to view the Git user interface which now tracks the changes for the repo.

## 3. Launch the MNIST example 
- From the pre-req step (0) and step 2.2 you should now see two directories on the left sidebar
 ![alt text](imgs/4001.0.png )
-  click on the **sm-mnist-basic** directory, and click on the **linear_learner_mnist.ipynb**, the notebook will launch in the main work area
![alt text](imgs/4001.1.png )
- You will now be prompted to select a kernel, choose **Python 3 (SageMaker JumpStart Data Science 1.0) **
![alt text](imgs/4001.png )
- The kernel will take couple of minutes to initialise
- Read the introduction to linear learner example
- TIPs on running notebook cells
 - - You can either use the tool bar "Play button" ![alt text](imgs/4001.2.png )
 - - Or use the keyboard shortcut SHIFT+ENTER
- Set permission and correct role
![alt text](imgs/4002.png )
- Data ingestion phase, the dataset is already available in this report, as follows:
 ![alt text](imgs/4004.png )
- Inspect the dataset
 ![alt text](imgs/4005.png )
- Converting the dataset 
 ![alt text](imgs/4006.png )
- Upload the training
  ![alt text](imgs/4008.png )
- Now we can start training the linear model. we start by specifying the container we'll be using.
- Then we kick off the base estimator. This step will take 6-8 mins, observe the outputs as it progresses.
 ![alt text](imgs/4009.png )
- Now you're model is read, we need to host it somewhere
 ![alt text](imgs/4010.png )
- Let's validate the model by predicting a single record
- First we need to set some request parameter
![alt text](imgs/4011.png )
- Now let's send a prediction
![alt text](imgs/4012.png )
- Now that we verified this works, let's try and send an entire batch, observe the results
![alt text](imgs/4013.png )
- Cleanup and Delete the endpoint
![alt text](imgs/4014.png )

