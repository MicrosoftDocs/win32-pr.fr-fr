---
title: Propriété UID IResultType (WdsSharedIDL. h)
description: Cette propriété contient l’identificateur unique pour le type.
ms.assetid: 31c2ef7d-f5a7-441e-80ea-fd7e46fded07
keywords:
- Propriété UID fonctionnalités d’environnement Windows héritées
- Propriété UID fonctionnalités d’environnement Windows héritées, interface IResultType
- Interface IResultType fonctionnalités d’environnement Windows héritées, propriété UID
topic_type:
- apiref
api_name:
- IResultType.UID
- IResultType.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbdd5a9b17da9cde04ac0b371a885b07415d0e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106303"
---
# <a name="iresulttypeuid-property"></a>IResultType :: UID, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Cette propriété contient l’identificateur unique pour le type.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a>Valeur de la propriété

adresse de l’emplacement contenant l’UID.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





