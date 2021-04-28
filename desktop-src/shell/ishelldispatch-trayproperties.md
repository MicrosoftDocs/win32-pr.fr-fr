---
description: 'Méthode IShellDispatch. TrayProperties : affiche la boîte de dialogue Propriétés de la barre des tâches et du menu Démarrer. Cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et sélectionnez Propriétés.'
ms.assetid: 8E0AC08E-1132-4312-9B75-E7686B91AB02
title: Méthode IShellDispatch. TrayProperties (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 424d25d7555090e4244d5cd22084171ca2a4fea9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086617"
---
# <a name="ishelldispatchtrayproperties-method"></a>Méthode IShellDispatch. TrayProperties

Affiche la boîte de dialogue **Propriétés de la barre des tâches et du menu Démarrer** . Cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et sélectionnez **Propriétés**.

## <a name="syntax"></a>Syntaxe


```JScript
IShellDispatch.TrayProperties()
```


```VB

IShellDispatch.TrayProperties()
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

### <a name="jscript"></a>JScript

Cette méthode ne retourne pas de valeur.

### <a name="vb"></a>VB

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes 

Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. TrayProperties**](shell-trayproperties.md) .

## <a name="examples"></a>Exemples

Les exemples suivants illustrent l’utilisation de **TrayProperties** dans JScript, VBScript et Visual Basic.

Langage


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TrayProperties();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 




