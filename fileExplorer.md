```python
import os, shutil
```


```python
path = r"C:/Users/tyson/Downloads/"
```


```python
file_name = os.listdir(path)
```


```python
# checking if path exists
folder_names = ['csv files', 'images', 'text', 'exe files']

#makes folders
for loop in range(0,4):
    if not os.path.exists(path + folder_names[loop]):
        os.makedirs((path + folder_names[loop]))
        
#moves files to appropriate folders        
for file in file_name:
    if ".csv" in file and not os.path.exists(path + "csv files/" + file):
        shutil.move(path + file, path + "csv files/" + file)
    if ".xlsx" in file and not os.path.exists(path + "csv files/" + file):
        shutil.move(path + file, path + "csv files/" + file)
    elif ".PNG" in file and not os.path.exists(path + "images/" + file):
        shutil.move(path + file, path + "images/" + file)
    elif ".png" in file and not os.path.exists(path + "images/" + file):
        shutil.move(path + file, path + "images/" + file)
    elif ".jpg" in file and not os.path.exists(path + "images/" + file):
        shutil.move(path + file, path + "images/" + file)
    elif ".pdf" in file and not os.path.exists(path + "text/" + file):
        shutil.move(path + file, path + "text/" + file)
    elif ".exe" in file and not os.path.exists(path + "exe files/" + file):
        shutil.move(path + file, path + "exe files/" + file)

        
    
```
