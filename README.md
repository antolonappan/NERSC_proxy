# NERSC_proxy
Password less login for NERSC

Save the NERSC password in `~/.mypass`

Install `oathtool`

Add a new key in iris.nersc.gov. Use the key in the bash function `nersc`

For generating the key for 24 hours use, `bash sshproxy.sh -u <OTP>`

Also one can add the function `nersc` in **nersc_proxy** to `bashrc` or `zprofile`

Then you can use it as `nersc`

Add the lines in `vscode` to the `.ssh/config` file (for connecting to NERSC using VS Code)

Add the task.json to the vscode task
