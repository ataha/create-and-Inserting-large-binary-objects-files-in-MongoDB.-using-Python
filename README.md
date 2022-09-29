# Create and store dummy large binary objects(e.g. files) in MongoDB using python

This script will generate a binary objects (e.g. files) containing random bytes and store those large files in MongoDB using python


# Prerequisites
The below python packages need to be installed.

pip install --user pymongo <br />
pip install --user gridfs <br />
pip install --user os

# How to use the python script:
modify the script with the preferred parameters/variables<br />
  <br />
  **client = MongoClient("mongodb://localhost:27017/", username='', password='')**  --> specify the host,port,username and password of mongodb<br />
  **database = ''**&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;--> The name of the Database. **test_database is the default value.** <br />
  **for numFile in range(10):**&emsp;&emsp;&emsp;&emsp;&emsp;--> How many files to be uploaded. **10 files is the default value.** <br />
  **newfile.write (os.urandom(500000000))**&emsp;--> generate 500MB random content. **file 1Mb is the default value.**
  
# Run the script:
```./create_store_files_monogodb.py```

# Expected output:
```
Connected successfully to Mongodb!
New File uploaded with Size 1 MegaBytes 
New File uploaded with Size 1 MegaBytes 
New File uploaded with Size 1 MegaBytes 
New File uploaded with Size 1 MegaBytes 
New File uploaded with Size 1 MegaBytes 
New File uploaded with Size 1 MegaBytes 
New File uploaded with Size 1 MegaBytes 
New File uploaded with Size 1 MegaBytes 
New File uploaded with Size 1 MegaBytes 
New File uploaded with Size 1 MegaBytes 
10 files are uploaded successfully
Total dataSize uploaded into DB test_database: 10 MegaBytes```
