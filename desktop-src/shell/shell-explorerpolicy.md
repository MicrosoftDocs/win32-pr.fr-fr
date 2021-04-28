---
description: Shell. ExplorerPolicy, méthode-obtient la valeur d’une stratégie Windows Internet Explorer spécifiée.
ms.assetid: 47E17F6A-ED43-44cd-AF77-A6E49865E1B5
title: Shell. ExplorerPolicy, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 765e1dc46edbe5a27292c5d8ff940e29b269f8dc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083697"
---
# <a name="shellexplorerpolicy-method"></a>Shell. ExplorerPolicy, méthode

Obtient la valeur pour une stratégie Windows Internet Explorer spécifiée.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Shell.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

Shell.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrPolicyName* \[ dans\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Chaîne** qui spécifie le nom de la stratégie.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

### <a name="jscript"></a>JScript

Type : **variante \***

Valeur associée au nom de stratégie spécifié.

### <a name="vb"></a>VB

Type : **variante \***

Valeur associée au nom de stratégie spécifié.

## <a name="remarks"></a>Notes 

Les administrateurs réseau peuvent contrôler et gérer l’environnement informatique de leurs utilisateurs en définissant des stratégies.

Le nom de la valeur spécifiée doit se trouver dans la **\_ \_** \\  \\  \\  \\  \\  \\ sous-clé de l'**Explorateur** de stratégies CurrentVersion de l’utilisateur actuel de HKEY Microsoft Windows. Si le nom de la valeur n’existe pas, la méthode retourne la valeur **null**.

## <a name="examples"></a>Exemples

Les exemples suivants illustrent l’utilisation correcte de **ExplorerPolicy** pour JScript, VBScript et Visual Basic.

Langage


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objShell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objShell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



Visual Basic :


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objShell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 6,0 ou ultérieure)</dt> </dl> |



 

 
