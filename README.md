# Sandbox Detection Tool

## Overview
This tool detects sandbox environments or automated analysis systems by monitoring user input activity, such as keystrokes, mouse clicks, and double-clicks, using Windows API calls. It is designed to help identify suspicious activity patterns and avoid sandbox traps during runtime.

## Features
- Tracks the time elapsed since the last user input event.
- Detects and counts keystrokes, mouse clicks, and double-clicks.
- Exits when specific thresholds are reached, indicating potential sandbox detection.

## Requirements
- **Operating System**: Windows (mandatory)
- **Python Version**: 3.x

### Required Python Libraries
- `ctypes` (built-in)
- `win32api`
- `random`
- `sys`
- `time`

You can install the required library `win32api` by running:
```bash
pip install pywin32
```

## How to Run

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/SandboxDetectionTool.git
   cd SandboxDetectionTool
   ```

2. **Ensure You Are Using Windows**
   This script is designed to run exclusively on Windows. Running it on other operating systems will result in an error.

3. **Install Dependencies**
   Ensure Python and `pywin32` are installed:
   ```bash
   pip install pywin32
   ```

4. **Run the Script**
   Execute the script in a terminal:
   ```bash
   python sandbox_detect.py
   ```

5. **Expected Output**
   The script will:
   - Continuously print the time elapsed since the last input event.
   - Monitor user input for keystrokes, mouse clicks, and double-clicks.
   - Exit if thresholds indicating a sandbox environment are detected.

## Importance of This Tool
- **Sandbox Detection**: Identify if your application is being run in an automated analysis environment (sandbox).
- **Security**: Avoid triggering malicious behavior in environments designed to analyze such actions.
- **Research**: Understand patterns of user input and detect abnormal activity.

### Use Cases
1. **Malware Research**: Analyze the effectiveness of sandbox detection mechanisms.
2. **Red Teaming**: Test sandbox evasion tactics during assessments.
3. **Learning Tool**: Understand how sandboxes work and how user activity is monitored.

## Notes
- This tool is for **educational purposes only**. Use it responsibly and ethically.
- Always ensure you have proper permissions before running the script in any environment.

## Troubleshooting
- **ImportError for `ctypes.windll`**: Ensure the script is run on Windows. It will not work on Linux or macOS.
- **Missing Libraries**: Install `pywin32` as mentioned above.
- **Script Exits Immediately**: Check if the thresholds for sandbox detection are too low; adjust them as needed.

## Author
**Prakhar Verma**

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
