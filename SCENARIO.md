## LIST THE FILES IN THE LIST OF FOLDERS

```
import os
folders = input("Please provide list of folders names with spaces in between:").split()

for folder in folders:
    try:
        files = os.listdir(folder)
    except FileNotFoundError:
        print("Please provide a valid folder name, looks like folder does not exist" + folder)
        continue
    except PermissionError:
        print("No access to this folder:" + folder)
        continue
    print(" === Listing files for the folder - " + folder)

    for file in files:
        print(file)
`
