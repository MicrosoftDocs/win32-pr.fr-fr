---
description: 'La méthode SetProperties spécifie le nombre de mémoires tampons à allouer et la taille de chaque mémoire tampon. Cette méthode implémente la méthode IMemAllocator :: SetProperties.'
ms.assetid: f53c22a4-c01d-4d2f-81f0-bedf8f2ae5f0
title: CBaseAllocator. SetProperties, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d81ee1c29f1c9e2cc9927f926144a7427b5e94f72406f94ce65f7d4a20e2ab32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057479"
---
# <a name="cbaseallocatorsetproperties-method"></a>CBaseAllocator. SetProperties, méthode

La `SetProperties` méthode spécifie le nombre de mémoires tampons à allouer et la taille de chaque mémoire tampon. Cette méthode implémente la méthode [**IMemAllocator :: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) .

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

Retourne l’une des valeurs **HRESULT** suivantes.



| Code de retour                                                                                                 | Description                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                        | Réussite.<br/>                                                   |
| <dl> <dt>**\_pointeur E**</dt> </dl>                   | Argument de pointeur **null** .<br/>                                 |
| <dl> <dt>**VFW \_ E \_ déjà \_ validé**</dt> </dl>   | Impossible de modifier la mémoire allouée lorsque le filtre est actif.<br/> |
| <dl> <dt>**VFW \_ E \_ BADALIGN**</dt> </dl>             | Un alignement non valide a été spécifié.<br/>                        |
| <dl> <dt>**\_ \_ mémoires tampons VFW E en \_ suspens**</dt> </dl> | Une ou plusieurs mémoires tampons sont toujours actives.<br/>                      |



 

## <a name="remarks"></a>Remarques

Cette méthode spécifie les spécifications de mémoire tampon, mais n’alloue pas de mémoire tampon. Appelez la méthode [**CBaseAllocator :: Commit**](cbaseallocator-commit.md) pour allouer des tampons.

L’appelant alloue deux structures de propriétés d’allocateur \_ . Le paramètre *pRequest* contient les exigences de mémoire tampon de l’appelant, y compris le nombre de mémoires tampons et la taille de chaque mémoire tampon. Lorsque la méthode est retournée, le paramètre *pActual* contient les propriétés de mémoire tampon réelles, telles qu’elles sont définies par l’allocateur. Dans la classe de base, en supposant que la méthode aboutisse, les propriétés réelles correspondent toujours aux propriétés demandées. Les classes dérivées peuvent substituer ce comportement.

L’allocateur ne doit pas être validé et ne doit pas avoir de tampons en suspens. Dans la classe de base, l’alignement doit être égal à 1. La classe [**CMemAllocator**](cmemallocator.md) remplace cette exigence.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




