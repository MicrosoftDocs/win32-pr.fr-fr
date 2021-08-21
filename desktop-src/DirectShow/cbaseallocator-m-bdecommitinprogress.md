---
description: Indicateur spécifiant si une opération de dévalidation est en cours.
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: 'Membre CBaseAllocator :: m_bDecommitInProgress (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6d73514ffbe2b6e2430230e64ccfa9006809523a95cd3220ca078d4c4e40f41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017537"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a>CBaseAllocator :: m \_ bDecommitInProgress, membre

Indicateur spécifiant si une opération de dévalidation est en cours. La valeur est **true** après l’appel de la méthode [**CBaseAllocator ::D ecommit**](cbaseallocator-decommit.md) , mais avant la libération de toutes les mémoires tampons. Si la valeur est **true**, la méthode [**CBaseAllocator :: GetBuffer**](cbaseallocator-getbuffer.md) échoue. En outre, l’allocateur ne doit pas être supprimé tant que la valeur est **true**.

## <a name="syntax"></a>Syntaxe


```C++
BOOL m_bDecommitInProgress;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




