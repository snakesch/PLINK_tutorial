### **Windows**
1. **Using System Settings (Windows 10/11):**
   - Press the **Start** button and select **Settings**.
   - Go to **System** > **About**.
   - Look for the **System type** field under **Device specifications**, which will indicate whether your system is 32-bit or 64-bit.

2. **Using File Explorer:**
   - Open **File Explorer** (Windows Key + E).
   - Right-click on **This PC** or **My Computer** and select **Properties**.
   - In the System Properties window, check the **System type** field.

3. **Using Command Prompt:**
   - Open Command Prompt and type:  
     `WMIC os get osarchitecture`
   - Press Enter. The output will display "32-bit" or "64-bit".

### **Mac**
1. **Using About This Mac:**
   - Click the Apple menu and select **About This Mac**.
   - Check the processor information. If the processor is Intel Core 2 Duo or newer, it is 64-bit.

2. **Using Terminal:**
   - Open Terminal from Applications > Utilities.
   - Run the command:  
     `getconf LONG_BIT`  
     If the output is `64`, your system is 64-bit.

### **Linux (Ubuntu)**
1. **Using Terminal Commands:**
   - Open a terminal (`Ctrl` + `Alt` + `T`) and type:
     ```bash
     uname -m
     ```
     - If the output is `x86_64`, it’s a 64-bit system.
     - If it’s `i386`, `i686`, etc., it’s a 32-bit system.

2. Alternatively, run:
   ```bash
   dpkg --print-architecture
   ```
   This will display `amd64` for 64-bit or `i386` for 32-bit.
