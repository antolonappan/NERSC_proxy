# NERSC_proxy
Password less login for NERSC

Save the NERSC password in `~/.mypass`

For generating the key for 24 hours use, `bash sshproxy.sh -u <OTP>`

Also one can add the function `nersc` in **nersc_proxy** to `bashrc` or `zprofile`

Then you can use it as `nersc <OTP>`

add the lines in `vscode` to the ssh config file of VS Code(for connecting to NERSC using VS Code)
