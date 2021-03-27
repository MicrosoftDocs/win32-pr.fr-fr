---
description: Affiche la boîte de dialogue Exécuter à l’utilisateur.
ms.assetid: BC7C4C26-593D-4467-A2AA-4F2DF835C989
title: Méthode IShellDispatch. FileRun (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FileRun
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 56806edf06d334d90ad038886d955c00876f8f0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753093"
---
# <a name="ishelldispatchfilerun-method"></a>Méthode IShellDispatch. FileRun

Affiche la boîte de dialogue **exécuter** à l’utilisateur.

## <a name="syntax"></a>Syntaxe


```JScript
IShellDispatch.FileRun()
```


```VB

IShellDispatch.FileRun()
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

### <a name="jscript"></a>JScript

Cette méthode ne retourne pas de valeur.

### <a name="vb"></a>VB

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. FileRun**](shell-filerun.md) .

## <a name="examples"></a>Exemples

Les exemples suivants illustrent l’utilisation de **FileRun** dans JScript, VBScript et Visual Basic.

Langage


```JScript
<script language="JScript">
    function fnShellFileRunJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FileRun();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellFileRunVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.FileRun

        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellFileRunVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FileRun

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



 

 




