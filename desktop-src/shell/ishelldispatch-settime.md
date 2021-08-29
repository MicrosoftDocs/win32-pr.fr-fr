---
description: Affiche la boîte de dialogue date et heure. Cette méthode a le même effet que de cliquer avec le bouton droit sur l’horloge dans la zone d’état de la barre des tâches et de sélectionner ajuster la date/l’heure.
ms.assetid: D4B949F6-5508-4624-9706-491184703DC6
title: IShellDispatch. SetTime, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b3505b618e8ca5d9f0f2415137247ac9a3edd53371c07dfe5ec92b7b6b502700
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714149"
---
# <a name="ishelldispatchsettime-method"></a>IShellDispatch. SetTime, méthode

Affiche la boîte de dialogue **date et heure** . Cette méthode a le même effet que de cliquer avec le bouton droit sur l’horloge dans la zone d’état de la barre des tâches et de sélectionner **ajuster la date/l’heure**.

## <a name="syntax"></a>Syntaxe


```JScript
IShellDispatch.SetTime()
```


```VB

IShellDispatch.SetTime()
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

### <a name="jscript"></a>JScript

Cette méthode ne retourne pas de valeur.

### <a name="vb"></a>VB

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. SetTime**](shell-settime.md) .

## <a name="examples"></a>Exemples

les exemples suivants illustrent l’utilisation de **SetTime** dans JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.SetTime();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.SetTime
 
        set objShell = nothing
    end function
```



Visual Basic :


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.SetTime
 
    Set objShell = Nothing
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 




