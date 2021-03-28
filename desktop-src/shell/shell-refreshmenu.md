---
description: Actualise le contenu du menu Démarrer. Utilisé uniquement avec les systèmes antérieurs à Windows XP.
ms.assetid: 1269c66d-61df-432d-9220-5ac975e3ad58
title: Shell. RefreshMenu, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a5812312c846026f4e0c7d2a4f6a5f857a572a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973255"
---
# <a name="shellrefreshmenu-method"></a>Shell. RefreshMenu, méthode

Actualise le contenu du menu **Démarrer** . Utilisé uniquement avec les systèmes antérieurs à Windows XP.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = Shell.RefreshMenu()
```


```VB

Shell.RefreshMenu() As Integer
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="remarks"></a>Notes

La fonctionnalité fournie par **RefreshMenu** est gérée automatiquement sous Windows XP ou version ultérieure. N’appelez pas cette méthode sous ce système d’exploitation.

## <a name="examples"></a>Exemples

L’exemple suivant montre **RefreshMenu** en cours d’utilisation. L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.

Langage


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.RefreshMenu();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.RefreshMenu

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



 

 




