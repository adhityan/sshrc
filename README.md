# sshrc

Automatically copies the .sshrc file to remote after ssh and sources it. Very useful if you want to carry along your alias definitions to remote.

## Installation

Download and copy the sshrc file to $PATH. 


    $ wget https://raw.githubusercontent.com/adhityan/sshrc/master/sshrc &&
    chmod +x sshrc &&
    sudo mv sshrc /usr/local/bin #or anywhere else on your PATH

Next create a .sshrc in your home directory and enjoy.

## Usage

When connecting to a server use ```sshrc``` instead of ```ssh```. Works with your ssh config file.

```sshrc``` will copy over your local .sshrc file to remote and source it for you. I usually include a message along the lines of ```echo -e "\nWelcome \033[0;31mAdhityan\033[0m! This ssh connection is upgraded to your bash.\n\n"``` which pops up after the ssh connection completes letting me know my settings have been copied in.

Lastly, you can alias ```ssh``` to use ```sshrc``` like so ```alias ssh='sshrc'``` in your .bash_profile or .zshrc file. This makes it easy to not forget using sshrc.

## More Info

This bash file was originally contributed by https://github.com/Russell91/sshrc. However, his Github account is not available anymore.