**Things to edit in Google Colab:**

1. ngrok token

2. password

3. Github User

4. Github email

</br>

**Steps to setup Local VSCode on Remote GCE:**

</br>

Create an ngrok token from https://ngrok.com/

Open the Notebook https://colab.research.google.com/drive/1LC29rkqaIGd-BWf2xxAJng2TPVPJ9QSn?usp=sharing

Make sure to have GPU as runtime

Replace the 4 variables mentioned above

Run the notebook and enter your AuthToken for connecting gdrive

In the second last cell there are 4 lines containing Host, Hostname, User, Port - will be used later

Leave the last cell running to prevent Colab from closing session 

Open VSCode on local

Make sure to have Settings Sync as On (Type Settings Sync in Command Palette)

Install extension Remote Development on local VSCode (if not already installed)

Open command palette and type Remote-SSH: Open Configuration File -> /home/$USER/.ssh/config (where $USER = your username)

Paste the Host connection details in second last cell of Colab (step 6) and save

Open command palette and type Remote-SSH: Connect To Host -> google_colab_ssh

A new Window should open up with google_colab_ssh as Remote Host

Accept the fingerPrint prompt; when prompted, type in your password set previously in Colab

Go to extensions tab and click on the cloud button beside SSH:GOOGLE_COLAB_SSH - you should be able to select all extensions and install

Select the Python interpreter in command palette and select ~/miniconda3/envs/ml/bin/python as your interpreter

You are now setup with VSCode on Local running on Remote Google Compute Engine!!
