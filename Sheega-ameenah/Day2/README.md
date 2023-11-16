# 100 Days of Computer Vision - Day 2

## Error Encountered: ImportError - libGL.so.1: cannot open shared object file: No such file or directory

### Description:
During Day 2 of the 100 Days of Computer Vision streak, an `ImportError` occurred while working remotely using GitHub Codespaces. The error specifically mentioned the absence of the `libGL.so.1` library.

### Error Message:
```
ImportError: libGL.so.1: cannot open shared object file: No such file or directory
```

### Cause:
The error is related to missing graphical libraries required by OpenCV, and it commonly occurs in headless environments or systems without full graphical support.

### Solution:
To resolve the issue, the missing library needs to be installed. Use the following commands based on your system:

- **Ubuntu/Debian:**
  ```bash
  sudo apt-get install libgl1-mesa-glx
  ```

- **Red Hat/CentOS:**
  ```bash
  sudo yum install mesa-libGL
  ```

Alternatively, if graphical capabilities are not needed, you can install OpenCV without GUI support using:
```bash
pip install opencv-python-headless
```

Ensure that these commands are executed in your GitHub Codespaces environment. If you are using a virtual environment, make sure it is activated during the installation.

### Notes:
- If working on a headless system or a server, installing `opencv-python-headless` is a lightweight alternative that excludes unnecessary graphical dependencies.
- If the issue persists or if you encounter similar errors, consider checking the system's graphics capabilities and adjust OpenCV installation accordingly.
- Always document any specific steps or considerations for the Codespaces environment to help others following along with the 100 Days of Computer Vision streak.