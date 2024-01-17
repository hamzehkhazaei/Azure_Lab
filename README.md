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

1. Register using your **YorkU** account and your `PPY` password to complete the registration.
2. If you are already a user, sign in using your YorkU account and your `PPY` password.

   <p align="center">
      <img title="" alt="Click on Sign in to go to the login page" src="/images/login.png" >
   </p>

   
   <p align="center">
      <img title="" alt="Enter your York username" src="/images/username.png" width="500" >
   </p>

3. Once registered, confirm that you see the virtual machine for the lab you can access.  Now that you have registered, you can go directly to the Azure Lab Services portal at [https://labs.azure.com](https://labs.azure.com) in the future.
    
4. Wait until the virtual machine is ready. On the VM tile, notice the following fields:
    1. At the top of the tile, you see the **name of the lab**.
    2. To its right, you see the icon representing the **operating system (OS)** of the VM. In this example, it's Windows.
    3. The progress bar on the tile shows the number of hours used against the number of [quota hours] assigned to you. Quota time is time you have in addition to the scheduled time for the lab.
    4. You see icons and buttons at the bottom of the tile to start, stop, and connect to the VM.
    5. To the right of the buttons, you see the status of the VM. Confirm that you see the status of the VM is **Stopped**.
        
   <p align="center">
      <img title="" alt="" src="/images/lab-stopped.png" width="500" >
   </p>
   


## Start the VM

1. **Start** the VM by selecting the toggle button, as shown in the following image. This process takes some time.  

   <p align="center">
      <img title="" alt="" src="/images/lab-starting.png" width="500" >
   </p>
    
2. Confirm that the VM status is set to **Running**.
   
   <p align="center">
      <img title="" alt="" src="/images/lab-running.png" width="500" >
   </p>

## Connect to the Windows VM (Cluster Head)
To connect to your Cluster head, which is a Windows machine, do the following:

1. Select the button in the lower right of the tile, as shown in the following image, to download the RDP configuration file. This file will be used in the RDP desktop program to get connected to the VM. 

   <p align="center">
      <img title="" alt="Download the RDP config file" src="/images/lab-rdp.png" width="500" >
   </p>

2. Download and install the Microsoft Remote Desktop (MRD) for your laptop. It is available for all operating systems. 
3. Open the MRD program and drag the configuration file toward the program.
4. You should see a PC created in your MRD like the following:
   
   <p align="center">
      <img title="" alt="" src="/images/rdp1.png">
   </p>

5. Before starting your VM from MRD, ensure your cluster is in **Running** state.
6. Double-click on the new remote PC you created on the MRD. It should ask for a username and password. Use `eecs4222M` as your username. You should already know the password from the eClass post.
   
   <p align="center">
      <img title="" alt="" src="/images/rdp-login.png" width="500">
   </p>

Here, you will be connected to the Windows VM, which acts as the cluster head. Using this cluster head, we can get access to the Ubuntu VMs that are the ones that you will use for the project.

   <p align="center">
      <img title="" alt="" src="/images/win1.png" >
   </p>

 ## Connect to the Ubuntu Servers

1. On the Windows machine's desktop, you will see a program named ***Hyper-V Manager***. Open that program, and then you should be able to see three Ubuntu VMs that are running, like the picture below.  

   <p align="center">
      <img title="" alt="" src="/images/hyperv.png">
   </p>

Here is the information on these three VMs:

| Name         | IP Address      |
| :-------     | :------------   |
| server1      | 192.168.0.100   |
| server2      | 192.168.0.103   |
| server3      | 192.168.0.101   |
| server4      | 192.168.0.102   |

2. Open the terminal in the Windows machine, i.e., cmd.exe, program.
3. From there `ssh` to the *server1* by running: `ssh eecs@192.168.0.100`
   - The username and password for connecting to *Ubuntu* are **different** than Windows VM. For Ubuntu servers, use `eecs` as both username and password.
   - Repeat step 1 for server2, server3 and server4 as well.
   - At this point, you should have 4 terminals attached to your 4 Ubuntu VMs, as shown in the picture below.
   - You can see all the allocated and used resources for each VM at the beginning of the session (i.e., hard disk).

   <p align="center">
      <img title="" alt="" src="/images/cmd2.png">
   </p>

These Ubuntu VMs are the machines that you need to use to do your projects. 


**Important Note:** Please remember to close the RDP program when you no longer want to work on your project so that all your clusters can be shut down quickly. This way, you will not lose your quota while not working on your project.
 
