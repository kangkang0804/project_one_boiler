# Project One Awesome Boilerplate 🍛

Before getting started, as a general rule of thumb, you should be running the commands you see within the project directory. If you experience errors, your first check should be to run `pwd` and ensure the folder name you see returned is the one you should be in.

## First Time Setup
SKIP THIS IF YOU ALREADY HAVE DOCKER INSTALLED ON YOUR MACHINE

Only do this the first time you clone the repo. All you need to do is install docker and make sure it's running.

---
#### 1) Join Docker
* Create a Docker account [here](https://hub.docker.com/signup).
---
#### 2) Install Docker
* Windows Users: Install Docker [here](https://download.docker.com/win/stable/Docker%20for%20Windows%20Installer.exe).
* Mac Users: Install Docker [here](https://download.docker.com/mac/stable/Docker.dmg).

------ WARNING! ------

You may need to restart and update your computer after you install docker. This may take a few moments. Afterwards you may need to open the Docker application from your start menu, desktop, or your Applications / Program Files folder depending on your operating system. Once opened, login to the Docker account you previously created and you should be good to go.

On Windows when Docker is installed and running, you should see an icon in the notification area that looks like this: ![dockerwin](https://d1q6f0aelx0por.cloudfront.net/icons/whale-x-win.png)

On Mac when Docker is installed and running you should see a tool bar item that looks like this:
![dockermac](https://d1q6f0aelx0por.cloudfront.net/icons/whale-in-menu-bar.png)


#### 3) Install Yarn

If you have not already installed yarn, do so now.

* Windows Users: Install Yarn [here](https://yarnpkg.com/latest.msi).
* Mac Users: Using Homebrew Install Yarn like this: `brew install yarn`

#### 4) Building The Image

Get into the project directory first and then run the following.

```
yarn first-time-setup
```

IF THIS DOES NOT WORK TRY RUNNING `docker-compose up` first and then rerun `yarn first-time-setup`

Note: On Windows you will need to give admin access and a login screen will come up. You need to give it your PC password to allow Docker to run.

If you get authorization errors, run `docker logout` and repeat the above steps

## Using The Dev Environment Any Other Time

To start the container and server run `yarn dev` On Windows, you may need to use Powershell or cmd as opposed to gitbash for some docker stuff.

Visit `localhost:3000` in your chrome browser and you will see the `index.html`

With the server running you can restart it at any time by typing `rs` into the window and hitting enter.

Your files go in the following folders:

```
...
public
 --html <- html files get generated here
 --css <- put your css here
 --javascript <- put your javascript files here
 --images <- put your images here
...
```

If you run into any problems, first try to run `yarn rebuild` if that doesn't work restart your machine and run it again.

NOTE: If you need to close the Docker process in terminal at any time you can use either `ctrl + d` or `ctrl + c`

## Screen Generator

To generate a new screen for example an "about" page, you can run `yarn generate-screen -- about` in a new terminal tab and then reload the server in the previous tab with `rs` like stated above.

The result of these commands will give you an autogenerated html file in your `public/html` folder and call it `about.html`.

After a successful restart of the server you can visit your newly generated screen at `localhost:3000/about`. EZ PZ.

Obviously when you do this yourself, change the `about` to whatever you want to name your new screen.

## If Nothing Is Working

Try `yarn && yarn start`. Then visit `localhost:3000` in your browser.
