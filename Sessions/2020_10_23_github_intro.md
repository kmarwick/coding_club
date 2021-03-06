## KT Coding Club: Introduction to Git and Github

### Checklist:
*NB. I do all the following in a terminal on Mac. There is also the option to run the terminal within R studio - I've not tried this but heard it can be slow. You should also be able to run it in Windows equivalent of terminal.*
##### Already have git and github set up? Go to stage 4:
____________
1. [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) on your computer.


   *Easiest way to do this on UNIX OS is to use the package manager [Homebrew](https://docs.brew.sh/Installation/):* ``` brew install git ```



2. Create a [github](https://github.com/) account.
3. Set up git with your username and email. Follow this simplified guide [here](https://kbroman.org/github_tutorial/pages/first_time.html), including configuring your username and email associated with github and using an SSH key.

___________


4. Create a Git repository.

    - Change directory to a folder you want to put on Github:
    *NB. Stay in this directory for the commands after this too.*
    ```
    $ cd path/to/your/folder
    ```
    - Initialise your Git repo:
    ```
    $ git init
    ```

5. Create a [.gitignore](https://www.pluralsight.com/guides/how-to-use-gitignore-file) file:

    - Create a new file called .gitignore
    *Note that any files with a "." in front of them are hidden. On Mac use Command+Shift+Dot to toggle between these files shown or hidden in Finder.*
    ```
    $ touch .gitignore
    ``` 
    - Open it in a text editor (eg. [vi](https://www.washington.edu/computing/unix/vi.html)) and add any filenames or folders you don't want to commit. Include any large files in this.
    ``` 
    $ vi .gitignore
    ```

6. Create a README.md file:
    - This is a file that explains the project. We will have a session in the future on what should be included in a good README. 
    - The language this file is written in is ["markdown"](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)
    - Similar to creating our .gitignore file we can create a README.md and edit it in vi or your text editor of choice.
    ```
    $ touch README.md
    $ vi README.md
    ```

7. Make your first commit.
    - Add all files in current folder to the staging area:
    ```
    $ git add .
    ```
    or just some of the files
    ```
    $ git add file_name
    ```
    - "Commit" these changes to your repository:
    ```
    $ git commit -m "Short descriptive message detailing the commit. eg. Create repo"
    ```

8. Put your Git repo onto Github:
    - Go to [Github](www.github.com)
    - Click on "New" in the top left.  
    ![github_repo](../markdown_images/github_repo.png)
     - Enter the name of your project and choose whether to make it private or public.
    *NB If you don't have the option to make it private you need to change your settings to a student account associated with your university email address.*  
    ![Repo](../markdown_images/github_repo2.png)
    - Push your existing repo from the command line:
    ```
    $ git remote add origin git@github.com:AmeliaES/Project_name.git
    $ git branch -M main
    $ git push -u origin main
    ```

9. Now you're set up and your repo is on Github, this is generally the order of commands I use after making some changes:
*NB. I should really improve this by using branches as well.*

    ```
    $ git pull
    $ git status
    $ git add file_or_folder_names_to_commit
    $ git commit -m "Useful message detailing the commit"
    $ git push
    $ git status
    ```

### Other useful links:
- [Github cheatsheet](https://education.github.com/git-cheat-sheet-education.pdf)
