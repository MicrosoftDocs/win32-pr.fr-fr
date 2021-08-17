---
description: 'Méthode IShellDispatch2. ShowBrowserBar : affiche une barre de navigateur.'
ms.assetid: 5776370c-3bbf-449b-a8fe-2dbc7d89dd25
title: Méthode IShellDispatch2. ShowBrowserBar (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0b1380a44d2985b75e77dced43878c85e38d6a21b877fe06d9cdc7c10a8a2002
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090329"
---
# <a name="ishelldispatch2showbrowserbar-method"></a>Méthode IShellDispatch2. ShowBrowserBar

Affiche une barre de navigateur.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = IShellDispatch2.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

IShellDispatch2.ShowBrowserBar( _
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

Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. ShowBrowserBar**](./shell-showbrowserbar.md) .

Vous pouvez afficher l’une des barres d’exploration standard en définissant le paramètre *sCLSID* sur le CLSID de cette barre d’exploration. Les barres d’exploration standard et leurs chaînes CLSID sont les suivantes :



| Volet d’exploration | Chaîne CLSID                           |
|--------------|----------------------------------------|
| Favoris    | {EFA24E61-B078-11d0-89E4-00C04FC9E26E} |
| Dossiers      | {EFA24E64-B078-11d0-89E4-00C04FC9E26E} |
| Historique      | {EFA24E62-B078-11d0-89E4-00C04FC9E26E} |
| Rechercher       | {30D02401-6A81-11d0-8274-00C04FD5AE38} |



 

Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.

## <a name="examples"></a>Exemples

Les exemples suivants illustrent l’utilisation de **ShowBrowserBar** pour afficher la barre de navigateur **favoris** . l’utilisation est indiquée pour JScript et VBScript.

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



 

 
