---
description: 'La méthode Alloc alloue de la mémoire pour les mémoires tampons. Cette méthode remplace la méthode CBaseAllocator :: Alloc.'
ms.assetid: 4a246b4e-93b3-4adb-9f10-6b92d9f479eb
title: CImageAllocator. Alloc, méthode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bdf4c36bcf66d46a5c5ee7df16ac04a4461bd3a88de91e175b81e89ce496e1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076239"
---
# <a name="cimageallocatoralloc-method"></a>CImageAllocator. Alloc, méthode

La `Alloc` méthode alloue de la mémoire pour les mémoires tampons. Cette méthode remplace la méthode [**CBaseAllocator :: Alloc**](cbaseallocator-alloc.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                                   | Description                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Succès<br/>             |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode est appelée par la méthode [**CBaseAllocator :: Commit**](cbaseallocator-commit.md) , lorsque le filtre valide l’allocateur.

Cette méthode crée une liste d’exemples de médias, qui sont implémentés en tant qu’objets [**CImageSample**](cimagesample.md) . Chaque exemple contient une image bitmap indépendante du périphérique GDI, à l’aide de la fonction GDI **CreateDIBSection** .

En interne, cette méthode appelle [**CImageAllocator :: CreateDIB**](cimageallocator-createdib.md) pour créer chaque DIB, et [**CImageAllocator :: CreateImageSample**](cimageallocator-createimagesample.md) pour créer chaque exemple.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageAllocator, classe**](cimageallocator.md)
</dt> </dl>

 

 




