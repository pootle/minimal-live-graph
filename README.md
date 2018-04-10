# minimal-live-graph
A small and simple live graphing web server


This demo plots live temperature from a raspberry pi on a very simple web page. It needs only 3 files and runs on a raspbian lite installation with no extra packages installed. 


The 3 files are:
- chartweb.py; a basic web server in 100 lines of python
- index.html; a very simple web page in 50 lines of html (of which 30 lines are embedded javascript)
- smoothie.js; the javascript from [smoothie on github](https://github.com/joewalnes/smoothie) that renders the live graph

## background
I wanted a small lightweight way to plot a live graph of data from my raspberry pi. I investigated a few javascript charting libraries, but they were often large cumbersome beasts that required installion of other large packages - usually node.js. 

Eventually I found [smoothie.js](https://github.com/joewalnes/smoothie) and thought it ideal for my purposes. It requires only a single freestanding .js file to be referenced from main web page; it is small, lightweight and easily embedded in a web page. It can also easily be run in a walled environment with no need for internet access. It is a great little package.

## installation and use
1. Start with a bare linux installation, such as raspbian lite or ubuntu or whatever. I haven't got a clue if it will work on windoze. Once logged into linux (I use ssh) and connected to a network.......
2. clone this repository, or just make a folder and put the 2 files chartweb.py and index.html in the folder
3. grab the file smoothie.js from this repo on github and put it in the same folder
4. from the command line, and in the folder with the 3 files:
   - 'python3 chartweb.py'
5. check / copy the url reported by the app
6. from a browser on a pc, phone or tablet on the same network, goto the url from 5.
