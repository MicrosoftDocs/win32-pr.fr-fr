---
description: 'Méthode Shell. IsRestricted : récupère le paramètre de restriction d’un groupe à partir du Registre.'
ms.assetid: C4B3B5C0-7445-483a-885F-5283BD4D4B39
title: Shell. IsRestricted, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e428c914cf95d282fd721071009efc70fcb3a4d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412396"
---
# <a name="shellisrestricted-method"></a>Shell. IsRestricted, méthode

Récupère le paramètre de restriction d’un groupe à partir du Registre.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = Shell.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

Shell.IsRestricted( _
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

## <a name="return-value"></a>Valeur de retour

### <a name="jscript"></a>JScript

Type : **entier \***

Valeur de la restriction. Si la restriction spécifiée est introuvable, la valeur de retour est 0.

### <a name="vb"></a>VB

Type : **entier \***

Valeur de la restriction. Si la restriction spécifiée est introuvable, la valeur de retour est 0.

## <a name="remarks"></a>Notes

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

Les exemples suivants illustrent l’utilisation de **IsRestricted** pour récupérer la valeur de données de la restriction **undockwithoutlogon** à partir de la sous-clé **système** . l’utilisation est indiquée pour JScript et VBScript.

JScript :


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
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 
