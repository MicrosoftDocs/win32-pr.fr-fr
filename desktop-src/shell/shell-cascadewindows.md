---
description: Cascade toutes les fenêtres sur le bureau. Cette méthode a le même effet que le fait de cliquer avec le bouton droit sur la barre des tâches et de sélectionner cascade Windows.
ms.assetid: f73d2066-4626-455b-8ee6-f7004cc9e699
title: Shell. CascadeWindows, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CascadeWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fbff41f36d80a378202606b4c43cbf1b7b89dc3757ac821b88772312001ecb8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941799"
---
# <a name="shellcascadewindows-method"></a>Shell. CascadeWindows, méthode

Cascade toutes les fenêtres sur le bureau. Cette méthode a le même effet que le fait de cliquer avec le bouton droit sur la barre des tâches et de sélectionner **Cascade Windows**.

## <a name="syntax"></a>Syntaxe


```JScript
Shell.CascadeWindows()
```


```VB

Shell.CascadeWindows()
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

### <a name="jscript"></a>JScript

Cette méthode ne retourne pas de valeur.

### <a name="vb"></a>VB

Cette méthode ne retourne pas de valeur.

## <a name="examples"></a>Exemples

L’exemple suivant montre **CascadeWindows** en cours d’utilisation. l’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.CascadeWindows();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellCascadeWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.CascadeWindows
        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellCascadeWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.CascadeWindows
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 




