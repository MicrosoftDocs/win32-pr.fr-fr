---
description: La méthode SetProperties spécifie le nombre de mémoires tampons à allouer et la taille de chaque mémoire tampon.
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: CMemAllocator. SetProperties, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8505916245cca81fdd84132e4523fe9dd03b971b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526527"
---
# <a name="cmemallocatorsetproperties-method"></a>CMemAllocator. SetProperties, méthode

La `SetProperties` méthode spécifie le nombre de mémoires tampons à allouer et la taille de chaque mémoire tampon.

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

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                                 | Description                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                        | Opération réussie.<br/>                                                   |
| <dl> <dt>**\_pointeur E**</dt> </dl>                   | Argument de pointeur **null** .<br/>                                 |
| <dl> <dt>**VFW \_ E \_ déjà \_ validé**</dt> </dl>   | Impossible de modifier la mémoire allouée lorsque le filtre est actif.<br/> |
| <dl> <dt>**VFW \_ E \_ BADALIGN**</dt> </dl>             | Un alignement non valide a été spécifié.<br/>                        |
| <dl> <dt>**\_ \_ mémoires tampons VFW E en \_ suspens**</dt> </dl> | Une ou plusieurs mémoires tampons sont toujours actives.<br/>                      |



 

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CBaseAllocator :: SetProperties**](cbaseallocator-setproperties.md) .

L’alignement de la mémoire tampon, spécifié par le membre **cbAlign** de la structure de **\_ Propriétés Allocator** , doit être une puissance égale à deux.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMemAllocator, classe**](cmemallocator.md)
</dt> </dl>

 

 




