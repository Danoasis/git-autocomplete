# git-autocomplete

git autocomplete instructions for MAC terminal (works for catalina)

Go to: [Git completion web page](https://github.com/git/git/blob/master/contrib/completion/git-completion.bash)

Click the RAW button

Open terminal and write on your home folder ``/user/yourname``
```bash
Curl -OL the.raw.link.of.the.file
``` 

Check that you have a .bash_profile
file  in your home folder with 
```
ls -al
```
or type 
```
mdfind .bash_profile
```
if you don't have .bash_profile create it using

``nano .bashprofile 
``
(with this option after you paste the code do ctrl + o then press enter (return) and then ctrl + x to exit
or `touch .bash_profile` (this will create a file you can access) 

check with `ls -al` if it's there and put this in the file that you created using vim or any text editor that you use:
```
export PATH="$HOME/bin:$PATH";
source ~/git-completion.bash
```
(with vim .bash_profile press i in the keyboard to insert then press esc and write wq to save and quit file)

Note: if you're not sure about the how to use a text editor in your terminal you can google: how to use vim or vi.

Save it and in your home folder 

write in terminal `nano .bashrc` and add the next code lines to the file: 

Note: 
``
[ -n "$PS1" ] && source ~/.bash_profile; 
``
should be in your .bashrc file

```
if[ -f ~/.git-completion.bash ]; then
	source ~/.git-completion.bash
fi

Type source ~/git-completion.bash
```

Close and open a new terminal

Type `git h` and hit tab it should complete to `git help`

