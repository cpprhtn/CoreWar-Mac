# CoreWar-Mac
 


### Legacy Code  
This project is based on the legacy code from [Core War on SourceForge](https://sourceforge.net/projects/corewar/).  

### Running on M1 Mac  
To run the project on an M1 Mac, you need to set up an X11 environment by downloading [XQuartz](https://www.xquartz.org/).  

### Adjusting X11 Path  
After installing XQuartz, the X11 folder is typically located at a specific path. Make sure to update the path in the `Makefile` to match your environment.  

```
CFLAGS += -I/opt/X11/include
LIB += -L/opt/X11/lib -lX11
```

### Change Logs
- round  
The `round` function has been included in the `math.h` header since the C99 standard.  
To avoid conflicts with the legacy code's `round` variable, the variable name has been changed to `round_`.  

- sighandler  
The `sighandler` function is no longer available as a built-in function in C99 and later standards.  
As a result, any lines containing this function have been commented out.  