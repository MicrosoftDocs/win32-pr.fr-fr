---
description: 'La méthode SetProperties spécifie le nombre de mémoires tampons à allouer et la taille de chaque mémoire tampon. Cette méthode remplace la méthode CBaseAllocator :: SetProperties.'
ms.assetid: 8d419432-a9a7-44fb-b916-8dacd08eb6ec
title: CImageAllocator. SetProperties, méthode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c04501fe3511d9cdd45f3513c68082d2ffece0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537999"
---
# <a name="cimageallocatorsetproperties-method"></a>CImageAllocator. SetProperties, méthode

La `SetProperties` méthode spécifie le nombre de mémoires tampons à allouer et la taille de chaque mémoire tampon. Cette méthode remplace la méthode [**CBaseAllocator :: SetProperties**](cbaseallocator-setproperties.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pRequest* 
</dt> <dd>

Pointeur vers une structure de [**\_ Propriétés Allocator**](/windows/win32/api/strmif/ns-strmif-allocator_properties) qui contient les exigences de mémoire tampon.

</dd> <dt>

*pActual* 
</dt> <dd>

Pointeur vers une structure de **\_ Propriétés Allocator** qui reçoit les propriétés de mémoire tampon réelles.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode appelle [**CImageAllocator :: CheckSizes**](cimageallocator-checksizes.md) pour valider la taille de mémoire tampon demandée. Il appelle également la version de classe de base de `SetProperties` .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageAllocator, classe**](cimageallocator.md)
</dt> </dl>

 

 




