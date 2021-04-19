---
description: 'Indicateur qui spécifie si le rappel de mise en version est activé. Cet indicateur est défini dans la méthode du constructeur. Si la valeur est FALSe, l’appel de la méthode CBaseAllocator :: SetNotify provoque l’activation d’une assertion (dans les versions Debug).'
ms.assetid: cc9adc7c-ec44-41e7-875a-b3e553120804
title: 'Membre CBaseAllocator :: m_fEnableReleaseCallback (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fEnableReleaseCallback
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 626f1e8f4101eb48e79bc1cf679d1b91be9b2b31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541763"
---
# <a name="cbaseallocatorm_fenablereleasecallback-member"></a>CBaseAllocator :: m \_ fEnableReleaseCallback, membre

Indicateur qui spécifie si le rappel de mise en version est activé. Cet indicateur est défini dans la méthode du constructeur. Si la valeur est **false**, l’appel de la méthode [**CBaseAllocator :: SetNotify**](cbaseallocator-setnotify.md) provoque l’activation d’une assertion (dans les versions Debug).

## <a name="syntax"></a>Syntaxe


```C++
BOOL m_fEnableReleaseCallback;
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

 

 




