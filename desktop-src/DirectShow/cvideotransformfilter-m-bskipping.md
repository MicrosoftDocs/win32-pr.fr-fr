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
ms.openlocfilehash: 7beb4073052149e246a55ffbb1ff057e836704c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234204"
---
# <a name="cvideotransformfilterm_bskipping-member"></a>CVideoTransformFilter :: m \_ bSkipping, membre

Valeur booléenne qui indique si le filtre supprime actuellement des frames. Si cette valeur est **true**, le filtre continue à supprimer des frames jusqu’à ce qu’il atteigne l’image clé suivante, ou jusqu’à ce qu’il reçoive 30 images Delta dans une ligne sans image clé.

## <a name="syntax"></a>Syntaxe


```C++
BOOL m_bSkipping;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Vtrans. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CVideoTransformFilter, classe**](cvideotransformfilter.md)
</dt> </dl>

 

 




