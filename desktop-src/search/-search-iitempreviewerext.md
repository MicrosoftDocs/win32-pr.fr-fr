---
description: Fournit des méthodes pour fournir des paramètres de navigateur. L’interface IItemPreviewerExt est prise en charge uniquement sur Windows XP et Windows Server 2003 et ne doit plus être utilisée.
ms.assetid: d7d6cbb0-18bf-4e68-b7b4-307cadbced5c
title: Interface IItemPreviewerExt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt
api_type:
- COM
api_location: ''
ms.openlocfilehash: 820ddfdf73d36a7cba968a721872b1e9fb33a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951030"
---
# <a name="iitempreviewerext-interface"></a>Interface IItemPreviewerExt

Fournit des méthodes pour fournir des paramètres de navigateur. L’interface **IItemPreviewerExt** est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.

## <a name="members"></a>Membres

L’interface **IItemPreviewerExt** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IItemPreviewerExt** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IItemPreviewerExt** possède ces méthodes.



| Méthode                                                                               | Description                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md)               | Autorise l’extension à du contenu riche pour une propriété. <br/>                            |
| [**GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md)                   | Obtient une partie associée du corps pour l’incorporation dans le flux MHTML de sortie.<br/>              |
| [**ProcessTransformCommand**](-search-iitempreviewerext-processtransformcommand.md) | Autorise le traitement d’une commande de transformation rencontrée dans un modèle d’aperçu.<br/> |
| [**SuggestBrowserPolicy**](-search-iitempreviewerext-suggestbrowserpolicy.md)       | Suggère la stratégie de sécurité à appliquer au navigateur.<br/>                        |



 

## <a name="remarks"></a>Notes

L’interface **IItemPreviewerExt** est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.

Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface **IItemPreviewerExt** et les API suivantes : les interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) et [**ISearchItem**](-search-isearchitem.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LinkType**](-search-linktype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



 

 
