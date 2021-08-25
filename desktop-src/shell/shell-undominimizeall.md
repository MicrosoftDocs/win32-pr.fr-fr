---
description: Restaure toutes les fenêtres de bureau dans le même État que celui dans lequel elles se trouvaient avant la dernière commande MinimizeAll.
ms.assetid: dcedfa18-6dde-4fb8-9679-4d6ff80249e4
title: Shell. UndoMinimizeALL, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5e2342bda1059e2bcb00893afb182e415840a4e650392fc3e1d3df4756cb2d03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941569"
---
# <a name="shellundominimizeall-method"></a>Shell. UndoMinimizeALL, méthode

Restaure toutes les fenêtres de bureau dans le même État que celui dans lequel elles se trouvaient avant la dernière commande [**MinimizeAll**](shell-minimizeall.md) . cette méthode a le même effet que le fait de cliquer avec le bouton droit sur la barre des tâches et de sélectionner **annuler réduire tout Windows** sur les systèmes plus anciens ou un second clic sur l’icône **afficher le bureau** dans la zone lancement rapide de la barre des tâches de Windows 2000 ou Windows XP.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = Shell.UndoMinimizeALL()
```


```VB

Shell.UndoMinimizeALL() As Integer
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="examples"></a>Exemples

L’exemple suivant montre **UndoMinimizeALL** en cours d’utilisation. l’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.UndoMinimizeALL();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.UndoMinimizeALL

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



 

 




