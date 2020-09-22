<div align="center">

## RadCheck\! list of Checkboxes that acts like Radio Buttons with Select Highliting\!


</div>

### Description

Just started Learning JavaScript Yesterday.. Don't know how elegant this code is, but it works!.

It allows you to use Checkboxes instead of radio buttons but.

especially useful in long listings is the highliting which clearly shows the row that the user selects..
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[bmgx](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/bmgx.md)
**Level**          |Beginner
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |
**Category**       |[Controls/ Forms/ Graphics/ Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/controls-forms-graphics-menus__2-59.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/bmgx-radcheck-list-of-checkboxes-that-acts-like-radio-buttons-with-select-highliting__2-3385/archive/master.zip)





### Source Code

```
<html>
<head>
	<title>RadCheck! Checkbox that acts like Radio Button with Select Highliting</title>
<style>
table{font: 12px verdana;}
td{border:1px solid powderblue;}
</style>
<script language="javascript">
function Highlight($objId,$id)
{
	//unselect other checkbox's
	for(i=0;i<(document.form1.rad_id.length);i++)
	{
		if(document.form1.rad_id[i].id!=$objId)
		{
			document.form1.rad_id[i].checked=false;
			var row_id = "row"+(document.form1.rad_id[i].value);
			document.getElementById(row_id).style.background="transparent";
		}
	}
	//When checkbox is checked(TRUE) change background to blue
	if(document.getElementById($objId).checked==true)
	{
		document.getElementById($id).style.background="skyblue";
	}
	//When checkbox is UNchecked(FALSE) Restore Defaults
		else if(document.getElementById($objId).checked==false)
		{
			document.getElementById($id).style.background="transparent";
		}
}
</script>
</head>
<body>
<form name="form1" method="post" action="">
	<table align="left" cellpadding="0" cellspacing="1" border="0" width="100">
	<tr id="row1">
		<td width="25">
		<input type="checkbox" id="obj1" onclick='Highlight("obj1","row1")' name="rad_id" value="1">one
		</td>
	</tr>
	<tr id="row2">
		<td width="25">
		<input type="checkbox" id="obj2" onclick='Highlight("obj2","row2")' name="rad_id" value="2">two
		</td>
	</tr>
	<tr id="row3">
		<td width="25">
		<input type="checkbox" id="obj3" onclick='Highlight("obj3","row3")' name="rad_id" value="3">three
		</td>
	</tr>
	<tr id="row4">
		<td width="25">
		<input type="checkbox" id="obj4" onclick='Highlight("obj4","row4")' name="rad_id" value="4">four
		</td>
	</tr>
	<tr id="row5">
		<td width="25">
		<input type="checkbox" id="obj5" onclick='Highlight("obj5","row5")' name="rad_id" value="5">five
		</td>
	</tr>
	</table>
</form>
</body>
</html>
```

