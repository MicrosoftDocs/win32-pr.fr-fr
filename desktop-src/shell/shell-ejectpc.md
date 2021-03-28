---
description: Éjecte l’ordinateur de sa station d’accueil. Cela revient à cliquer sur le menu Démarrer et à sélectionner éjecter le PC, si votre ordinateur prend en charge cette commande.
ms.assetid: eaba3dce-8fea-453f-90c2-4a9b5cb05ecc
title: Shell. EjectPC, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 355d75b2ffaca9c9f90e66fbc535333a84bfa45d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973326"
---
# <a name="shellejectpc-method"></a>Shell. EjectPC, méthode

Éjecte l’ordinateur de sa station d’accueil. Cela revient à cliquer sur le menu **Démarrer** et à sélectionner **éjecter le PC**, si votre ordinateur prend en charge cette commande.

## <a name="syntax"></a>Syntaxe


```JScript
Shell.EjectPC()
```


```VB

Shell.EjectPC()
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

### <a name="jscript"></a>JScript

Cette méthode ne retourne pas de valeur.

### <a name="vb"></a>VB

Cette méthode ne retourne pas de valeur.

## <a name="examples"></a>Exemples

L’exemple suivant montre **EjectPC** en cours d’utilisation. L’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.

Langage


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.EjectPC();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.EjectPC

        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.EjectPC

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



 

 




