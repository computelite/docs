(pythoneditor)=

# Python Editor

![Execute Python](../images/run_python.png)

Users can input Python code in a clean and intuitive editor and run by clicking on icon (highlighted in yellow). Upon execution, the output is displayed in a designated area.Python code execution leverages the Pyodide runtime for running Python in a web environment.

## Image Output

![Image Output](../images/img_output.png)

The user can also get the output as an image. To achieve this, additional code must be added to the existing code block. Below is an example:

```
# Sample code to display random dog images 
import urllib3, json, os,io
from pyodide.ffi import to_js

url = "https://random.dog/woof.json"
response  = urllib3.request("GET", url)
img_url = response.json()['url']

extension = ""

while extension not in ("JPEG", "PNG", "JPG", "GIF"):
  response  = urllib3.request("GET", url)
  img_url = response.json()['url']
  print(img_url)
  extension = img_url.split(".")[-1].upper()

response = urllib3.request("GET", img_url)

# Once the image response is retrieved, the following lines must be added to render the image:

buf = io.BytesIO(response.data)

to_js(buf.getvalue())

```
The user can also download the output by clicking on --icon (highlighted in yellow).

## Upload/Download Files

![Upload Zip File](../images/upload_zip.png)

Users can upload and download Python code files in a zip format by clicking on icons (highlighted in yellow); when a zip file is uploaded, it replaces the existing files by deleting them and creating new ones from the uploaded content.


## File Management

![File Management](../images/file_management.png)

Users can add or delete files and folders as needed using these icons (highlighted in yellow). Any changes made to the files are instantly reflected in the editor, ensuring a seamless workflow. All files are stored within the selected model, specifically in the **S_ExecutionFiles** table. This table can be accessed from **Setups** > **Code Files**.


## Add To Home Page

![Home](../images/add_home.png)

Users can add files from the Python editor to the homepage, allowing them to execute the file's code directly from the homepage. Once a file is added, it will appear under the **"Run"** dropdown menu on the homepage, displayed with the name specified at the time of addition.


## Load Package

If the user wants to add and use Python packages in their project, they can create a **requirements.txt** file in the root folder.This file allows the user to specify all the necessary packages for their project.

Users can use either pure Python packages or packages supported by Pyodide. A complete list of these packages can be found [Here](https://pyodide.org/en/stable/usage/packages-in-pyodide.html).

![Requirements](../images/requirements.png)

Additionally, if a required package is not included in Pyodide, users can create pyodide packages and upload wheel files from the home page and integrate them into their code seamlessly.

**Navigation**: **Model** > **Upload Package**

![Requirements](../images/upload_package.png)

All files are stored as blobs in the selected model, specifically in the **S_PackageWheels** table. This table can be accessed from **All Other** > **PackageWheels**.

In the requirements.txt file, the user should list all the package names line by line, avoiding spaces, commas, or specific version numbers. For example:

```
numpy
pandas
matplotlib

```
Once the packages are specified in requirements.txt, user can import and utilize them in the Python files where they are required. For example, if the user wants to use numpy in a file named script.py, they can do so like this:

```
import numpy as np

# Example usage
array = np.array([1, 2, 3])
print(array)

```