# NERSC_proxy
Password less login for NERSC


# Steps:


1. Save the NERSC password in your home directory `~/.mypass` (or somewhere safe as a hidden file. This file will be read at Line 234 of `sshproxy.sh`)
2. Save the `sshproxy.sh` in a directory (for example,/home/username/softwares/NERSC_proxy)
3. Edit the line 233 of `sshproxy.sh` with your username.
4. Install `oathtool` https://formulae.brew.sh/formula/oath-toolkit
5. Add a new key in https://iris.nersc.gov. Go to the section __MFA__. Click on __Add token__. Copy the __Authy Code__, the 32 alphanumeric key displayed. Replace the hyphen with a single space and use it in the next step(for ex, change `ABCD-ASDF` to `ABCD ASDF`)
6. Copy the function `nersc_proxy` in the file __nersc_proxy__ to your `.bashrc` or `.zprofile`, and copy-paste the key from the previous step(remove the angle bracket)
7. source the `.bashrc` file.
8. Now execute `nersc` from a new terminal. This will save the SSH keys for 12 hrs. 
9. Now ssh to Cori or Perlmutter without a password.
10. If you use VScode, add the lines in the file `ssh config` to `.ssh/config`.
11. Install the VScode extension `Remote SSH`.
12. Also, you can add a task in VScode to run the command `nersc` directly from the vscode. Go to command pannel( shift+ctrl+p) in mac instead of ctrl, try cmd, type 'task' and click on the 'configure task'. Copy the lines in `task.json`. Save and exit. Now you can go to the command panel again and write the task; you can see the 'Run task'. 
13. Run the task before connecting to the NERSC; you will need to rerun it after 12 hours.
