---
description: Exécute l’application du panneau de configuration ( \*.cpl) spécifiée.
title: Shell. ControlPanelItem, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 54979bbd-b36b-4b5b-a8a0-5f63e9526fa5
ms.openlocfilehash: 04d2493f5d0ec5b86d19689cb8e7c2a02a82e536
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196416"
---
# <a name="shellcontrolpanelitem-method"></a>Shell. ControlPanelItem, méthode

Exécute l’application du panneau de configuration ( \*.cpl) spécifiée. Si l’application est déjà ouverte, elle activera l’instance en cours d’exécution.

> [!Note]  
> à partir de Windows Vista, la plupart des applications du panneau de configuration sont des éléments de Shell et ne peuvent pas être ouvertes avec cette fonction. Pour ouvrir ces applications du panneau de configuration, transmettez le nom canonique à control.exe. Par exemple :
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a>Syntaxe


```JScript
Shell.ControlPanelItem(
  bstrDir
)
```


```VB

Shell.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrDir* \[ dans\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Nom de fichier de l’application du panneau de configuration. Toutes les applications du panneau de configuration ont l’extension .cpl.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

### <a name="jscript"></a>JScript

Cette méthode ne retourne pas de valeur.

### <a name="vb"></a>VB

Cette méthode ne retourne pas de valeur.

## <a name="examples"></a>Exemples

L’exemple suivant utilise **ControlPanelItem** pour exécuter l’élément des **propriétés d’affichage** du panneau de configuration. l’utilisation appropriée est indiquée pour JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ControlPanelItem("desk.cpl");
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 
