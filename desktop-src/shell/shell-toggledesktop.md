---
description: 'Méthode Shell. ToggleDesktop : affiche ou masque le bureau.'
title: Shell.ToggleDesktop, méthode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ToggleDesktop
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: BD07F7F2-A588-4189-95F4-3A8E2905E8F5
ms.openlocfilehash: 2007b133e6ef13ab4c4284ddff8486307c5beb6e0450b067699a0f6316df8d7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968508"
---
# <a name="shelltoggledesktop-method"></a>Shell. ToggleDesktop, méthode

Affiche ou masque le bureau.

## <a name="syntax"></a>Syntaxe


```JScript
Shell.ToggleDesktop()
```


```VB

Shell.ToggleDesktop()
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

### <a name="jscript"></a>JScript

Cette méthode ne retourne pas de valeur.

### <a name="vb"></a>VB

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode a le même effet que le bouton **afficher le bureau** sur la barre des tâches. Il masque toutes les fenêtres ouvertes pour afficher le bureau ou masque le bureau en affichant toutes les fenêtres ouvertes. La méthode **ToggleDesktop** n’affiche pas d’interface utilisateur, elle appelle simplement l’action bascule.

## <a name="examples"></a>Exemples

les exemples suivants illustrent l’utilisation correcte de **ToggleDesktop** pour JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnIShellDispatch4ToggleDesktopVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objShell.ToggleDesktop
        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 6,0 ou ultérieure)</dt> </dl> |



 

 




