<div align="center">

## Status Bar Message Fly


</div>

### Description

This code will make letters fly from the right to the left of the status bar, slowly creating a message. You can adjust the speed of how fast they go and what the message says.
 
### More Info
 
Will stop any text being showed in the status bar until the user has left the page.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[SeRkaL\_7](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/serkal-7.md)
**Level**          |Intermediate
**User Rating**    |4.8 (19 globes from 4 users)
**Compatibility**  |
**Category**       |[Browser/ System Services](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/browser-system-services__2-69.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/serkal-7-status-bar-message-fly__2-1800/archive/master.zip)





### Source Code

```
<Body
onload="timeout = window.setTimeout('setMessage()',500);">
<script language="JavaScript">
<!--
//Type the message you want to appear below
var startMsg = "Type message here";
var str   = "";
var msg   = "";
var leftMsg = "";
function setMessage()
{
  if (msg == "")
  {
    str = " ";
    msg = startMsg;
    leftMsg = "";
  }
  if (str.length == 1)
  {
    while (msg.substring(0, 1) == " ")
    {
      leftMsg = leftMsg + str;
      str = msg.substring(0, 1);
      msg = msg.substring(1, msg.length);
    }
    leftMsg = leftMsg + str;
    str = msg.substring(0, 1);
    msg = msg.substring(1, msg.length);
    for (var ii = 0; ii < 120; ii++)
    {
      str = " " + str;
    }
  }
  else
    str = str.substring(10, str.length);
  window.status = leftMsg + str;
  timeout = window.setTimeout('setMessage()',100);
}
// -->
</script>
```

