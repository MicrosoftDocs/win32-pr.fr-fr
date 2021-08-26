---
description: Shell. ShowBrowserBar, méthode-affiche une barre de navigateur.
ms.assetid: 203636D2-54D3-4163-B9AC-39213D6F4203
title: Shell. ShowBrowserBar, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 21bafde8c148ea8249672dd26a244dec152ed0e9fc5ce5fbb769e5cae6c92b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008889"
---
# <a name="shellshowbrowserbar-method"></a>Shell. ShowBrowserBar, méthode

Affiche une barre de navigateur.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Shell.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

Shell.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*sCLSID* \[ dans\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Chaîne** qui contient le format de chaîne du CLSID de la barre de navigateur à afficher. L’objet doit être inscrit en tant qu’objet de barre d’explorateur avec une \_ catégorie de composant INFOBAND CATID. Pour plus d’informations, consultez [création de barres d’exploration personnalisées, de bandes d’outils et de bandes de bureau](band-objects.md).

</dd> <dt>

*vShow* \[ dans\]
</dt> <dd>

Type : **variante**

Affectez la valeur **true** pour afficher la barre de navigateur ou **false** pour la masquer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

### <a name="jscript"></a>JScript

Type : **variante \***

Retourne la **valeur true** en cas de réussite ; Sinon, **false**.

### <a name="vb"></a>VB

Type : **variante \***

Retourne la **valeur true** en cas de réussite ; Sinon, **false**.

## <a name="remarks"></a>Remarques

Vous pouvez afficher l’une des barres d’exploration standard en définissant le paramètre *sCLSID* sur le CLSID de cette barre d’exploration. Les barres d’exploration standard et leurs chaînes CLSID sont les suivantes :



| Volet d’exploration | Chaîne CLSID                           |
|--------------|----------------------------------------|
| Favoris    | {EFA24E61-B078-11d0-89E4-00C04FC9E26E} |
| Dossiers      | {EFA24E64-B078-11d0-89E4-00C04FC9E26E} |
| Historique      | {EFA24E62-B078-11d0-89E4-00C04FC9E26E} |
| Recherche       | {30D02401-6A81-11d0-8274-00C04FD5AE38} |



 

Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.

## <a name="examples"></a>Exemples

Les exemples suivants illustrent l’utilisation de **Shell. ShowBrowserBar** pour afficher la barre de navigateur **favoris** . l’utilisation est indiquée pour JScript et VBScript.

JScript :


```JScript
<script language="JavaScript">
    function fnShowBrowserBarJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShowBrowserBarVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 
