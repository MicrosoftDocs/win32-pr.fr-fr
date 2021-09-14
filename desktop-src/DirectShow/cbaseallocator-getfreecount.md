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
ms.openlocfilehash: a0538229053b5d47ca1bdc8f30b38a0937e36cb5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010169"
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

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette méthode implémente la méthode [**IMemAllocatorCallbackTemp :: GetFreeCount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) . L’Allocator n’expose pas l’interface IMemAllocatorCallbackTemp, sauf si l’indicateur *fEnableReleaseCallback* a la valeur **true** dans le constructeur CBaseAllocator.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




