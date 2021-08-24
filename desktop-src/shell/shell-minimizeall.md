---
description: Réduit toutes les fenêtres sur le bureau.
ms.assetid: 3af98a16-27d1-4c93-ac72-7c9e24e68c23
title: Shell. MinimizeAll, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5daf7ef1b59d202851c91bfbc35b70c3836e62df7f00b5338063b98ee3b1eb80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709769"
---
# <a name="shellminimizeall-method"></a>Shell. MinimizeAll, méthode

Réduit toutes les fenêtres sur le bureau. cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et que vous sélectionnez **réduire tout Windows** sur les anciens systèmes ou si vous cliquez sur l’icône **afficher le bureau** dans la zone lancement rapide de la barre des tâches de Windows 2000 ou Windows XP.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = Shell.MinimizeAll()
```


```VB

Shell.MinimizeAll() As Integer
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="examples"></a>Exemples

L’exemple suivant montre **MinimizeAll** en cours d’utilisation. l’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.MinimizeAll();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.MinimizeAll

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



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Shell**](shell.md)
</dt> <dt>

[**UndoMinimizeALL**](shell-undominimizeall.md)
</dt> </dl>

 

 




