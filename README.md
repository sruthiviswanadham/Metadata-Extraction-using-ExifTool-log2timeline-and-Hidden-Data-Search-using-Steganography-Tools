## Metadata-Extraction-using-ExifTool-log2timeline-and-Hidden-Data-Search-using-Steganography-Tools

## AIM:
To extract metadata, perform timeline analysis, and search for hidden data using forensic tools like ExifTool, log2timeline, and steganography detection tools.

## DESIGN STEPS:
## Step 1:
Use exiftool to extract metadata from files such as images, documents, and videos.

## Step 2:
Use log2timeline and plaso to create and analyze event timelines from system logs and file metadata.

## Step 3:
Apply steganography detection tools like steghide, zsteg, or binwalk to uncover hidden data in media files.

## PROGRAM:
Metadata and Timeline Forensics, Steganography Analysis Steps

## OUTPUT:
## A. Using ExifTool – for file metadata
Install:
```
sudo apt update
sudo apt install exiftool -y
```
## Extract metadata from a file:
```
exiftool image.jpg
```
## Batch process a folder:
```
exiftool -r /path/to/folder
```
## Useful flags:

-G: Show metadata group

-time:all: Show only timestamps

-GPSLatitude -GPSLongitude: Extract GPS data
![image](https://github.com/user-attachments/assets/e3b1c8e6-7136-479c-b17b-002cef442a20)



## install log2timeline
```
sudo apt install plaso -y
```
```
sudo apt install steghide -y
```
## Embed data
```
steghide embed -cf /home/kali/Downloads/wallpaper.jpg -ef /home/kali/Downloads/secret.txt
```
![image](https://github.com/user-attachments/assets/82c9375b-8b94-4007-8c51-d59a01068c03)


## Extract hidden data:
```
steghide extract -sf hidden.jpg
```
![image](https://github.com/user-attachments/assets/42e48f90-ced6-434d-b6e5-f1f63e050532)


## Using binwalk – for file analysis
```
sudo apt install binwalk -y
binwalk suspicious.jpg
```
![image](https://github.com/user-attachments/assets/a9662fe0-862a-4fff-aaf0-70f698034315)


## RESULT:
Metadata was successfully extracted, timeline analysis was completed, and hidden data was identified using steganography tools.
