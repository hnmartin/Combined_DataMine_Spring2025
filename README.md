# PHYS_324 Spring Semester Course

Welcome to the PHYS_324 course for the spring semester. This repository contains notebooks that helps undergraduate students of PHYS_324 to learn about data from CMS open source and use different techniques to analyse them. These notebooks will help you understand and explore the course material effectively.

# Connecting to Jupyter Lab/Notebook 
For this course, we will be using Jupyter Notebook, which is useful for creating and sharing documents containing code and narrative text. There are two primary ways to access Jupyter Notebook: through the terminal and through Purdue JupyterHub. Before using either method, you need to have scholar access. Please contact the TA for this access.

# Connecting through Jupyterhub
1. Obtain Scholar Access: Ensure you have scholar access by contacting the course TA.
2. Access JupyterHub:
    - Open your web browser and go to: https://gateway.scholar.rcac.purdue.edu/
    - Log in using your BoilerKey username and password. In the password field, enter your BoilerKey password followed by ```,push``` and confirm the login with Duo Mobile.
   
F.Y.I. You can also access terminal from here which will be seperate from the terminal in your local machine.

# Connecting through terminal
1. On your local machine, open the terminal.
2. Use the following command to connect to the Scholar server:
```
ssh <user_name>@scholar.rcac.purdue.edu -L <port_number>:localhost:<port_number>
```
 - Replace <user_name> with your Purdue username.
 - Replace <port_number> with your chosen port number (default is 8888, but you can use any number above 8000 if 8888 is occupied).
Example (assuming the username is bhanda25):
```
ssh bhanda25@scholar.rcac.purdue.edu -L 8868:localhost:8868
```
Enter your BoilerKey password followed by ```,push``` and confirm with Duo Mobile.

After logging in

```
module load anaconda
```
```
jupyter lab --port 8868
```
Copy the provided URL into your web browser to access Jupyter Lab. It's the best to practice to connect to a remote server via ssh-keys: https://www.rcac.purdue.edu/knowledge/scholar/accounts/login/sshkeys.


# Set up Conda Environment 
For the purpose of this course, we need to be able to access root files. Therefore, installing ROOT is important. However, it is very difficult to install ROOT locally. Instead, we
create Conda Environment and install ROOT within it along with all the packages that are needed for this course.

I have already created Conda Environment for your use, all it remains is to link this environment with your notebook: 

You can access to your scholar terminal either from your local machine or through jupyterlab, Once you are logged in: 

Load anaconda module,

```
module load anaconda

``` 
Load a common kernel from the common area, for example, my kernel: 
```
source activate /depot/cms/conda_envs/bhanda25/Coffea-Santosh
``` 
then register this kernel to jupyter: 
```
python -m ipykernel install --user --name=Coffea-Santosh

``` 
Refresh your notebook then you will see this new kernel with customized conda packages 

# Clone this repository to have access to the github
Once the environment is set up, you are ready to clone the github repository. Please go to your local lapop's terminal and do the following:
```
git clone https://github.com/hnmartin/Combined_DataMine_Spring2025.git

```
If you want to clone the Github repository onto the Purdue gateway rcac JupyterLab, open a JuypterLab terminal and type 

```
cd ~/
```
If you then check your directory files in this folder

```
dir
```
you should see the same files and folders as those that show on the left side of the window. Then, you can clone the github
```
git clone https://github.com/hnmartin/Combined_DataMine_Spring2025.git

```
Each week, a new folder will be added to this GitHub repository. To get the latest changes from GitHub, follow these steps:

1. **Navigate to your local repository**: Open your terminal and change to the directory where your repository is cloned:
   ```bash
   cd /path/to/your/repository
   
Pull the latest changes: Run the following command to fetch the latest updates from GitHub:
```
   git pull
```

Now you are all set for your journey of data analysis !! Good Luck
