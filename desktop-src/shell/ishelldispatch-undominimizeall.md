---
description: Restaure toutes les fenêtres de bureau à l’État où elles se trouvaient avant la dernière commande MinimizeAll.
ms.assetid: 32BDE544-C4FF-4a64-99AF-F8960AEC4690
title: Méthode IShellDispatch. UndoMinimizeALL (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1b11fdd7a0a82a11baa20b0f3a63a31a8a46b701
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527333"
---
# <a name="ishelldispatchundominimizeall-method"></a>Méthode IShellDispatch. UndoMinimizeALL

Restaure toutes les fenêtres de bureau à l’État où elles se trouvaient avant la dernière commande [**MinimizeAll**](shell-minimizeall.md) . Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner **Annuler réduire toutes les fenêtres** (sur les systèmes plus anciens) ou un second clic sur l’icône **afficher le bureau** dans la barre des tâches.

## <a name="syntax"></a>Syntaxe


```JScript
IShellDispatch.UndoMinimizeALL()
```


```VB

IShellDispatch.UndoMinimizeALL()
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

### <a name="jscript"></a>JScript

Cette méthode ne retourne pas de valeur.

### <a name="vb"></a>VB

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. UndoMinimizeAll**](./shell-undominimizeall.md) .

## <a name="examples"></a>Exemples

Les exemples suivants illustrent l’utilisation de **UndoMinimizeALL** dans JScript, VBScript et Visual Basic.

Langage


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.UndoMinimizeALL();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.UndoMinimizeALL

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 
