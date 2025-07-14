## 1. What is version control?
Version Control is a system that tracks and manages changes to a file

## 2. What is the importance of version control?
Version control is important because it provides us a recovery point in the case of data loss or a malfunction. It allows us to revert to a more stable version of our project when needed.

## 3. What is git?
Git is a version control system that runs on your local machine and allows you to track and manage your files locally

## 4. What is github?
Github is a remote platform where users can collaborate on a project and share resources over a central point

## 5. Difference between git and github
The difference between git and github is in its resource or file access. Git is local to your machine, thereby making access available only via that machine while Github provides remote access, making it possible for multiple persons to share resources and collaborate

## 6. Comprehensive git and github setup guide for beginners

1. Open your Terminal
2. Type `git --version` to see if git is installed and what version
3. If git isn't installed type 
    ```
    sudo apt install git
    ```
4. Go to `https://github.com/signup` in your browser and signup to get a github account

5. Go back to your terminal and type the text below to check your current git configuration
    ```
    git config --list
    ```
6. It shouldn't return anything, now type the text below to setup your identity (use your own name and the email used to create github account). Using `--global` makes your identity available anywhere within your machine
    ```
    git config --global user.name "<your_name>"
    git config --global user.email <your_email>
    ```

7. Generate a new ssh key by typing the text below. Use the email you used to create a github accout
    ```
    ssh-keygen -t ed25519 -C "<your_email@example.com>"
    ```
    
8. Start the ssh agent by typing. It displays an ssh agent id when typed in
    ```
    eval "$(ssh-agent -s)"
    ```
    Output
    ```color
    Agent pid 59566
    ```
9. Type whats below to add SSH private key to the ssh-agent.
    ```
    ssh-add ~/.ssh/id_ed25519
    ```
    
10.  Type whats below to display your public key then copy what is displayed
     ```
     cat ~/.ssh/id_ed25519.pub
     ```
    
11. Sign into your github and go to `https://github.com/settings/keys`

12. Click on the `New SSH key` button on the visited page

13. Paste copied key into the `key` section and write a title (preferably device or operating system name) in the `title` section

14. Now click on the `Add SSH key` button to add public key to your Github account. You're now done with your initial setup 
