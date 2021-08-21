---
description: 'méthode IShellDispatch4. WindowsSecurity : affiche la boîte de dialogue Sécurité Windows.'
title: IShellDispatch4.WindowsSecurity, méthode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.WindowsSecurity
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 665c4644-7749-446e-8212-3ecc9901a035
ms.openlocfilehash: 8142867d8d0423729794460a077a0f7f12d97f5d9744a119571d3ddd2b90a592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720711"
---
# <a name="ishelldispatch4windowssecurity-method"></a>Méthode IShellDispatch4. WindowsSecurity

affiche la boîte de dialogue **Sécurité Windows** .

## <a name="syntax"></a>Syntaxe


```JScript
IShellDispatch4.WindowsSecurity()
```


```VB

IShellDispatch4.WindowsSecurity()
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

### <a name="jscript"></a>JScript

Cette méthode ne retourne pas de valeur.

### <a name="vb"></a>VB

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode affiche la boîte de dialogue qui s’affiche après avoir appuyé sur CTRL + ALT + SUPPR ou à l’aide de l’option sécurité dans le menu **Démarrer** .

> [!Note]  
> Cette méthode peut être utilisée uniquement lorsqu’elle est connectée par une session terminal à Microsoft Terminal Server.

 

## <a name="examples"></a>Exemples

les exemples suivants illustrent l’utilisation de **WindowsSecurity** pour JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.WindowsSecurity();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objshell.WindowsSecurity
        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objshell.WindowsSecurity
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



 

 




