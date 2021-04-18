---
title: Propriété de l’indicateur IResultProperty (WdsSharedIDL. h)
description: Valeur spéciale utilisée pour faciliter la récupération de données.
ms.assetid: fa888c5e-898e-4f48-b87e-2d0d078fd1fe
keywords:
- Propriété d’indicateur fonctionnalités héritées de l’environnement Windows
- Propriété d’indicateur fonctionnalités héritées de l’environnement Windows, interface IResultProperty
- Interface IResultProperty fonctionnalités de l’environnement Windows héritées, propriété Hint
topic_type:
- apiref
api_name:
- IResultProperty.Hint
- IResultProperty.get_Hint
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3edfed528ab6a6833cced99c113c33e7e2f859d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512381"
---
# <a name="iresultpropertyhint-property"></a>IResultProperty :: Hint, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Valeur spéciale utilisée pour faciliter la récupération de données.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Hint(
  [out, retval] ling *hint
);
```



## <a name="property-value"></a>Valeur de la propriété

retourne un pointeur désignant l’indicateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





