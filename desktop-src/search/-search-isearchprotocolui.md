---
description: Fournit une méthode pour appeler des objets ISearchItem.
ms.assetid: b52fd64b-b03a-4d02-a64f-201f6b7d5045
title: Interface ISearchProtocolUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3923ddaff014d393690be31c0e0ca2be94a3cb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517460"
---
# <a name="isearchprotocolui-interface"></a>Interface ISearchProtocolUI

Fournit une méthode pour appeler des objets [**ISearchItem**](-search-isearchitem.md) . Les méthodes de cette interface sont appelées par l’hôte de protocole lors du traitement des URL à partir du Rassembleur. Le gestionnaire de protocole implémente le protocole d’accès à une source de contenu dans son format natif, et cette interface implémente un gestionnaire de protocole personnalisé pour développer les sources de données qui peuvent être indexées.

## <a name="members"></a>Membres

L’interface **ISearchProtocolUI** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISearchProtocolUI** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ISearchProtocolUI** possède ces méthodes.



| Méthode                                                                       | Description                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSearchItemForUrl**](-search-isearchprotocolui-getsearchitemforurl.md) | Obtient l’élément de recherche pour les données spécifiées. Cette méthode est appelée une fois pour chaque URL traitée par le rassembleur et récupère un pointeur vers l’objet [**ISearchItem**](-search-isearchitem.md) . <br/> |



 

## <a name="remarks"></a>Notes

L’interface **ISearchProtocolUI** est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.

Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface **ISearchProtocolUI** et les API suivantes : les interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) et [**ISearchItem**](-search-isearchitem.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LinkType**](-search-linktype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>          |



 

 
