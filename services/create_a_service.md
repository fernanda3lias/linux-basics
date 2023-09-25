<h1> How to create a linux service? </h1>

1. Create a service file
```
sudo nano /etc/systemd/system/FILE_NAME.service
```
1. Enable and start the service:
```
sudo systemctl enable FILE_NAME.service
sudo systemctl start FILE_NAME.service
```
3. Utilities
- Check the status:
```
sudo systemctl status FILE_NAME
```
- Restart:
```
sudo systemctl restart FILE_NAME
```
- Whenever you edit the .service file or the code file being executed (the one you define in ExecStart), run:
```
sudo systemctl daemon-reload and then restart the service.
```
4. Reminders
- In the ExecStart field, you should put the command you want to be executed, always with the full path to the files, like:
```
usr/bin/python /home/embeddo/code.py
```
- If you don't know the full path of a tool, just run:
```
which MODULE
```
- For example, if you run which python, it will return:
```
/usr/bin/python.
```
