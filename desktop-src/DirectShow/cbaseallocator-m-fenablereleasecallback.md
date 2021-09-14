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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010155"
---
# <a name="cbaseallocatorm_fenablereleasecallback-member"></a>CBaseAllocator :: m \_ fEnableReleaseCallback, membre

Indicateur qui spécifie si le rappel de mise en version est activé. Cet indicateur est défini dans la méthode du constructeur. Si la valeur est **false**, l’appel de la méthode [**CBaseAllocator :: SetNotify**](cbaseallocator-setnotify.md) provoque l’activation d’une assertion (dans les versions Debug).

## <a name="syntax"></a>Syntaxe


```C++
BOOL m_fEnableReleaseCallback;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




