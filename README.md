# windows-kernel-debugging-guide

## Setting up virtual machine

1. Enable kernel debugging
``` 
bcdedit /debug on

```
2. Set COM port
``` 
bcdedit /dbgsettings serial debugport:2 baudrate:115200
```

3. Turn off Firewall   

4. Install WDK Test Target. Can be copied from the following path on the host machine
```
C:\Program Files (x86)\Windows Kits\10\Remote\x64\WDK Test Target Setup x64-x64_en-us.msi
```
  
5. Set COM port for virtual machine

![COM port for virtual machine](./images/com_port_for_debugger.PNG)

## Setting up visual studio debugger

### Config kernel debug device

![COM port for virtual machine](./images/config_debug_device_1.PNG)

![COM port for virtual machine](./images/config_debug_device_2.PNG)

![COM port for virtual machine](./images/config_debug_device_3.PNG)

### Set new device as remote debugged machine

![COM port for virtual machine](./images/config_remote_kernel_host.PNG)


## Stert debugger session

1. Attach to remote kernel

![COM port for virtual machine](./images/attach_to_remote_kernel.PNG)

