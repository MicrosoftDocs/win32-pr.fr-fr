---
description: 'Méthode IShellDispatch. Windows : crée et retourne un objet ShellWindows. Cet objet représente une collection de toutes les fenêtres ouvertes qui appartiennent au shell.'
ms.assetid: 788E2106-3534-4e22-801F-677FD02BDFE0
title: Méthode IShellDispatch. Windows (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 16991d6a251909e8f3b277894a96e6ad08a7f9a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117167"
---
# <a name="ishelldispatchwindows-method"></a>IShellDispatch. Windows, méthode

Crée et retourne un objet [**ShellWindows**](shellwindows.md) . Cet objet représente une collection de toutes les fenêtres ouvertes qui appartiennent au shell.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = IShellDispatch.Windows()
```


```VB

IShellDispatch.Windows() As IDispatch
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

### <a name="jscript"></a>JScript

Type : **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***

Référence d’objet à l’objet [**ShellWindows**](shellwindows.md) .

### <a name="vb"></a>VB

Type : **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***

Référence d’objet à l’objet [**ShellWindows**](shellwindows.md) .

## <a name="remarks"></a>Notes 

Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. Windows**](shell-windows.md) .

## <a name="examples"></a>Exemples

Les exemples suivants utilisent **Windows** pour récupérer l’objet [**ShellWindows**](shellwindows.md) et afficher le nombre d’éléments qu’il contient. L’utilisation est indiquée pour JScript, VBScript et Visual Basic.

Langage


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();

        if (objShellWindows != null)
        {
            alert(objShellWindows.Count);
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellWindowsVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows

        if (not objShellWindows is nothing) then
            alert(objShellWindows.Count)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
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



 

 
