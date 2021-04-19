---
description: La \_ variable de membre m bUsingImageAllocator indique si l’allocateur de la connexion de code confidentiel est un objet CImageAllocator. Si la valeur est TRUE, l’allocateur est un objet CImageAllocator (ou est dérivé de cette classe).
ms.assetid: 8eddcab6-77b9-4c8f-be74-33e91661430d
title: 'Membre CDrawImage :: m_bUsingImageAllocator (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bUsingImageAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e08d1e8217f42c6855759cefeef40e56949156fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544030"
---
# <a name="cdrawimagem_busingimageallocator-member"></a>CDrawImage :: m \_ bUsingImageAllocator, membre

La `m_bUsingImageAllocator` variable membre indique si l’allocateur pour la connexion de code confidentiel est un objet **CImageAllocator** . Si la valeur est **true**, l’allocateur est un objet **CImageAllocator** (ou est dérivé de cette classe).

## <a name="syntax"></a>Syntaxe


```C++
BOOL m_bUsingImageAllocator;
```



## <a name="remarks"></a>Notes

Lorsque la valeur est **true**, l’objet **CDrawImage** peut utiliser les fonctions **GDI BitBlt** et **StretchBlt** pour restituer l’image, plutôt que les fonctions **SetDIBitsToDevice** et **StretchDIBits** plus lentes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::NotifyAllocator**](cdrawimage-notifyallocator.md)
</dt> <dt>

[**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




