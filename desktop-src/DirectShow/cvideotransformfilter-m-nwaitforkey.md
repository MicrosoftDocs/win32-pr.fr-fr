---
description: Nombre maximal actuel d’images Delta à supprimer.
ms.assetid: d14c594e-55ab-42c2-bdb0-6829f71d02dd
title: 'Membre CVideoTransformFilter :: m_nWaitForKey (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_nWaitForKey
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a168a26816825c33c0e047d93cc8b14ebd0f3536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532499"
---
# <a name="cvideotransformfilterm_nwaitforkey-member"></a>CVideoTransformFilter :: m \_ nWaitForKey, membre

Nombre maximal actuel d’images Delta à supprimer. Alors que cette variable est supérieure à zéro, le filtre supprime les frames jusqu’à ce qu’il atteigne une image clé. Pour chaque frame supprimé, le filtre décrémente cette variable d’une unité, ce qui empêche le filtre de supprimer un nombre excessif de frames. Après 30 images Delta dans une ligne sans images clés, le filtre recommence à fournir des frames.

## <a name="syntax"></a>Syntaxe


```C++
int m_nWaitForKey;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Vtrans. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CVideoTransformFilter, classe**](cvideotransformfilter.md)
</dt> </dl>

 

 




