---
description: La méthode DecideBufferSize définit les exigences de la mémoire tampon.
ms.assetid: 1f7a3424-18ba-4a10-b09f-947ee8585ffa
title: Méthode CBaseOutputPin. DecideBufferSize (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dcb3328b56a7e203575a3abbaab64cda6a9b87f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526423"
---
# <a name="cbaseoutputpindecidebuffersize-method"></a>Méthode CBaseOutputPin. DecideBufferSize

La `DecideBufferSize` méthode définit les spécifications de la mémoire tampon.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAlloc* 
</dt> <dd>

Pointeur vers l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) de l’allocateur.

</dd> <dt>

*ppropInputRequest* 
</dt> <dd>

Pointeur vers une structure de [**\_ Propriétés Allocator**](/windows/win32/api/strmif/ns-strmif-allocator_properties) qui contient les exigences de mémoire tampon du code confidentiel d’entrée. Si la broche d’entrée n’a pas de spécifications, l’appelant doit zéro les membres de cette structure avant d’appeler la méthode.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.

## <a name="remarks"></a>Notes

Substituez cette méthode dans votre classe dérivée. Appelez la méthode [**IMemAllocator :: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) pour spécifier vos exigences en matière de mémoire tampon. En règle générale, la classe dérivée honore les exigences de mémoire tampon du pin d’entrée, mais elle n’est pas requise pour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseOutputPin, classe**](cbaseoutputpin.md)
</dt> </dl>

 

 




