[< back to contents](./readme.md)

# Adding public ssh-key to github.com

1. Copy the ssh public key to clipboard:
   ```
   clip < ~/.ssh/your_key.pub
   ```
   or copy it manualy from file `~/.ssh/your_key.pub`
2. In the upper-right corner of any page, click your profile photo, then click **Settings**.   
    ![](./assets/screen_1.png)
3. In the user settings sidebar, click **SSH and GPG keys**.   
    ![](./assets/screen_2.png)
4. Click **New SSH key** or **Add SSH key**.   
    ![](./assets/screen_3.png)
5. In the "Title" field, add a descriptive label for the new key. For example name of you PC.
6. Paste your key into the "Key" field.   
    ![](./assets/screen_4.png)
7. Click **Add SSH** key.   
    ![](./assets/screen_5.png)
8. If prompted, confirm your GitHub password.
   
So, now you can push your work to github from local machine using SSH key

[<Previous](./ssh.md) ... [Next>](./config.md)