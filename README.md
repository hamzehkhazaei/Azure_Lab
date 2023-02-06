<!-- ---
Title: Access a lab in Azure Lab Services 
Description: In this tutorial, students access to the cluster of virtual machines in the EECS4222-lab
Topic: Tutorial
Date: 01/02/2023
--- -->

# Tutorial: Access the EECS4222 lab in Azure Lab Services

In this tutorial, you, as a student, connect to your cluster of virtual machines (VM) in a lab by completing the following actions in the Lab Services web portal: [https://labs.azure.com](https://labs.azure.com):

- [x] Register to the lab
- [x] Start the Cluster
- [x] Connect to Cluster Head (i.e., Windows Server VM) using RDP program
- [x] Connect to Ubuntu VMs via the Cluster Head 

## Register to the lab

1. Navigate to [https://labs.azure.com](https://labs.azure.com).  

   <img title="" alt="Click on Sign in to go to the login page" src="/images/login.png" >

2. Sign in using your YorkU account, i.e., `user@yorku.ca` and your `PPY` password to complete the registration.
   
   <img title="" alt="Enter your York username" src="/images/username.png" width="500" >

3. Once registered, confirm that you see the virtual machine for the lab you have access to.  Now that you have registered, you can go directly to the Azure Lab Services portal at [https://labs.azure.com](https://labs.azure.com) in the future.
    
4. Wait until the virtual machine is ready. On the VM tile, notice the following fields:
    1. At the top of the tile, you see the **name of the lab**.
    2. To its right, you see the icon representing the **operating system (OS)** of the VM. In this example, it's Windows.
    3. The progress bar on the tile shows the number of hours used against the number of [quota hours] assigned to you. Quota time is time you have in addition to the scheduled time for the lab.
    4. You see icons and buttons at the bottom of the tile to start, stop, and connect to the VM.
    5. To the right of the buttons, you see the status of the VM. Confirm that you see the status of the VM is **Stopped**.
        
   <img title="" alt="" src="/images/lab-stopped.png" width="500" >


## Start the VM

1. **Start** the VM by selecting the toggle button as shown in the following image. This process takes some time.  

   <img title="" alt="" src="/images/lab-starting.png" width="500" >
    
2. Confirm that the status of the VM is set to **Running**.
   
   <img title="" alt="" src="/images/lab-running.png" width="500" >

## Connect to the Windows VM (Cluster Head)
In order to connect to your Cluster head which is a Windows machine do the followings:

1. Select the button in the lower right of the tile as shown in the following image to download the RDP configuration file. This file will be used in RDP desktop program to get connected to the VM. 

   <img title="" alt="Download the RDP config file" src="/images/lab-rdp.png" width="500" >

2. Download and install the RDP Desktop for your laptop. It is available for all operating systems. 
3. Open the RDP desktop program and then drag the RDP configuration file toward the program.
4. You should see a PC created in your RDP Desktop like the following:
   
   <img title="" alt="" src="/images/rdp1.png">

5. Before starting you VM from RDP desktop make sure your VM is in **Running** state.
6. Then double click on the new remote PC that you created in RDP desktop. It should ask for username and password that you already received from the instructor.
   
   <img title="" alt="" src="/images/rdp-login.png" width="500">

Here you will be connected the Windows VM which in fact acts as the cluster head. Using this cluster head we can get access to the Ubuntu VMs that are the one that you will use for the project.

   <img title="" alt="" src="/images/win1.png" >

 ## Connect to the Ubuntu Servers

1. On the Windows machine's desktop you will see a program name ***Hyper-V Manager***. Open that program and then you should be able to see three Ubuntu VMs that are running, like the following picture.  

   <img title="" alt="" src="/images/hyperv.png">

Here is the information of these three VMs:

| Name         | IP Address      |
| :-------     | :------------   |
| server1      | 192.168.0.100   |
| server2      | 192.168.0.101   |
| server3      | 192.168.0.102   |

2. Open the terminal in the Windows machine, i.e., cmd.exe, program.
3. From there `ssh` to the *server1* by running: `ssh your_username@192.168.0.100`
   - The username and password for connecting to *Ubuntu* are **different** than Windows VM. You should have already received this credentials from your instructor as well.
   - Repeat step 1 for server2 and server3 as well.
   - At this point you should have 3 terminal attached to your 3 Ubuntu VMs as the picture bellow.

   <img title="" alt="" src="/images/cmd2.png">

These Ubuntu VMs are the machines that you need to use to do your projects. 

**Note:** In this tutorial, you accessed a lab using the registration link you got from your educator. Please remember to close the RDP program when you no longer wants to work on your project so that all your cluster be shutdown after a short time. This way you are not going to lose your quota while not working on your project.

## Next steps

No you can head over to the Project 1 repository to start working on your project here: [https://github.com/hamzehkhazaei/EECS4222_Project_1](https://github.com/hamzehkhazaei/EECS4222_Project_1).
 