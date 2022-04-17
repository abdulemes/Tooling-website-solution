# Project Workflow

## Setting up VM environment

Step 1 - EC2 instances for webservers, DB server and NFS server were setup.

![IMG_9769](https://user-images.githubusercontent.com/93732510/163687501-c0af213d-00c9-4df4-99e2-afa9d1794587.jpg)

## Preparing NFS server

Step 1 - After logging into the server, the block devices attached to the are inspected.

![IMG_9709](https://user-images.githubusercontent.com/93732510/163679938-9c84dad1-e0a7-4707-bb04-12f0f7e4b51d.jpg)

Step 2 - Single partition is then created on each of the 3 disks.

![IMG_9714](https://user-images.githubusercontent.com/93732510/163680068-c2473c00-58cc-43c6-aed3-0e9a208bf15f.jpg)

Step 3 - The newly created partition is now inspected.

![IMG_9715](https://user-images.githubusercontent.com/93732510/163680140-bfab9412-b23f-4d7a-8a97-6814daaef090.jpg)

Step 4 - lvm2 package is installed and available partition is then checked.

![IMG_9716](https://user-images.githubusercontent.com/93732510/163680229-485538a1-54b2-4fd8-8a51-3420a494421e.jpg)

![IMG_9717](https://user-images.githubusercontent.com/93732510/163680260-4da66b9d-9b6b-4997-9cc0-0571095c8ca6.jpg)

Step 5 - Physical volumes to be used by lvm are created and then added to a group.

![IMG_9775](https://user-images.githubusercontent.com/93732510/163688853-4ab629f7-49a4-4426-a9d4-d66d47047190.jpg)

Step 6 - The logical volumes are then formatted as xfs.

![IMG_9777](https://user-images.githubusercontent.com/93732510/163706922-71ef12f5-291e-45b2-a890-8e4e32fc2cdb.jpg)

Step 7 - Mount points are created and then the volumes are mounted to thier respective directories.

![IMG_9778](https://user-images.githubusercontent.com/93732510/163707182-b81b0dd8-254c-46ce-a78a-16768e387125.jpg)

Step 8 - NFS server is installed, enabled and status checked.

![IMG_9779](https://user-images.githubusercontent.com/93732510/163707241-e5190503-3a86-41c8-928d-2fd0500a447c.jpg)

Step 9 - Permission is set to allow web servers to read, write and execute files on NFS.

![IMG_9782](https://user-images.githubusercontent.com/93732510/163707401-90606950-8a66-4578-a579-de82102d4e6f.jpg)

Step 10 - Access to NFS clients is configured within the same subnet.

![IMG_9783](https://user-images.githubusercontent.com/93732510/163707528-e7aa5f61-372f-4472-8bf1-35802cd17f07.jpg)

Step 11 - NFS port is checked.

![IMG_9784](https://user-images.githubusercontent.com/93732510/163707665-877f1a33-8e5f-4353-812b-3706428d22f2.jpg)

Step 12 -  Below ports are opened on NFS server so clients can access it.

![IMG_9786](https://user-images.githubusercontent.com/93732510/163707724-c9034793-d7cf-4d12-a091-b9aeeb15618a.jpg)

## Configuring database server

Step 1 - Mysql server is installed and database created.

![IMG_9780](https://user-images.githubusercontent.com/93732510/163707901-f8d77831-0ad4-4bf0-86de-708b9d14c99e.jpg)

## Configuring the web servers

Step 1 -  NFS client is installed and /var/www mounted.

![IMG_9789](https://user-images.githubusercontent.com/93732510/163708892-b697390e-0db5-49a2-b57a-72ad69ebbcd5.jpg)

Step 2 - fstab is updated so the changes will persist after reboot.

![IMG_9790](https://user-images.githubusercontent.com/93732510/163708951-1fc63d50-d7bc-40ef-a395-ae73ce0dd8fc.jpg)

Step 3 - Apache, PHP and Remis's repository are installed, enabled and started.

![IMG_9792](https://user-images.githubusercontent.com/93732510/163709002-a4245a1a-75b2-42a8-bd96-9ea098e98d6f.jpg)

Step 4 - Tooling source code was forked from github.

![IMG_9793](https://user-images.githubusercontent.com/93732510/163709095-92d3b79b-e295-4e83-a96f-748db94ff5f8.jpg)

Step 5 - Databse was updated with an admin user, users inserted, tooling script added.

Step 6 - Application was acessed via browser.

![IMG_9794](https://user-images.githubusercontent.com/93732510/163709182-1273c002-45e4-40ee-8994-c2d9a2e27e99.jpg)
