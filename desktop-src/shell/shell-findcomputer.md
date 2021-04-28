---
Description : méthode Shell. FindComputer-affiche la boîte de dialogue résultats de la recherche : ordinateurs. La boîte de dialogue affiche le résultat de la recherche d’un ordinateur spécifié.
ms. AssetID : 0304b955-AFDE-4DE4-824a-9ec9c9530360 title : Shell. FindComputer, méthode (shldisp. h) ms. topic : référence ms. Date : 05/31/2018 topic_type : 
- APIRef
- api_name kbSyntax : 
- Api_type Shell. FindComputer : 
- Api_location COM : 
- Shell32.dll
---

# <a name="shellfindcomputer-method"></a>Shell. FindComputer, méthode

Affiche la boîte de dialogue résultats de la **recherche : ordinateurs** . La boîte de dialogue affiche le résultat de la recherche d’un ordinateur spécifié.

## <a name="syntax"></a>Syntaxe


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

### <a name="jscript"></a>JScript

Cette méthode ne retourne pas de valeur.

### <a name="vb"></a>VB

Cette méthode ne retourne pas de valeur.

## <a name="examples"></a>Exemples

L’exemple suivant montre **FindComputer** en cours d’utilisation. Le résultat de ce code est le même que si vous appuyez sur le bouton **Démarrer** , sur **Rechercher**, sur l’option **imprimantes, ordinateurs ou personnes** , puis sur **un ordinateur sur le réseau**. L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.

Langage


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
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
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

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



 

 




