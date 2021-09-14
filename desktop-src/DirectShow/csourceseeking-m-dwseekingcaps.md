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
ms.openlocfilehash: e4addb06b120801b0d5e697c7df93ab8ba620bbd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296714"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceSeeking, classe**](csourceseeking.md)
</dt> </dl>

 

 




