---
description: Suggère la stratégie de sécurité à appliquer au navigateur.
ms.assetid: 73541611-2024-4c33-ab03-e3204244c46c
title: 'IItemPreviewerExt :: SuggestBrowserPolicy, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.SuggestBrowserPolicy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0a4f248edbfa4a1779016e40d73051d8c1d9acac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525432"
---
# <a name="iitempreviewerextsuggestbrowserpolicy-method"></a>IItemPreviewerExt :: SuggestBrowserPolicy, méthode

Suggère la stratégie de sécurité à appliquer au navigateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SuggestBrowserPolicy(
  [in]          DWORD dwContext,
  [out, retval] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwContext* \[ dans\]
</dt> <dd>

Type : **DWORD**

Identificateur de contexte de l’opération. Remplacez la valeur par défaut de *dwContext* pour définir l’identificateur de contexte sur la valeur de votre choix.

</dd> <dt>

*pdwFlags* \[ out, retval\]
</dt> <dd>

Type : **DWORD \***

Pointeur vers une valeur DWORD contenant des indicateurs de contrôle de vérification. L’indicateur de **\_ \_ contenu non approuvé BROWSERPOLICY** désactive toute possibilité d’exécution de l’aperçu de script ou de ActiveX. Le paramètre *pdwFlags* ne doit pas être un pointeur **null** .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

l’interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.

pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) et les api suivantes : les interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) et [**ISearchItem**](-search-isearchitem.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LINKTYPE**](-search-linktype.md) .

Il est fortement recommandé d’utiliser l’indicateur de **\_ \_ contenu non approuvé BROWSERPOLICY** pour désactiver toute possibilité d’exécution d’un script ou d’un ActiveX. La méthode **IItemPreviewerExt :: SuggestBrowserPolicy** peut retourner des informations indiquant si l’aperçu de l’élément est approuvé ou non. cela permet au contrôle de l’écran trident d’exécuter le script et même de ActiveX contrôles. Étant donné que le générateur d’aperçu utilise souvent des fichiers temporaires pour générer la version préliminaire, cela peut entraîner l’exécution d’un script et d’une exécution de code inattendus dans la zone de l’ordinateur local.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




