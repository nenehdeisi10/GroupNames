# GroupNames
Func _GetLocalGroupName($sSID = 'S-1-5-18')     $objWMIService = ObjGet ("winmgmts:\\" &amp; @ComputerName &amp; "\root\cimv2")     $colItems = $objWMIService.ExecQuery('SELECT Name FROM Win32_Group where SID="' &amp; $sSID &amp; '"')     For $GroupNames in $colItems         MsgBox (0,"",$GroupNames.Name)         ExitLoop     Next EndFunc
