---
description: 'La méthode Commit alloue la mémoire pour les mémoires tampons. Cette méthode implémente la méthode IMemAllocator :: Commit.'
ms.assetid: e8c36276-0229-428f-b030-978651ab7534
title: CBaseAllocator. Commit, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Commit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b49fae72e5588105b1235c1f0c461d5cc45cfa2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296858"
---
# <a name="cbaseallocatorcommit-method"></a>CBaseAllocator. Commit, méthode

La `Commit` méthode alloue la mémoire pour les mémoires tampons. Cette méthode implémente la méthode [**IMemAllocator :: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Commit();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                       | Description                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Réussite.<br/>                                |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | Les exigences de mémoire tampon n’ont pas été spécifiées.<br/> |



 

## <a name="remarks"></a>Notes

Avant d’appeler cette méthode, appelez la méthode [**CBaseAllocator :: SetProperties**](cbaseallocator-setproperties.md) pour spécifier les exigences en matière de mémoire tampon.

Cette méthode appelle la méthode virtuelle [**CBaseAllocator :: Alloc**](cbaseallocator-alloc.md) pour allouer la mémoire pour les mémoires tampons. Les classes dérivées peuvent substituer **Alloc**. Si une opération de dévalidation est en attente, elle est annulée.

Vous devez appeler cette méthode avant d’appeler la méthode [**CBaseAllocator :: GetBuffer**](cbaseallocator-getbuffer.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




