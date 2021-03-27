---
description: Récupère le paramètre de restriction d’un groupe à partir du Registre.
ms.assetid: 04275c5f-c3ed-4962-882f-2cce0258a9f4
title: Méthode IShellDispatch2. IsRestricted (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f666a9ed3407d12eb9cf2c28ae062a9886d7a2cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972406"
---
# <a name="ishelldispatch2isrestricted-method"></a>Méthode IShellDispatch2. IsRestricted

Récupère le paramètre de restriction d’un groupe à partir du Registre.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = IShellDispatch2.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

IShellDispatch2.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*sGroup* \[ dans\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Chaîne** qui contient le nom du groupe. Cette valeur est le nom d’une sous-clé de Registre sous laquelle vérifier la restriction.

</dd> <dt>

*sRestriction* \[ dans\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Chaîne** qui contient la restriction dont la valeur doit être récupérée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

### <a name="jscript"></a>JScript

Type : **entier \** _

Valeur de la restriction. Si la restriction spécifiée est introuvable, la valeur de retour est 0.

### <a name="vb"></a>VB

Type : _*entier \**_

Valeur de la restriction. Si la restriction spécifiée est introuvable, la valeur de retour est 0.

## <a name="remarks"></a>Notes

Cette méthode est implémentée et accessible par le biais de la méthode [_ *Shell. IsRestricted* *](./shell-isrestricted.md) .

**IsRestricted** recherche d’abord un nom de sous-clé qui correspond à *sGroup* sous la clé suivante.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

Les restrictions sont déclarées en tant que valeurs des sous-clés de stratégie individuelles. Si la restriction nommée dans *sRestriction* se trouve dans la sous-clé nommée dans *sGroup*, **IsRestricted** retourne la valeur actuelle de la restriction. Si la restriction est introuvable sous **HKEY \_ local \_ machine**, la même sous-clé est vérifiée sous **HKEY \_ Current \_ User**.

Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.

## <a name="examples"></a>Exemples

Les exemples suivants illustrent l’utilisation de **IsRestricted** pour récupérer la valeur de données de la restriction **undockwithoutlogon** à partir de la sous-clé **système** . L’utilisation est indiquée pour JScript et VBScript.

Langage


```JScript
<script language="JScript">
    function fnIsRestricedJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var lReturn;
        
        lReturn = objShell.IsRestricted("system", "undockwithoutlogon");
        document.write(lReturn);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnIsRestricedVB()
        dim objShell
        dim lReturn

        set objShell = CreateObject("shell.application")

        lReturn = objShell.IsRestricted("system", "undockwithoutlogon")
        document.write(lReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 
