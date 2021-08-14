---
title: IPropertyFilterCollection, propriété AddItem (WdsSharedIDL. h)
description: Ajoute un nouveau filtre à la collection.
ms.assetid: 01078e7a-811a-4dfb-b122-4801f39413d8
keywords:
- propriété AddItem Windows fonctionnalités d’environnement héritées
- AddItem, propriété héritée Windows fonctionnalités d’environnement, interface IPropertyFilterCollection
- fonctionnalités d’environnement Windows héritées de l’interface IPropertyFilterCollection, propriété AddItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.AddItem
- IPropertyFilterCollection.get_AddItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeafec95549fefa244dff6ff44ad9110150ae1b410e38b423a0a31f09cf54194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755446"
---
# <a name="ipropertyfiltercollectionadditem-property"></a>IPropertyFilterCollection :: AddItem, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

Ajoute un nouveau filtre à la collection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_AddItem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a>Valeur de la propriété

retourne un pointeur vers l’adresse du nouveau filtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





