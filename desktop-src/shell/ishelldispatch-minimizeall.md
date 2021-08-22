---
description: Réduit toutes les fenêtres sur le bureau. cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et que vous sélectionnez réduire tout Windows sur les anciens systèmes ou si vous cliquez sur l’icône afficher le bureau dans la barre des tâches.
ms.assetid: 25DD56B0-221E-44a2-9FAD-FB358ADD7FF1
title: Méthode IShellDispatch. MinimizeAll (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 18f1256f93c9cd18d0c904f090716641b466e91319dbef323ee5107b802f82ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452984"
---
# <a name="ishelldispatchminimizeall-method"></a>Méthode IShellDispatch. MinimizeAll

Réduit toutes les fenêtres sur le bureau. cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et que vous sélectionnez **réduire tout Windows** sur les anciens systèmes ou si vous cliquez sur l’icône **afficher le bureau** dans la barre des tâches.

## <a name="syntax"></a>Syntaxe


```JScript
IShellDispatch.MinimizeAll()
```


```VB

IShellDispatch.MinimizeAll()
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

### <a name="jscript"></a>JScript

Cette méthode ne retourne pas de valeur.

### <a name="vb"></a>VB

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. MinimizeAll**](shell-minimizeall.md) .

## <a name="examples"></a>Exemples

les exemples suivants illustrent l’utilisation de **MinimizeAll** en cours d’utilisation pour JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.MinimizeAll();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.MinimizeAll

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

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**UndoMinimizeALL**](shell-undominimizeall.md)
</dt> </dl>

 

 




