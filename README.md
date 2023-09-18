# These are the steps needed to successfully deploy a flask app using the Microsoft Azure Web App Services

## Step 1: Creating a good workspace
In Google Shell, create a workspace that contains a folder that contains the following:  A folder labeled templates. This is where you will store the various html files for your flask application.  A python file named app.py, this will be the code neeed to run the flas application.  A README.md file that will explain the code involed in this project. A requirements.txt file that included the necessary packages for the app.py to work properly. In this specific instance, flask, faker, and pandas are needed. 

## Step 2: Linking with Azure
In the google shell, you have to download the Azure Command Line Interface to interact with the Azure Cloud Service. This can be done by using the command "curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash"

## Step 3: Log-in with Azure Account
After installed, you can login with your Azure Account using the command, az login --use-device-code.
This will prompt you to click a hyperlink and enter a code that will link your azure account to your google cloud session

## Step 4: Change subscription ID
After you are logged in, you have to change your subscription ID to the subscription linked to your stony brook account.
You can find the azure student subscription ID with the following command: 'az account list --output table'.
You can set the subscription ID with the following command: 'az account set --subscription'.

## Step 5: Creating a resource group 
Now that the Google shell session and the azure cloud service are linked, you can log into the azure web portal and create a new resource group.
This can be done on the homepage under the azure services.

## Step 6: Deployment
The final step to deploy your flask application is to enter the following command into the terminal of your google shell session. 

"az webapp up --resource-group 'groupname'> --name 'app-name' --runtime PYTHON:3.9 --sku B1". 
The values encased in the ' ' must be replaced with the information for your application. 

## After completion, you can view the status of the application and view a preview of it under the overview tab of the application inside azure. 
