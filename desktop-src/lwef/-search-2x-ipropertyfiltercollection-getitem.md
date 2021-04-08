---
title: IPropertyFilterCollection, propriété GetITem (WdsSharedIDL. h)
description: Retourne un filtre spécifique dans la collection.
ms.assetid: 72a35d98-b2d8-4dfb-84a7-365a3778fc85
keywords:
- Propriété GetITem fonctionnalités de l’environnement Windows héritées
- Propriété GetITem fonctionnalités de l’environnement Windows héritées, interface IPropertyFilterCollection
- Interface IPropertyFilterCollection fonctionnalités de l’environnement Windows héritées, propriété GetITem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.GetITem
- IPropertyFilterCollection.get_GetITem
- IPropertyFilterCollection.put_GetITem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8027bf175efc615c1324f55229c7e307a123c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941977"
---
# <a name="ipropertyfiltercollectiongetitem-property"></a>IPropertyFilterCollection :: GetITem, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Retourne un filtre spécifique dans la collection.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_GetITem(
  [in]          long            index
);

HRESULT get_GetITem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a>Valeur de la propriété

Définit l’adresse du filtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





