<div align="center">

## How to compile a DLL for mIRC using Microsoft Visual C\+\+ 6\.0


</div>

### Description

Shows HOW to compile a mIRC DLL with Microsoft Visual C++ 6.0
 
### More Info
 
Please vote for me if you like the code. :-)


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Drat911](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/drat911.md)
**Level**          |Beginner
**User Rating**    |4.2 (21 globes from 5 users)
**Compatibility**  |C, Microsoft Visual C\+\+
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__3-1.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/drat911-how-to-compile-a-dll-for-mirc-using-microsoft-visual-c-6-0__3-3749/archive/master.zip)





### Source Code

```

mIRCDLL.c
Demonstrates how to compile a DLL for mIRC in MS Visual C 6.0
/* How to compile a DLL for mIRC using Microsoft Visual C++ 6.0
  by Drat911 (drat911@nwez.com)
  http://rm-f.net/~drat/
*/
#include <windows.h>
#include <stdio.h>
int __stdcall funcname(HWND mWnd, HWND aWnd, char *data, char *parms, BOOL show, BOOL nopause)
{
  /*
  How to execute a command:
  mIRC: $dll(testmirc.dll, funcname, _)
  Code:
  _snprintf(data, 900, "/echo -a The DLL worked!");
  return 2;
  *******
  How to return a value or text:
  mIRC: echo -a $dll(testmirc.dll, funcname, _)
  Code:
  _snprintf(data, 900, "Echo in action");
  return 3;
  */
}
/* You also need a .def file included in your "Source Files" containing
some info on the DLL. Mine looks like:
LIBRARY testmirc
DESCRIPTION "Example of using a DLL with mIRC"
EXPORTS
funcname
That's all, make sure you name it something.def and add it properly,
after that, it should compile fine and give you a .dll to work with.
*/
```

