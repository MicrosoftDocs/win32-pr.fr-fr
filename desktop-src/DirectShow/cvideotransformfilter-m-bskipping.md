---
description: Valeur booléenne qui indique si le filtre supprime actuellement des frames. Si cette valeur est TRUE, le filtre continue à supprimer des frames jusqu’à ce qu’il atteigne l’image clé suivante, ou jusqu’à ce qu’il reçoive 30 images Delta dans une ligne sans image clé.
ms.assetid: 1af22879-bf9b-4835-b3b5-06fb52b3140f
title: 'Membre CVideoTransformFilter :: m_bSkipping (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSkipping
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f865bdc707b206a8528413a357a4e14bcfe88fff813e1f62a44d30e6f4843ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821914"
---
# <a name="cvideotransformfilterm_bskipping-member"></a>CVideoTransformFilter :: m \_ bSkipping, membre

Valeur booléenne qui indique si le filtre supprime actuellement des frames. Si cette valeur est **true**, le filtre continue à supprimer des frames jusqu’à ce qu’il atteigne l’image clé suivante, ou jusqu’à ce qu’il reçoive 30 images Delta dans une ligne sans image clé.

## <a name="syntax"></a>Syntaxe


```C++
BOOL m_bSkipping;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Vtrans. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CVideoTransformFilter, classe**](cvideotransformfilter.md)
</dt> </dl>

 

 




