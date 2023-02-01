---
title: Access a lab in Azure Lab Services | Microsoft Docs adopted by Hamzeh Khazaei @ EECS department at York University 
description: In this tutorial, students access to the cluster of virtual machines in the EECS4222-lab that's set up by EECS TECH Team. 
topic: Tutorial
date: 01/02/2023
---

# Tutorial: Access a lab in Azure Lab Services

In this tutorial, you, as a student, connect to a your cluster of virtual machines (VM) in a lab by completing the following actions in the Lab Services web portal: [https://labs.azure.com](https://labs.azure.com):

- [x] Register to the lab
- [x] Start the Cluster
- [x] Connect to Cluster Head (i.e., Windows Server VM) using RDP program
- [x] Connect to Ubuntu VMs via the Cluster Head 

## Register to the lab

1. Navigate to the **registration URL** that you received from the educator. You only have to use the registration URL once to complete the registration.  

![Alt text](https://github.com/hamzehkhazaei/Azure_Lab/blob/main/images/login.png "")


1. Sign in using your school account to complete the registration.

    > [!NOTE]
    > A Microsoft account is required for using Azure Lab Services. If you are trying to use your non-Microsoft account such as Yahoo or Google accounts to sign in to the portal, follow instructions to create a Microsoft account that will be linked to your non-Microsoft account email. Then, follow the steps to complete the registration process.
2. Once registered, confirm that you see the virtual machine for the lab you have access to.  Now that you have registered, you can go directly to the Azure Lab Services portal at [https://labs.azure.com](https://labs.azure.com) in the future.
    :::image type="content" source="./media/tutorial-connect-vm-in-classroom-lab/accessible-vms.png" alt-text="Screenshot of My virtual machines page in Azure Lab Services portal.":::
3. Wait until the virtual machine is ready. On the VM tile, notice the following fields:
    1. At the top of the tile, you see the **name of the lab**.
    2. To its right, you see the icon representing the **operating system (OS)** of the VM. In this example, it's Windows.
    3. The progress bar on the tile shows the number of hours used against the number of [quota hours](how-to-configure-student-usage.md#set-quotas-for-users) assigned to you. Quota time is time you have in addition to the scheduled time for the lab.
    4. You see icons and buttons at the bottom of the tile to start, stop, and connect to the VM.
    5. To the right of the buttons, you see the status of the VM. Confirm that you see the status of the VM is **Stopped**.
        :::image type="content" source="./media/tutorial-connect-vm-in-classroom-lab/vm-in-stopped-state.png" alt-text="Screenshot of My virtual machines page in Azure Lab Services portal.  VM state toggle with stopped label is highlighted.":::

## Start the VM

1. **Start** the VM by selecting the toggle button as shown in the following image. This process takes some time.  
    :::image type="content" source="./media/tutorial-connect-vm-in-classroom-lab/start-vm.png" alt-text="Screenshot of My virtual machines page in Azure Lab Services portal.  VM state toggle with starting label is highlighted.":::
1. Confirm that the status of the VM is set to **Running**.
    :::image type="content" source="./media/tutorial-connect-vm-in-classroom-lab/vm-running.png" alt-text="Screenshot of My virtual machines page in Azure Lab Services portal.  VM state toggle with running label is highlighted.":::

## Connect to the VM

1. Select the button in the lower right of the tile as shown in the following image to connect to the lab's VM.
    :::image type="content" source="./media/tutorial-connect-vm-in-classroom-lab/connect-vm.png" alt-text="Screenshot of My virtual machines page in Azure Lab Services portal. Connect VM button is highlighted.":::
1. Do one of the following steps:
    1. For **Windows** virtual machines, open the **RDP** file once it has finished downloading. Use the **username** and **password** you get from your educator to sign in to the machine. For more information, see [Connect to a Windows lab VM](connect-virtual-machine.md#connect-to-a-windows-lab-vm).
    2. For **Linux** virtual machines, you can use **SSH** or **RDP** (if it's enabled) to connect to them. For more information, see [Connect to a Linux lab VM](connect-virtual-machine.md#connect-to-a-linux-lab-vm).

## Next steps

In this tutorial, you accessed a lab using the registration link you got from your educator.  When done with the VM, stop the VM from the Azure Lab Services portal.

>[!div class="nextstepaction"]
>[Stop the VM](how-to-use-lab.md#start-or-stop-the-vm)