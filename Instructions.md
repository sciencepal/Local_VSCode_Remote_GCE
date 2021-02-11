**Steps to setup Local VSCode on Remote GCE:**

</br>

1. Create an ngrok token from https://ngrok.com/

2. Open the Notebook https://colab.research.google.com/drive/1LC29rkqaIGd-BWf2xxAJng2TPVPJ9QSn?usp=sharing

3. Make sure to have GPU as runtime

4. Replace 4 variables in the Notebook - 

<ul>
  <li>ngrok token</li>
  <li>password</li>
  <li>Github User</li>
  <li>Github email</li>
</ul>

5. Run the notebook and enter your AuthToken for connecting gdrive

6. In the second last cell there are 4 lines containing Host, Hostname, User, Port - will be used later

7. Leave the last cell running to prevent Colab from closing session 

8. Open VSCode on local

9. Make sure to have Settings Sync as On (Type Settings Sync in Command Palette)

10. Install extension Remote Development on local VSCode (if not already installed)

11. Open command palette and type Remote-SSH: Open Configuration File -> /home/$USER/.ssh/config (where $USER = your username)

12. Paste the Host connection details in second last cell of Colab (step 6) and save

13. Open command palette and type Remote-SSH: Connect To Host -> google_colab_ssh

14. A new Window should open up with google_colab_ssh as Remote Host

15. Accept the fingerPrint prompt; when prompted, type in your password set previously in Colab

16. Go to extensions tab and click on the cloud button beside SSH:GOOGLE_COLAB_SSH - you should be able to select all extensions and install

17. Select the Python interpreter in command palette and select ~/miniconda3/envs/ml/bin/python as your interpreter

18. When opening a new terminal, if (base) env is activated : type *conda activate ml* first to start running code

**You are now setup with VSCode on Local running on Remote Google Compute Engine!!**
