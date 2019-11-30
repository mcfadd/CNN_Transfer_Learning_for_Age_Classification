# Colab Setup

This project requires the use of a GPU to process images.
If you don't have a GPU available you can still run the notebook by using Colab, which is free!

Reference: https://course.fast.ai/start_colab.html#step-2-configuring-your-notebook-instance

### Step 1: Accessing Colab

1. First of all you should sign in to you Google account if you are not signed in by default. You must do this step before opening Colab, otherwise the notebooks will not work. You can sign in [here](https://accounts.google.com/signin/v2/identifier?hl=en-gb&flowName=GlifWebSignIn&flowEntry=ServiceLogin).

2. Next, head on to the [Colab Welcome Page](https://colab.research.google.com/notebooks/welcome.ipynb#recent=true) and click on ‘Github’. In the ‘Enter a GitHub URL or search by organization or user’ line enter ‘https://github.com/mcfadd/CNN_Transfer_Learning_for_Age_Classification’. Click on the jupyter notebook listed. 

3. You should see your notebook displayed now. Before running anything, you need to tell Colab that you are interested in using a GPU. You can do this by clicking on the ‘Runtime’ tab and selecting ‘Change runtime type’. A pop-up window will open up with a drop-down menu. Select ‘GPU’ from the menu and click ‘Save’.

### Step 2: Configuring your notebook instance

1. Before you start using your notebook, you need to install the necessary packages. You can do this by creating a code cell, and running:
   
    ```jupyter
    !curl -s https://raw.githubusercontent.com/mcfadd/CNN_Transfer_Learning_for_Age_Classification/master/colab_setup.bash | bash    
    ```
   
2. When you run the first cell, you will face a pop-up saying ‘Warning: This notebook was not authored by Google’; you should leave the default tick in the ‘Reset all runtimes before running’ check box and click on ‘Run Anyway’.

3. On the new window click ‘Yes’ to reset all runtimes. You should be able to run the project now. 

### Step 3: Saving your notebook

If you opened a notebook from Github, you will need to save your work to Google Drive. You can do this by clicking on ‘File’ > ‘Save’ > ’Save a Copy in Drive’.

This will open up a new tab with the same file, only this time located in your Drive. If you want to continue working after saving, use the file in the new tab. Your notebook will be saved in a folder called Colab Notebooks in your Google Drive by default.

### Step 4: Saving your data files

If you run a script which creates/ downloads files, the files will NOT persist after the allocated instance is shutdown. To save files, you need to permit your Colaboratory instance to read and write files to your Google Drive. Run the cell with the following contents to save your data set to Google Drive.
   ```python3
    from google.colab import drive
    drive.mount('/content/gdrive', force_remount=True)
    root_dir = "/content/gdrive/My Drive/"
    data_path = root_dir + 'data/faces_data_set'
    model_path = root_dir + 'models'
   ```
