---
Description : IShellDispatch. FindComputer, méthode-affiche la boîte de dialogue résultats de la recherche : ordinateurs. La boîte de dialogue affiche le résultat de la recherche d’un ordinateur spécifié.
ms. AssetID : 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 title : IShellDispatch. FindComputer, méthode (shldisp. h) ms. topic : référence ms. Date : 05/31/2018 topic_type : 
- APIRef
- api_name kbSyntax : 
- Api_type IShellDispatch. FindComputer : 
- Api_location COM : 
- Shell32.dll
---

# <a name="ishelldispatchfindcomputer-method"></a>Méthode IShellDispatch. FindComputer

Affiche la boîte de dialogue résultats de la **recherche : ordinateurs** . La boîte de dialogue affiche le résultat de la recherche d’un ordinateur spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

### <a name="jscript"></a>JScript

Cette méthode ne retourne pas de valeur.

### <a name="vb"></a>VB

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes 

Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. FindComputer**](shell-findcomputer.md) .

## <a name="examples"></a>Exemples

Les exemples suivants illustrent l’utilisation de **FindComputer** dans JScript, VBScript et Visual Basic.

Langage


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



VBScript


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 




