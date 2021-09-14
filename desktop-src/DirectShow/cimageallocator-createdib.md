---
description: La méthode CreateDIB crée une image bitmap indépendante du périphérique (DIB) GDI. Le DIB est alloué dans un bloc mempory partagé, ce qui élimine une opération de copie lorsque le filtre propriétaire BLITS l’image.
ms.assetid: 8a9ab1cf-4104-48e9-ba6c-28d0f1a1d226
title: Méthode CImageAllocator. CreateDIB (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateDIB
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 316b7aeadfa442a8df4e80075380464758f3c6bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119986"
---
# <a name="cimageallocatorcreatedib-method"></a>Méthode CImageAllocator. CreateDIB

La `CreateDIB` méthode crée une image bitmap indépendante du périphérique (DIB) GDI. Le DIB est alloué dans un bloc mempory partagé, ce qui élimine une opération de copie lorsque le filtre propriétaire BLITS l’image.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateDIB(
        LONG    InSize,
  [ref] DIBDATA &DibData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*InSIZE* 
</dt> <dd>

Taille de l’image bitmap.

</dd> <dt>

*DibData* \[ Réf\]
</dt> <dd>

Référence à une structure [**DIBDATA**](dibdata.md) . La méthode remplit cette structure avec des informations sur le DIB.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK en cas de réussite, ou un code d’erreur dans le cas contraire.

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

 

 




