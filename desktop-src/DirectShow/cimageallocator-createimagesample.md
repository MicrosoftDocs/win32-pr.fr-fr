---
description: La méthode CreateImageSample crée un exemple de support.
ms.assetid: dae71692-5cbc-4bc7-a363-41766ef17c58
title: Méthode CImageAllocator. CreateImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57463a7025ea816b6fe6bcaa8b964231458903de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119982"
---
# <a name="cimageallocatorcreateimagesample-method"></a>Méthode CImageAllocator. CreateImageSample

La `CreateImageSample` méthode crée un exemple de support.

## <a name="syntax"></a>Syntaxe


```C++
virtual CImageSample* CreateImageSample(
   LPBYTE pData,
   LONG   Length
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pData* 
</dt> <dd>

Pointeur vers une mémoire tampon de *longueur* de taille, alloué par l’appelant.

</dd> <dt>

*Durée* 
</dt> <dd>

Longueur de la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne un objet [**CImageSample**](cimagesample.md) .

## <a name="remarks"></a>Notes

Cette méthode crée un nouvel exemple de support, implémenté comme un objet **CImageSample** . La méthode [**IMediaSample :: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) de l’exemple retourne un pointeur vers la mémoire tampon spécifiée dans le paramètre *pData* .

Si vous dérivez une nouvelle classe Allocator de [**CImageAllocator**](cimageallocator.md) et un nouvel exemple de classe de support à partir de [**CImageSample**](cimagesample.md), vous devez substituer cette méthode pour créer une instance de votre classe d’exemple de support.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageAllocator, classe**](cimageallocator.md)
</dt> <dt>

[**CImageAllocator :: Alloc**](cimageallocator-alloc.md)
</dt> </dl>

 

 




