---
title: IPropertyFilterCollection, propriété AddItem (WdsSharedIDL. h)
description: Ajoute un nouveau filtre à la collection.
ms.assetid: 01078e7a-811a-4dfb-b122-4801f39413d8
keywords:
- AddItem, propriété fonctionnalités d’environnement Windows héritées
- AddItem, propriété fonctionnalités de l’environnement Windows héritées, interface IPropertyFilterCollection
- Interface IPropertyFilterCollection fonctionnalités de l’environnement Windows héritées, propriété AddItem
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
ms.openlocfilehash: b199f0e696f75fb5549b274ac888989f7a723b48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032716"
---
# <a name="ipropertyfiltercollectionadditem-property"></a>IPropertyFilterCollection :: AddItem, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

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
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





