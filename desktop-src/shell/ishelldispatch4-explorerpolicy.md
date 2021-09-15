---
description: 'méthode IShellDispatch4. ExplorerPolicy : obtient la valeur d’une Windows spécifiée dans la stratégie Internet Explorer.'
ms.assetid: 490c3e18-b606-456a-9016-dc4f7bad2bc3
title: Méthode IShellDispatch4. ExplorerPolicy (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4a03d61905bdb1f2b16de11cc604625d8e71a7ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412461"
---
# <a name="ishelldispatch4explorerpolicy-method"></a>Méthode IShellDispatch4. ExplorerPolicy

obtient la valeur d’une Windows de stratégie Internet Explorer spécifiée.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = IShellDispatch4.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

IShellDispatch4.ExplorerPolicy( _
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

## <a name="return-value"></a>Valeur de retour

### <a name="jscript"></a>JScript

Type : **variante \***

Valeur associée au nom de stratégie spécifié.

### <a name="vb"></a>VB

Type : **variante \***

Valeur associée au nom de stratégie spécifié.

## <a name="remarks"></a>Notes

Les administrateurs réseau peuvent contrôler et gérer l’environnement informatique de leurs utilisateurs en définissant des stratégies.

le nom de la valeur spécifiée doit se trouver dans la sous-clé **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **policies** \\ **Explorer** . Si le nom de la valeur n’existe pas, la méthode retourne la valeur **null**.

## <a name="examples"></a>Exemples

les exemples suivants illustrent l’utilisation correcte de **ExplorerPolicy** pour JScript, VBScript et Visual Basic.

JScript :


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objshell.ExplorerPolicy("ValueName");
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
            vReturn = objshell.ExplorerPolicy("ValueName")
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
        vReturn = objshell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 6,0 ou ultérieure)</dt> </dl> |



 

 
