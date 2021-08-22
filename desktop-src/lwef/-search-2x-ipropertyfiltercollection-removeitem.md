---
title: IPropertyFilterCollection RemoveItem, propriété (WdsSharedIDL. h)
description: Supprime un filtre spécifique de la collection.
ms.assetid: a8b8a1f7-d47a-45dc-81c9-f01ecf6c1560
keywords:
- RemoveItem, propriété héritage Windows fonctionnalités d’environnement
- RemoveItem, propriété héritée Windows fonctionnalités d’environnement, interface IPropertyFilterCollection
- fonctionnalités d’environnement Windows héritées de l’interface IPropertyFilterCollection, propriété RemoveItem
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.RemoveItem
- IPropertyFilterCollection.put_RemoveItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54822e95e2ea7d6e10fdd5bbf833adb63b51cb01e8d860ce77f550432b41e926
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755418"
---
# <a name="ipropertyfiltercollectionremoveitem-property"></a>IPropertyFilterCollection :: RemoveItem, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

Supprime un filtre spécifique de la collection.

Cette propriété est en écriture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_RemoveItem(
  [in] long index
);
```



## <a name="property-value"></a>Valeur de la propriété

Accepte un pointeur vers l’index pour le filtre à supprimer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





