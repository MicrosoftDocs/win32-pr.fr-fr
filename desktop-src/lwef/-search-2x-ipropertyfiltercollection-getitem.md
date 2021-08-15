---
title: IPropertyFilterCollection, propriété GetITem (WdsSharedIDL. h)
description: Retourne un filtre spécifique dans la collection.
ms.assetid: 72a35d98-b2d8-4dfb-84a7-365a3778fc85
keywords:
- fonctions de l’environnement Windows hérité de la propriété GetITem
- propriété GetITem héritée Windows fonctionnalités d’environnement, interface IPropertyFilterCollection
- fonctionnalités d’environnement Windows héritées de l’interface IPropertyFilterCollection, propriété GetITem
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
ms.openlocfilehash: 7436e1fe10c26621f3cf4480be7db9710f80906bea18084a2e775e563db4dd8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451081"
---
# <a name="ipropertyfiltercollectiongetitem-property"></a>IPropertyFilterCollection :: GetITem, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

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
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





