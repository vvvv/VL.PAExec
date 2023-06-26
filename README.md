# VL.PAExec
Set of nodes to execute [PAExec](https://www.poweradmin.com/paexec/) ([repo](https://github.com/poweradminllc/PAExec)).

## License
PAExec has its own very permissive [license](https://www.poweradmin.com/paexec/paexec_eula.txt).

## Troubleshooting
Getting PAExec to work can be a bit tricky. The following seem to be the most important settings to check on the target PC:

* Turn on `File and Printer Sharing`
* Check if `Remote Procedure Call (RPC)` is running (Services App).
* If executing commands remotely works, but is very slow (it should be instant!), try with all firewalls disabled
* If it doesn't work, you need to enable access to the Admin shares. Via regedit, set: HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\system\LocalAccountTokenFilterPolicy to 1 (DWORD32).
* If pslist.exe doesn't seem to work, it is likely that you have to [enable the Remote Registry Service](https://kb.paessler.com/en/topic/15543-how-do-i-enable-the-remote-registry-service-on-a-windows-pc)
