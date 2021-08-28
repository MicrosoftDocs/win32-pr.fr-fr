---
description: La méthode GetFreeCount récupère le nombre d’exemples de supports qui ne sont pas utilisés.
ms.assetid: f4ce4cca-0168-42db-9fe7-858862f033a8
title: Méthode CBaseAllocator. GetFreeCount (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetFreeCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c4552829482a604b368a6710c62d0fc0b26a94aa3bb33b67ef386f2785d6c90e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057509"
---
# <a name="cbaseallocatorgetfreecount-method"></a>Méthode CBaseAllocator. GetFreeCount

La `GetFreeCount` méthode récupère le nombre d’exemples de supports qui ne sont pas en cours d’utilisation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetFreeCount(
   LONG *plBuffersFree
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*plBuffersFree* 
</dt> <dd>

Adresse d’une variable qui reçoit le nombre d’exemples qui ne sont pas en cours d’utilisation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Cette méthode implémente la méthode [**IMemAllocatorCallbackTemp :: GetFreeCount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) . L’Allocator n’expose pas l’interface IMemAllocatorCallbackTemp, sauf si l’indicateur *fEnableReleaseCallback* a la valeur **true** dans le constructeur CBaseAllocator.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




