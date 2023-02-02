<!-- ---
Title: Access a lab in Azure Lab Services 
Description: In this tutorial, students access to the cluster of virtual machines in the EECS4222-lab
Topic: Tutorial
Date: 01/02/2023
--- -->

# Tutorial: Access the EECS4222 lab in Azure Lab Services

In this tutorial, you, as a student, connect to a your cluster of virtual machines (VM) in a lab by completing the following actions in the Lab Services web portal: [https://labs.azure.com](https://labs.azure.com):

- [x] Register to the lab
- [x] Start the Cluster
- [x] Connect to Cluster Head (i.e., Windows Server VM) using RDP program
- [x] Connect to Ubuntu VMs via the Cluster Head 

## Register to the lab

1. Navigate to the **registration URL** that you received from the educator. You only have to use the registration URL once to complete the registration.  

<img title="" alt="Click on Sign in to go to the login page" src="/images/login.png" >

2. Sign in using your YorkU account to complete the registration.

<img title="" alt="Click on Sign in to go to the login page" src="/images/username.png" width="500" >


3. Once registered, confirm that you see the virtual machine for the lab you have access to.  Now that you have registered, you can go directly to the Azure Lab Services portal at [https://labs.azure.com](https://labs.azure.com) in the future.

<img title="" alt="Click on Sign in to go to the login page" src="/images/eecs4222-lab.png" width="500" >

    
1. Wait until the virtual machine is ready. On the VM tile, notice the following fields:
    1. At the top of the tile, you see the **name of the lab**.
    2. To its right, you see the icon representing the **operating system (OS)** of the VM. In this example, it's Windows.
    3. The progress bar on the tile shows the number of hours used against the number of [quota hours] assigned to you. Quota time is time you have in addition to the scheduled time for the lab.
    4. You see icons and buttons at the bottom of the tile to start, stop, and connect to the VM.
    5. To the right of the buttons, you see the status of the VM. Confirm that you see the status of the VM is **Stopped**.
        

## Start the VM

1. **Start** the VM by selecting the toggle button as shown in the following image. This process takes some time.  
    
2. Confirm that the status of the VM is set to **Running**.
    

## Connect to the Windows VM (Cluster Head)

1. Select the button in the lower right of the tile as shown in the following image to download the RDP configuration file. This file will be used in RDP desktop program to get connected to the VM. 
   1. Download the RDP Desktop for your laptop. It is available for operating systems.
   2. Open the RDP desktop program and then drag the RDP config file toward the program.
   3. You should see a PC created in your RDP Desktop.
   4. Before starting you VM from RDP desktop make sure your VM is in **Running** state.
   5. Then double click on the new remote PC that you created in RDP desktop.
   6. It should ask for username and password that you already received from the instructor.

Here you will be connected the Windows VM which in fact acts as the cluster head. Using this cluster head we can get access to the Ubuntu VMs that are the one that you will use for the project.

 ## Connect to the Ubuntu Servers

1. On the Windows machine's desktop you will see a program name ***Hyper-V Manager***. Open that program and then you should be able to see three Ubuntu VMs that are running.

2. Here is the information of these three VMs:

    | Name         | IP Address      |
    | :-------     | :------------   |
    | server1      | 192.168.0.100   |
    | server2      | 192.168.0.101   |
    | server3      | 192.168.0.102   |


3. Open the terminal in the Windows machine, i.e., cmd.exe, program.
4. From there `ssh` to the Server1 by running: `ssh eecs@192.168.0.100`
   1. The password for `eecs` user have been posted to your by the instructor.
   2. Repeat step 1 for server2 and server3 as well.
   3. At this point you should have 3 terminal attached to your 3 Ubuntu VMs as the picture bellow.

These Ubuntu VMs are the machines that you need to use to do your projects. 

## Next steps

In this tutorial, you accessed a lab using the registration link you got from your educator.  When you are done, close the RDP program so that all your cluster be shutdown after a short time. This way you are not going to lose your quota while not working on your project.