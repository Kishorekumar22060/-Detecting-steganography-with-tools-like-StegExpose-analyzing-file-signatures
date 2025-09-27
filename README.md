# Detecting-steganography-with-tools-like-StegExpose-analyzing-file-signatures
## AIM:
To detect hidden data using steganography detection tools like StegExpose and analyze file signatures for authenticity and manipulation.
## Requirements:
- **Operating System:** Linux / Windows
- **Tools:**
    - StegExpose (Java-based tool)
    - Hex Editor (e.g., xxd, HxD)
    - File command (Linux) or TrID (Windows)
- **Sample files:**
    - Suspected stego files (.jpg, .png, .wav)
    - Clean reference files
## ARCHITECTURE DIAGRAM:
```mermaid
flowchart TD
    A[Input File: JPG/PNG/WAV] --> B[File Signature Analysis]
    B --> C{Signature Match?}
    C -- Yes --> D[Pass to StegExpose]
    C -- No --> E[File Tampered / Mismatch]
    D --> F[StegExpose Detection: Suspicious or Clean]
    F --> G[Report Findings]
```

## DESIGN STEPS:
### Step 1:
Install StegExpose or use the JAR version to detect steganography in image files.

### Step 2:
Run StegExpose on a directory of suspected image files using the command:

### Step 3:
Analyze file signatures using tools like file, binwalk, or xxd to check for inconsistencies or embedded content.

## PROGRAM:
**Check file type**
```bash
file suspect.jpg
```
or view magic bytes:
```
xxd suspect.jpg | head
```
**Run StegExpose**
```bash
java -jar StegExpose.jar suspect.jpg
```
## OUTPUT:
List of Images with Steganography Detection Scores and File Signature Details
### Install and Verify Steghide Tool
![image](https://github.com/user-attachments/assets/3719303e-1517-48f5-ab66-ee9cdf314759)

### Embed the Secret Message into the Image
![image](https://github.com/user-attachments/assets/079fa42c-9615-438c-b46e-e82644fd8659)

### Delete Original Secret File
![image](https://github.com/user-attachments/assets/ebb0e137-d5b4-4978-8c04-fc07c2a0ac96)

###  Extract the Hidden Secret from Image
![image](https://github.com/user-attachments/assets/44ab3d26-56c5-4845-b4d0-25e7aa1c857c)

### Verify the Extracted Message
![image](https://github.com/user-attachments/assets/9d67f14e-272a-4dc7-8963-ebe08d10527b)

### Retrieve Information About the Embedded Data
![image](https://github.com/user-attachments/assets/1d2ed2e9-59d5-4541-8319-66c0c0be82f6)

### Analyze File Signature
![image](https://github.com/user-attachments/assets/292fdad7-cd87-4c07-bd43-d7808ad7c509)

## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
