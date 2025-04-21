# Parent PID spoofing
<a href="https://t.me/pulzetools"><img src="https://img.shields.io/badge/Join%20my%20Telegram%20group-2CA5E0?style=for-the-badge&logo=telegram&labelColor=db44ad&color=5e2775"></a>

- This is a simple method to bypass malicious behavior detections based on parent-child process relationship. Usually when an application starts another executable, the new process has a parent PID assigned which indicates the process that created it. This allows to detect and possibly block malicious intents like for example ```Word/Excel``` application starting ```Powershell```. This technique may be combined with for example process hollowing to achieve more stealth.

- The great thing is that ```CreateProcess``` API lets you provide additional information for process creation, including the one called ```PROC_THREAD_ATTRIBUTE_PARENT_PROCESS```. Let’s see how to use it - we will create a ```Notepad``` process in a way that it will look like it was spawned by ```explorer.exe```


## License
This project is licensed under the MIT License. See the LICENSE file for details.