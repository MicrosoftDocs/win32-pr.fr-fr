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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484425"
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

Type : **DWORD \** _

Pointeur vers une valeur DWORD contenant des indicateurs de contrôle de vérification. L’indicateur _ *BROWSERPOLICY \_ non fiable \_ content** désactive toute possibilité de la préversion de l’exécution d’un script ou d’un ActiveX. Le paramètre *pdwFlags* ne doit pas être un pointeur **null** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

L’interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.

Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) et les API suivantes : les interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) et [**ISearchItem**](-search-isearchitem.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LinkType**](-search-linktype.md) .

L’utilisation de l’indicateur de **\_ \_ contenu non approuvé BROWSERPOLICY** est fortement recommandée pour désactiver toute possibilité de la version préliminaire de pouvoir exécuter un script ou un ActiveX. La méthode **IItemPreviewerExt :: SuggestBrowserPolicy** peut retourner des informations indiquant si l’aperçu de l’élément est approuvé ou non. Cela permet au contrôle d’affichage Trident d’exécuter le script, et même les contrôles ActiveX. Étant donné que le générateur d’aperçu utilise souvent des fichiers temporaires pour générer la version préliminaire, cela peut entraîner l’exécution d’un script et d’une exécution de code inattendus dans la zone de l’ordinateur local.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




