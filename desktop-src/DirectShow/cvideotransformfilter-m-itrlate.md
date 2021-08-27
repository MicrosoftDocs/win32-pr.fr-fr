---
description: Indique la date à laquelle les échantillons arrivent au convertisseur, en unités de temps de référence. Stockéesyntaxe.
ms.assetid: 7b30fbe1-5e57-4aa4-8e87-ddd584f186e4
title: 'Membre CVideoTransformFilter :: m_itrLate (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_itrLate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ba2d14d19849768538184e54de5ca84b9495371783d57231ab9ad6aa7738718
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075949"
---
# <a name="cvideotransformfilterm_itrlate-member"></a>CVideoTransformFilter :: m \_ itrLate, membre

Indique la date à laquelle les échantillons arrivent au convertisseur, en unités de temps de référence. Syntaxe

## <a name="syntax"></a>Syntaxe


```C++
int m_itrLate;
```



## <a name="remarks"></a>Notes

Lorsque le filtre reçoit un message de qualité en aval, il stocke la valeur de fin dans cette variable. Quand le filtre supprime des frames, il met à jour cette valeur en soustrayant la durée de chaque image.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Vtrans. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CVideoTransformFilter, classe**](cvideotransformfilter.md)
</dt> </dl>

 

 




