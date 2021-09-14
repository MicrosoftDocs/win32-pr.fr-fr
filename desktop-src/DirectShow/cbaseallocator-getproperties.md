---
description: 'La méthode GetProperties récupère le nombre de mémoires tampons créées par l’allocateur, ainsi que les propriétés de la mémoire tampon. Cette méthode implémente la méthode IMemAllocator :: GetProperties.'
ms.assetid: ccee4d69-52fc-4e3c-b6a4-787914708be4
title: CBaseAllocator. GetProperties, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abf143b11b6dd67fca6c87f9a31ce69f18951311
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010170"
---
# <a name="cbaseallocatorgetproperties-method"></a>CBaseAllocator. GetProperties, méthode

La `GetProperties` méthode récupère le nombre de mémoires tampons créées par l’allocateur, ainsi que les propriétés de la mémoire tampon. Cette méthode implémente la méthode [**IMemAllocator :: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetProperties(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pProps* 
</dt> <dd>

Pointeur désignant une structure de [**\_ propriétés d’allocateur**](/windows/win32/api/strmif/ns-strmif-allocator_properties) qui reçoit les propriétés d’allocateur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




