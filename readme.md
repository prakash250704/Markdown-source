# Static Website Hosting

Hello Everyone. 

I will share something with you about how to display the templates on the server side and I hope it is helpful for my tech friends.
## Introduction
This is my first website hosting on ec2 instance
![website UI](./img/ss1.png)

# Steps:
1: Go to AWS management console and sign in. Click on launch instances and create the instance.
![website UI](./img/ss2(1).png)

2: Download the static website hosting templates file from browser, it is in zip format.

3: After downloads cut and paste in ssh-key folder in simple format(means not in zip format). If you want to rename it then rename it, I do rename as catalog_z.

4: Now open the git bash here from your ssh-key and type the command: 
# scp -i "north-v-key" -r catalog_z/ ec2-user@3.3.3.3:/home/ec2-user/
where, 
"north-v-key" -> private key,
-r -> use for folder
catalog_z -> Your downlaoded folder
3.3.3.3 -> Mention your public ip
and other words in commands you can type same.

5. Now, your all files, folders, pictures, videos are install on server side.

6. Now, you will go on your instances and connect and copy the URL & paste on git bash.
![Website UI](./img/ss3.png)

7. Type some cammands and run it on the incognito window:
    ## Commands:
    - **ls**                     # to display data
    - **cd catalog_z**          # enter into catalog_z
    - **cd ..**                 # exit
    - sudo cp -r catalog_z/* /usr/share/nginx/html/ # copy all files from catalog_z and paste in /usr/share/nginx/html/
    - **cd /usr/share/nginx/html/**    # enter in html
    - **ls**                           # to display data of html

    - **cat /etc/nginx/nginx.conf**     # to check the server information like port no., path, or .html file.
    ![Website UI](./img/ss7.png)

    - **sudo vim /etc/nginx/nginx.conf**  # to make changes in server information if you want.
    ![Website UI](./img/ss7(1).png)

8. Now last step, Copy your public IP and paste on incognito window. It will display the GUI of your request on the browser.


I will be share fully practically next time and we are downlaoding the new template.
   ## Thank You !!