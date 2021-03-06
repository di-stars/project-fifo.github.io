---
layout: default
category: jingles
section: jingles/machines
title: Jingles Machines
---
# Jingles Machines

## List<a id="list"></a>
![](/assets/img/jingles/machines01.png)

The "Machines" tab is the central area within the UI where new virtual machine are created and where most of the actions related to existing virtual machines are performed.

1. Column Selector : Click the column selector and check the columns you would like to display.

    ![](/assets/img/jingles/machines02.png)

2. The filter entry area is designed to selectively filter the machines that are displayed in your list by your filter criteria. The filter is designed to remember what you have typed and will continue filter by your custom criteria even if you leave and return to the machines tab.

    ![](/assets/img/jingles/machines03.png)

3. Clicking on the "new machine button" will launch a new UI page which contains options relevant to new vm creation.     ![](/assets/img/jingles/machines04.png)

4. The "Action Icons" are used to perform specific actions on machines directly from list view list.
  1. ![](/assets/img/jingles/machines-kvm.png) Launch zone/kvm console.
  2. ![](/assets/img/jingles/machines-zone.png) Power on a machine.

## Create<a id="new"></a>

![](/assets/img/jingles/machines05.png)

1. Choose the name or alias of your new machine.
2. Choose the dataset that will be used for your new machine.
3. Choose the package that will be used for your new machine.
4. Choose the network/s your machine will be connected to. Please note: you will only be able to select more than 1 network if the package selected supports multiple networks.
5. Choose optional advanced paramaters if you require them.

    ![](/assets/img/jingles/machines06.png)

6. Click the create button to start machine creation.



## Details<a id="details"></a>
![](/assets/img/jingles/machines07.png)

1. Shows the current realtime state of the machine.

2. These "action buttons" perform the following actions:
 - ![](/assets/img/jingles/machines-destroy.png) Destroythe machine.
     - Note: only clickable if machine is both "stopped" and is not "lock protected".
     - A confirmation dialog will ask you for confirmation before the machine is deleted.
 - ![](/assets/img/jingles/machines-console.png) Launch the machine's zone or kvm console.
 - ![](/assets/img/jingles/machines-lock.png) Lock protect the machine to ensure no accidental changes can be made.
 - ![](/assets/img/jingles/machines-start.png) Start the machine, only clickable if machine is in a stopped state.
 - ![](/assets/img/jingles/machines-restart.png) Restart the machine, only clickable if machine is in a running state.
 - ![](/assets/img/jingles/machines-stop.png) Stop the machine, only clickable if machine is in a running state.

3. Machine sub tabs contain sub sections relevant to your machine, we will explore each one in more detail below.
4. Sub tab display area will show you information related to the sub tab you have selected.
5. The default "details" tab includes a color selector which will mark your vm a certain color in the "machine list" view page. This is useful for easily and quickly identifying certain machines in the list or for grouping certain types of machines with common colors.
6. Clicking on the "blue" edit configuration icon will expand a section which will allow you to change certain machine fields.

    ![](/assets/img/jingles/machines-conf.png)
     - **Describe** A internal own use field thats can be enabled as one of the columns in machine list view.
     - **Alias** Change the alias name of the machine.
     - **Hostname** Change the machines's hostname.
     - **Resolvers** Change the machines resolvers.

### Machine Performance TAB

![](/assets/img/jingles/machines08.png)

The performance tab shows various metrics and performance graphs relating to the machine.

Disk IOPS
Disk throughput
Memory usage
Swap Usage
CPU usage
Network throughput
Network packets per second

### Snapshots
![](/assets/img/jingles/machines09.png)

The snapshots tab is where you create snapshots and where you can roll back to previous snapshots. The rollback icon will only be visible if the machine is in a "stopped" state and is not "lock protected".  To create a snapshot simply click the snapshot button and enter a name/comment for your snapshot in the snapshot popup window and then click the "ok" button to create it. It is important to note that when rolling back a snapshot all snapshots that exist after the rollback date will be destroyed. To delete a specific snapshot click on the "trash" icon next to the snapshot.

### Resize
![](/assets/img/jingles/machines10.png)

The resize tab is used to upgrade or downgrade your vm by associating it with a different package. The cpu share, cpu cap, ram and disk size will be changed when a package is changed. To do this simply select a new package in the "Change to" area and click the "change" button to apply the change. The change will be applied in real time if the machine is a smartmachine / zone based machine. If the machine is KVM based machine it will require a shutdown and startup for the changes to take effect.

### History
![](/assets/img/jingles/machines11.png)

The history tab is where you can view a chronological record or log of any actions or changes that have occurred with the machine. All entries are associated with a date/time entry related to when the change occurred.

### Notes
![](/assets/img/jingles/machines12.png)

The notes tab is a area for you to record notes or details related to the machine. This can be any information that you deem useful and would like to remember. To create a note simply click on the "+" button and type your note into the popup dialogue and then click ok to create the note. Each individual note is time stamped so you know when it was created. To delete a note, simply click on the <kbd>x</kbd> icon in the top right hand corner of the note.
