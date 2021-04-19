---
description: La \_ variable de membre m EndSample spécifie l’heure d’arrêt de l’exemple le plus récent.
ms.assetid: 694815b6-8da5-4174-b2c7-7d686a557c6c
title: 'Membre CDrawImage :: m_EndSample (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_EndSample
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78268e8335d6dd8c24497a9e4d74b0caab205a99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540317"
---
# <a name="cdrawimagem_endsample-member"></a>CDrawImage :: m \_ EndSample, membre

La `m_EndSample` variable membre spécifie l’heure d’arrêt de l’exemple le plus récent.

## <a name="syntax"></a>Syntaxe


```C++
CRefTime m_EndSample;
```



## <a name="remarks"></a>Notes

La valeur est valide uniquement à l’intérieur de la méthode [**CDrawImage ::D isplaysampletimes**](cdrawimage-displaysampletimes.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> </dl>

 

 




