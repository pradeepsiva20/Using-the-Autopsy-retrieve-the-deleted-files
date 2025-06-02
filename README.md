# File_Recovery-using-Autopsy
### Name : PRADEEP S
### Reg.No : 212222100034
## Aim
The objective of this guide is to demonstrate how to:

- Create a Virtual Hard Disk (VHD).
- Add images to the disk, delete them, and recover them using Autopsy.
- Understand the forensic recovery process for deleted files.
- Learn how to remove the virtual disk after completing the experiment.

## Virtual Disk Creation & File Recovery using Autopsy
### Step 1:
Create a Virtual Hard Disk (VHD)

### 1. Open Disk Management
- Press Windows + X → Click Disk Management

![disk1](https://github.com/user-attachments/assets/f5f69c3b-f2d9-4171-b5cc-fa4a589597d5)


### 2. Create a New VHD

- Click Action (top menu) → Create VHD.

![disk2](https://github.com/user-attachments/assets/e448bb5c-c84b-4fff-86f1-0da8fed39473)


### 3. Choose File Location & Size

- Click Browse and select where to save the VHD file (e.g, C:\new VHD.vhd)
- Set the size (e.g: 1GB)
- Choose VHD (Fixed Size) and Click OK

![disk3](https://github.com/user-attachments/assets/5c7ad16c-653a-4336-b6a4-9073e551f059)


### 4. Initialize the Disk
- In Disk Management, find your new disk (marked as "Not Initialized").

![disk4](https://github.com/user-attachments/assets/e11238fd-fc4d-4172-b1e6-62953e35625d)

- Right-click the disk → Click Initialize Disk.


![disk5](https://github.com/user-attachments/assets/057fe017-0b93-4c02-9113-6bb14770a4ae)


- Select MBR (Master Boot Record).

![disk6](https://github.com/user-attachments/assets/a22c12ec-2ad2-407b-9fb2-29e1a8a58bec)


### 6. Create & Format the Partition
- Right-click the Unallocated Space → Click New Simple Volume.

![disk7](https://github.com/user-attachments/assets/49976d36-5c05-48c0-a192-68b5aad1e6f8)

![disk8](https://github.com/user-attachments/assets/178181ce-e985-466d-a470-0cc55f05ab71)

![disk9](https://github.com/user-attachments/assets/494599df-8dd3-48c3-b6c2-312fab049d6b)


- Click Next → Click on Mount in the following empty NTFS folder → Browse → Assign a drive letter (e.g., C: or D:) → New folder → OK

![disk10](https://github.com/user-attachments/assets/1f29da14-0843-42e0-9a7a-4aaee6f7d3d1)

![disk12](https://github.com/user-attachments/assets/3f449e6f-a228-442f-a42b-357120509cea)


![disk11](https://github.com/user-attachments/assets/0b19b8f4-5add-4253-b4ef-d708106c4a5a)


Click next → Finish.
## Step 2: Add & Delete Files for Recovery
### 1. Copy Files to the Virtual Disk
- Open File Explorer → Go to the new drive (C: or D:), where the folder created in the previous step
- Create a new folder (TestFolder) and copy images or files into it.
### 2. Delete the Files
- Select any one or two images → Press Delete.
- Empty the Recycle Bin to permanently delete them.
## Step 3: Recover Deleted Files Using Autopsy
1. Open Autopsy & Create a New Case
- Launch Autopsy and Run as a administrator
- Click Create New Case.

![a1](https://github.com/user-attachments/assets/821f785a-6003-4de8-a552-643b4d95e10a)


- Enter a Case Name (e.g., Autopsy1).
- Choose a Case Folder location.
- Click Next → Click Finish.

![a2](https://github.com/user-attachments/assets/6dea0010-f136-4d89-9d41-602950688c6d)


### 2. Add the Virtual Disk as an Evidence Source
- Click Add Data Source → Select Host

![a3](https://github.com/user-attachments/assets/722c686a-29d9-4a1f-b053-4447c06297f9)


- Select Local Disk → next

![a4](https://github.com/user-attachments/assets/a6d62d11-e362-4596-a1ff-a030af4ec3d1)


- Select Disk → Choose the VHD drive (Drive1)

![a5](https://github.com/user-attachments/assets/7425f8e3-6e0c-4218-bf42-a139d936fd56)


- Click Next → Keep default settings → Click Finish.
- Wait for Autopsy to process the disk.
### 3. Recover Deleted Files
- Go to File Views (left panel).

![a6](https://github.com/user-attachments/assets/dd810271-2ca7-421b-a9bb-27acf92ec9d9)


- Click Deleted Files → Find your deleted images.
- Right-click an image → Click Extract File.

![a7](https://github.com/user-attachments/assets/1d86092d-1b2c-4ca8-982a-f8b264a5b3e5)

- Select a folder to see the recovered files (e.g., C:\image_recovery).
- Your deleted images are now recovered!

## Step 4: Delete the Virtual Disk (Optional Cleanup)
### 1. Detach the VHD
- Open Disk Management (Win + X → Disk Management).
- Find the virtual disk (C: or D:).
- Right-click the disk (not the partition) → Click Detach VHD.
### 2. Delete the VHD File
- Open File Explorer.
- Go to the location where you saved the .vhd file (e.g., C:\new VHD.vhd).
- Delete the .vhd file.
- Empty the Recycle Bin.
- Your virtual disk is completely removed!

## Result :
This guide covers creating a Virtual Hard Disk (VHD), adding, deleting, and recovering images using Autopsy, and safely deleting the virtual disk after the experiment.
