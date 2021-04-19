---
description: Indicateur qui spécifie si l’objet fournit des exemples dans des lots exacts.
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: 'Membre COutputQueue :: m_bBatchExact (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bBatchExact
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5f38d8a0e7335025688f52015ff9ed4d4892820
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539991"
---
# <a name="coutputqueuem_bbatchexact-member"></a>COutputQueue :: m \_ bBatchExact, membre

Indicateur qui spécifie si l’objet fournit des exemples dans des lots exacts.

## <a name="syntax"></a>Syntaxe


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a>Notes

Si la valeur est **true**, l’objet attend jusqu’à ce qu’il dispose d’un lot complet d’exemples de supports avant d’en émettre un. Dans le cas contraire, il fournit des exemples à mesure qu’ils arrivent. La variable membre [**COutputQueue :: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md) définit la taille du lot.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COutputQueue, classe**](coutputqueue.md)
</dt> </dl>

 

 




