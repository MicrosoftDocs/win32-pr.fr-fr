---
description: 'Affiche la boîte de dialogue Rechercher : tous les fichiers. cela revient à cliquer sur le menu Démarrer puis à sélectionner rechercher (ou son équivalent dans les systèmes antérieurs à Windows XP).'
ms.assetid: cccdd3ea-b52a-4fbe-b4c5-1efc1dd6d770
title: Shell. FindFiles, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8c7295857509c19b06bed342508e0f0c5ee5aae42136edbe6035c6e256cdfb2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968578"
---
# <a name="shellfindfiles-method"></a>Shell. FindFiles, méthode

Affiche la boîte de dialogue **Rechercher : tous les fichiers** . cela revient à cliquer sur le menu **démarrer** , puis à sélectionner **rechercher** (ou son équivalent sous systèmes antérieurs à Windows XP).

## <a name="syntax"></a>Syntaxe


```JScript
Shell.FindFiles()
```


```VB

Shell.FindFiles()
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

### <a name="jscript"></a>JScript

Cette méthode ne retourne pas de valeur.

### <a name="vb"></a>VB

Cette méthode ne retourne pas de valeur.

## <a name="examples"></a>Exemples

L’exemple suivant montre **FindFiles** en cours d’utilisation. l’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Shell_FindFiles();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellFindFilesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.FindFiles

        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

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



 

 




