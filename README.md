# RHEL8-Docker-setup
Welcome to this simple tutorial to set up an RHEL8 (Redhat Enterprise Linux 8) docker container. 

# Installing Docker

To Download Docker Desktop click [here](https://desktop.docker.com/win/stable/amd64/Docker%20Desktop%20Installer.exe?utm_source=docker&utm_medium=webreferral&utm_campaign=dd-smartbutton&utm_location=header) . After Downloading follow the steps below:

1. Double click on the setup, you will see the following:

    ![](../assets/86bf150308a1c7ae197eb114e78cbcbf.png)

    [note: it is recommended to untick Install required Windows components for WSL 2, if you want WSL 2 capability then follow the WSL2 setup section ]

2. Wait for setup to finish and restart your computer. Docker is now installed.


# RHEL-8 Container

To install RHEL-8 Container open command prompt,
and follow the steps below:

1. open cmd and type the following command

    ```
    docker search registry.access.redhat.com/ubi
    ```

    press Enter. You will see this,

    ![](\assets\b52d75867fb9b469b50079dc0812a4b4.png)

2. Next Type this command in the Command prompt,

    ```
    docker run -it --name test registry.access.redhat.com/ubi8/ubi:8.1 bash
    ```

    it will look like this,

    ![](\assets\step6.png)

    you have successfully created an RHEL-8 docker container.

3. You will see the following in your docker desktop application,

    ![](\assets\Screenshot(22).png)

    click on the ">_" symbol to start the container, it should look something like this,

    ![](\assets\final_result.png)

    Congratulations you are now done with the container setup.





# WSL2 Setup [optional]
Do this step if you are getting this error or if you have checked the option during setup.

![](\assets\46e3b3297e998ac846f9a7097138f789.png)

first we need to enable WSL (Windows Subsystem for linux), follow the steps below:

1. click on search icon on taskbar -> type "Turn Windows features on or off"

2. you will see a menu like this:
![](\assets\cf5e93c3e140133154b977ce11b150e3.png)
    Check/Tick Windows Subsystem for linux, click ok and wait for it to enable and the prompt will ask you to restart your computer, then restart your computer.

3. Now you have to update WSL1 to WSL2, download the update from [here](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) .

4. Open CMD(command prompt) and type the following command and press enter:
    ```powershell
    wsl --set-default-version 2
    ```

## Made with ❤️ by Ducky 🦆
