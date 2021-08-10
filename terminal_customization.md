
## Change bash profile:

* Customize bash terminal as per our choice
* While starting terminal os will load the bash_profile and put our customization
* for mac os only creating .profile will work as it loads bash from ".profile"
* for other os you need to put your changes in .bashrc and call it from .bash_profile.



1. touch ./bash_profile
2. touch ./bashrc
3. touch ./profile


* for editing document (you can use any other editor e.g. vim, subl)

4. nano .profile
5. nano .bashrc

orange=$(tput setaf 166);
yellow=$(tput setaf 228);
green=$(tput setaf 71);
white=$(tput setaf 15);
bold=$(tput bold);
reset=$(tput sgr0);

PS1="\[${bold}\]\n";
PS1+="\[${orange}\]\u";   # username
PS1+="\[${white}\] at ";
PS1+="\[${yellow}\]\h";   # host
PS1+="\[${white}\] in ";
PS1+="\[${green}\]\W";     # working directory
PS1+="\n";
PS1+="\[${white}\]\$ \[${reset}\]";    # $ and reset color
export PS1;
export PATH="/usr/local/bin:$PATH" 


* put below commands in ".bash_profile" (we will be running .bashrc from .bash_profile)

6. nano .bash_profile

if [ -f ~/.bashrc ]; then
    source ~/.bashrc
fi
