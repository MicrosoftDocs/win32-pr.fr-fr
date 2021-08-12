---
description: La \_ variable de membre m bModifiesData indique si le filtre modifie les exemples de données qui sont reçus. La valeur est définie dans le constructeur CTransInPlaceFilter, mais prend par défaut la valeur TRUE.
ms.assetid: 8ccdba46-315f-4519-b363-6870d1217f98
title: 'Membre CTransInPlaceFilter :: m_bModifiesData (Transip. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bModifiesData
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7461f7f62a6cbd1fea2ff18f6e8f2e4b73825ea04cb9e3b0a679ee7cf15fef90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654878"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a>CTransInPlaceFilter :: m \_ bModifiesData, membre

La `m_bModifiesData` variable membre indique si le filtre modifie les exemples de données qui sont reçus. La valeur est définie dans le constructeur **CTransInPlaceFilter** , mais prend par défaut la valeur **true**.

## <a name="syntax"></a>Syntaxe


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a>Notes

Cette variable affecte la manière dont le filtre négocie l’allocateur. Si la valeur est **true**, le filtre ne peut pas utiliser d’allocateur en lecture seule pour les deux connexions de code confidentiel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceFilter, classe**](ctransinplacefilter.md)
</dt> </dl>

 

 




