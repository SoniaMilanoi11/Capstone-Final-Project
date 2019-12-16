# Capstone-Final-Project
Sonia Milanoi Capstone Project; Minerva Schools at KGI '20

## Instructions for Testing the Code Locally
In order to run this code locally, you will need to set up a local server. This code can not be run locally without setting up a local server because it contains asynchronous requests. Some browsers (including Chrome) will not run async requests (see Fetching data from the server) if you just run the example from a local file. This is because of security restrictions (for more on web security, read Website security).
To get around the problem of async requests, we need to test such examples by running them through a local web server. One of the easiest ways to do this for our purposes is to use Python's SimpleHTTPServer module.You can use several different approaches to creating a server, but I beieve the Pythonic approach is simplest, and since we are going to use Python within the tutorial, I decided on this as the best approach.

To do this:

Install Python. If you are using Linux or macOS, it should be available on your system already. If you are a Windows user, you can get an installer from the Python homepage and follow the instructions to install it:

Go to python.org
Under the Download section, click the link for Python "3.xxx".
At the bottom of the page, choose the Windows x86 executable installer and download it.
When it has downloaded, run it.
On the first installer page, make sure you check the "Add Python 3.xxx to PATH" checkbox.
Click Install, then click Close when the installation has finished.
Open your command prompt (Windows)/ terminal (macOS/ Linux). To check Python is installed, enter the following command:

  python -V
 
This should return a version number. If this is OK, navigate to the directory that your example is inside, using the cd command.

you can include the directory name to enter it, for example
cd Desktop
and you can use two dots to jump up one directory level if you need to
cd ..

Enter the command to start up the server in that directory:

If Python version returned above is 3.X
  python3 -m http.server
On windows try "python" instead of "python3"
If Python version returned above is 2.X
  python -m SimpleHTTPServer
  
By default, this will run the contents of the directory on a local web server, on port 8000. You can go to this server by going to the URL localhost:8000 in your web browser. Here you'll see the contents of the directory listed — click the HTML file you want to run.

  Important note: Note: If you already have something running on port 8000, you can choose another port by running the server command followed by an alternative port number, e.g. python3 -m http.server 7800 (Python 3.x) or python -m SimpleHTTPServer 7800 (Python 2.x). You can then access your content at localhost:7800.
  
To run the server side languages locally:
Python's SimpleHTTPServer (python 2.0) http.server (python 3.0) module is useful, but it doesn't know how to run code written in languages such as Python, PHP or JavaScript. To handle that you'll need something more — exactly what you'll need depends on the server-side language you are trying to run. Here are a few examples:

To run Python server-side code, you'll need to use a Python web framework. You can find out how to use the Django framework by reading Django Web Framework (Python). Flask is also a good (slightly less heavyweight) alternative to Django. To run this you'll need to install Python/PIP, then install Flask using pip3 install flask. At this point you should be able to run the Python Flask examples using for example python3 python-example.py, then navigating to localhost:5000 in your browser.


To run Node.js (JavaScript) server-side code, you'll need to use raw node or a framework built on top of it. Express is a good choice — see Express Web Framework (Node.js/JavaScript).
