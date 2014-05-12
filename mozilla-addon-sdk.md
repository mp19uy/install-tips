#### Problem

To develop with the Add-on SDK, you need to use Python 2.5, 2.6 or 2.7.  
Versions 3.x of Python are not supported on any platform.  
  
If you have installed Python 3.X , when running the command:  
``` source bin/activate ```  
you get an error regarding your version of Python.  
  
#### Solution  
  
You need to modify the `activate` script and the `cfx` script file and add the following line at the begining (they both are located at `addon-sdk/bin/`):  
```#!/usr/bin/env python2.7 ```  
and also at the end of the activate script, you need to replace `python` for `python2.7` in the line that says:  
``` python -c "from jetpack_sdk_env import welcome; welcome()" ```  
that means the last line of the activate script should look like this:  
``` python2.7 -c "from jetpack_sdk_env import welcome; welcome()" ```  
  
**NOTE**: This is, if you have installed Python 2.7 and want to use it, otherwise, replace with python2.5 or python2.6, depending which one you have installed and want to use.
