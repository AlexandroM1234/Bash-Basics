# Bash-Basics

## Task 1: Making Zsh my default shell

- This one is pretty simple in the nsswitch.conf file uncomment out db_shell: /bin/bash and change it to db_shell: /bin/zsh and done
  ![image](https://user-images.githubusercontent.com/59548630/140615621-2cb37e0b-9a39-4942-a3af-02ee23a2ec00.png)

## Task 2

- Now our prompt and looks a little bland close to something like this
  ![image](https://user-images.githubusercontent.com/59548630/140765755-e0be2782-9b40-4457-a046-b5dbc45a1d3b.png)

- and lets say you want to customize it up just a little bit like change the colors a bit or make your own custom theme
- in your .oh-my-zsh directory theres another directory in there called themes you can make the name whatever you want as long as it end in .zsh-theme

- For the first line its the PROMPT line and it may look something like this

- PROMPT="%{$fg_bold[green]%1}"
- From left to right you declare the prompt in all caps followed by the equals sign
- Then in quotes its followed by %{....%}
- inside of the brackets you decalare what you want the folor to be in our case its green and the %1 makes it so it shows the current directory without a symbol unless its the root directory in that case a ~ will show up on the left
- Now the next section is if you want some git information to show up if you use git
- The ZSH_THEME_GIT_PROMPT_PREFIX defines the git pefix and what it says
  ![image](https://user-images.githubusercontent.com/59548630/140810281-622bc84a-60a5-4c9a-b1ee-30c92c1a920d.png)

- so it my case it says branch and its in light purple and it says branch: and you can make it say whatever like current branch:, git etc.
- The ZSH_THEME_GIT_PROMPT_SUFFIX defines what color is typed out after the git command in my case its just the default reset color
- The ZSH_THEME_GIT_PROMPT_DIRTY defines what shows up when the current branch you are working on has changes that aren't commited in my case its a red x mark
- Finally ZSH_THEME_GIT_PROMPT_CLEAN defines what happens when the working branch is clean and has no changes

![image](https://user-images.githubusercontent.com/59548630/140810207-5c589318-e737-4c94-9558-1b9a79ccf077.png)

- With all the changes it looks something like this
