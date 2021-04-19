---
description: Indicateur qui spécifie si les exigences de la mémoire tampon ont été modifiées.
ms.assetid: 34d946f9-125c-40fb-b09e-82457add07d6
title: 'Membre CBaseAllocator :: m_bChanged (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86c700f3c0ee820206613bcf3147652b1826b57a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531058"
---
# <a name="cbaseallocatorm_bchanged-member"></a>CBaseAllocator :: m \_ bChanged, membre

Indicateur qui spécifie si les exigences de la mémoire tampon ont été modifiées. La méthode [**CBaseAllocator :: SetProperties**](cbaseallocator-setproperties.md) définit la valeur sur **true**. Dans une classe dérivée, la méthode virtuelle pure [**CBaseAllocator :: Alloc**](cbaseallocator-alloc.md) doit rétablir la valeur **false**. Une fois que les tampons ont été alloués, il n’est pas nécessaire de les réallouer alors que *m \_ bChanged* a la **valeur false**.

## <a name="syntax"></a>Syntaxe


```C++
BOOL m_bChanged;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




