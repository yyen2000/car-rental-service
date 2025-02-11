# Extracting ZIP Files

This guide provides step-by-step instructions on how to extract a ZIP file using various methods.

## Prerequisites
- Ensure you have the ZIP file that needs to be extracted.
- Have an extraction tool installed (e.g., built-in system utility, WinRAR, 7-Zip, or command-line tools).

## Methods

### 1. Using File Explorer (Windows)
1. Locate the ZIP file in File Explorer.
2. Right-click the ZIP file and select `Extract All`.
3. Choose the destination folder.
4. Click `Extract` to begin the extraction process.

### 2. Using Terminal (Linux & macOS)
#### Linux:
```sh
unzip filename.zip -d /path/to/destination
```
#### macOS:
```sh
unzip filename.zip -d /Users/YourUsername/DestinationFolder
```

### 3. Using Command Prompt (Windows)
```sh
powershell Expand-Archive -Path "C:\path\to\file.zip" -DestinationPath "C:\path\to\destination"
```

### 4. Using Python Script
```python
import zipfile

def extract_zip(zip_path, extract_to):
    with zipfile.ZipFile(zip_path, 'r') as zip_ref:
        zip_ref.extractall(extract_to)

# Example usage
extract_zip("path/to/file.zip", "path/to/destination")
```

## Notes
- Ensure the destination folder has sufficient space.
- If the ZIP file is password-protected, use an appropriate tool that supports password input.
- For large ZIP files, extraction may take some time depending on system performance.

## Troubleshooting
- **Error: File is corrupted** → Try downloading the ZIP file again.
- **Error: Permission denied** → Run the extraction command with administrator/root privileges.
- **Error: Unsupported format** → Ensure the ZIP file is not another compressed format like `.rar` or `.tar.gz`.
