---
description: Affiche la boîte de dialogue Propriétés de date et heure. Cette méthode a le même effet que de cliquer avec le bouton droit sur l’horloge dans la zone d’état de la barre des tâches et de sélectionner ajuster la date/l’heure.
ms.assetid: 01694607-3fc2-4d0d-ba48-5bdbb40da000
title: Shell. SetTime, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: cff10e89cfdc8ba038be2b619264c02b1c7b168d4ecb35cd625683f648121be6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452839"
---
# <a name="shellsettime-method"></a>Shell. SetTime, méthode

Affiche la boîte de dialogue **Propriétés de date et heure** . Cette méthode a le même effet que de cliquer avec le bouton droit sur l’horloge dans la zone d’état de la barre des tâches et de sélectionner **ajuster la date/l’heure**.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = Shell.SetTime()
```


```VB

Shell.SetTime() As Integer
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="examples"></a>Exemples

L’exemple suivant illustre la commande **setTime** en cours d’utilisation. l’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.SetTime();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.SetTime
 
        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.SetTime
 
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



 

 




