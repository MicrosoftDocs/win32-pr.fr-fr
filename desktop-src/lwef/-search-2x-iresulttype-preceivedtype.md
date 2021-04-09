---
title: IResultType PreceivedType, propriété (WdsSharedIDL. h)
description: Cette propriété contient la chaîne utilisée pour identifier le type dans l’index.
ms.assetid: 26d5f14c-162a-4ded-ac72-875561b8c977
keywords:
- Propriétés PreceivedType héritées fonctionnalités de l’environnement Windows
- Propriété PreceivedType fonctionnalités de l’environnement Windows héritées, interface IResultType
- Interface IResultType fonctionnalités d’environnement Windows héritées, propriété PreceivedType
topic_type:
- apiref
api_name:
- IResultType.PreceivedType
- IResultType.get_PreceivedType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b058105af254403c3b733f484d7c49a9ac5a0da3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843373"
---
# <a name="iresulttypepreceivedtype-property"></a>IResultType ::P propriété receivedType

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Cette propriété contient la chaîne utilisée pour identifier le type dans l’index.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_PreceivedType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valeur de la propriété

retourne l’adresse de la chaîne identifyint le type dans l’index.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





