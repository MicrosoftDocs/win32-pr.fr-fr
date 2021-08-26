---
description: Fonctionnalités de recherche.
ms.assetid: c849db20-7567-41e0-9a57-85070a6e6a3a
title: 'Membre CSourceSeeking :: m_dwSeekingCaps (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwSeekingCaps
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98044f8a05c22022f66e6014be591d99ec57451e33e8f2d7d464e6793bec19e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054029"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a>CSourceSeeking :: m \_ dwSeekingCaps, membre

Fonctionnalités de recherche.

## <a name="syntax"></a>Syntaxe


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a>Notes

Par défaut, la valeur est définie sur la combinaison d’opérations de bits des indicateurs suivants :

-   \_Recherche de \_ CanSeekForwards
-   \_Recherche de \_ CanSeekBackwards
-   \_Recherche de \_ CanSeekAbsolute
-   \_Recherche de \_ CanGetStopPos
-   \_Recherche de \_ CanGetDuration

Si le filtre prend en charge un ensemble de fonctionnalités différent, remplacez cette valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




