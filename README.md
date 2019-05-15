# Debugging with Visual Studio Code, XDebug and Docker on Windows

1. Clone the repository: https://github.com/apparena/docker-init
```git
git clone https://github.com/tald7344
```

2. Open **Docker Debug** folder using vcode

3. Make sure that PHP Debug extension is installed, if not visit this site 
[debug php in vscode](https://www.codewall.co.uk/debug-php-in-vscode-with-xdebug/)

4. Open up the index.php file in src directory. On line 3, click to the left of the “3” and you should get a red dot. That’s a breakpoint.

5. Open a terminal window (View / Terminal) and run :
```docker
docker-compose up
```
