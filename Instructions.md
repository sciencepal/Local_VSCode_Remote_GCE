Create an ngrok token from https://ngrok.com/

Open the Notebook https://colab.research.google.com/drive/1LC29rkqaIGd-BWf2xxAJng2TPVPJ9QSn?usp=sharing

Make sure to have GPU as runtime

Replace ngrok token obtained from Step 1 and fill in a custom password

Run the notebook and enter your AuthToken for connecting gdrive

In the second last cell copy the 4 lines containing Host, Hostname, User, Port

The last cell will keep running to prevent Colab from closing

Open VSCode on local

Make sure to have Settings Sync as On (Type Settings Sync in Command Palette)

Install extension Remote Development on local VSCode (if not already installed)

Open command palette and type Remote-SSH: Open Configuration File -> /home/$USER/.ssh/config (where $USER = your username)

Paste the Host connection details copied from Colab in step 6 and save

Open command palette and type Remote-SSH: Connect To Host -> google_colab_ssh

A new Window should open up with google_colab_ssh as Remote Host - Type in your custom password when prompted

Go to extensions tab and click on the cloud button beside SSH:GOOGLE_COLAB_SSH - you should be able to select all extensions and install

You are setup with VSCode on Local running on Remote Google Compute Engine!!

</br>

**Optional Steps / Getting started with an ML framework (Could have automated these steps but I will leave it to your discretion):**

</br>

Open a new terminal in VS Code and type the following commands

curl -o /tmp/Miniconda3-latest-Linux-x86_64.sh https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh

chmod +x /tmp/Miniconda3-latest-Linux-x86_64.sh

sh /tmp/Miniconda3-latest-Linux-x86_64.sh -b -p

alias conda=/root/miniconda3/bin/conda

conda init bash

*At this point you may need to restart bash terminal*

git clone https://github.com/sciencepal/Local_VSCode_Remote_GCE.git /tmp/Local_VSCode_Remote_GCE

conda env create -f /tmp/Local_VSCode_Remote_GCE/environment.yml

conda activate ml

Voila you can begin coding -> remember to work in the folder /root/gdrive/MyDrive/Colab\ Notebooks as it is your Google Drive mount .. else you will lose the data when you close
