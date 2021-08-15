---
description: en savoir plus sur la méthode IShellDispatch. RefreshMenu, qui actualise le contenu du menu Démarrer. utilisé uniquement avec les systèmes précédents Windows XP.
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
title: Méthode IShellDispatch. RefreshMenu (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ac5bb37f5880011fcabcfcc0e923196857694012a547b0391326a9fe5d8424f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969058"
---
# <a name="ishelldispatchrefreshmenu-method"></a>Méthode IShellDispatch. RefreshMenu

Actualise le contenu du menu **Démarrer** . utilisé uniquement avec les systèmes précédents Windows XP.

## <a name="syntax"></a>Syntaxe


```JScript
IShellDispatch.RefreshMenu()
```


```VB

IShellDispatch.RefreshMenu()
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

### <a name="jscript"></a>JScript

Cette méthode ne retourne pas de valeur.

### <a name="vb"></a>VB

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. TrayProperties**](shell-trayproperties.md) .

la fonctionnalité fournie par **RefreshMenu** est gérée automatiquement sous Windows XP ou version ultérieure. n’appelez pas cette méthode sur Windows XP ou version ultérieure.

## <a name="examples"></a>Exemples

les exemples suivants illustrent l’utilisation de **RefreshMenu** dans JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.RefreshMenu

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



 

 




