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
ms.openlocfilehash: 7acd13e2d2d09e6e491a2f338aef2fe7564b82b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545551"
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



 

## <a name="remarks"></a>Notes

Cette méthode est appelée par la méthode [**CBaseAllocator :: Commit**](cbaseallocator-commit.md) , lorsque le filtre valide l’allocateur.

Cette méthode crée une liste d’exemples de médias, qui sont implémentés en tant qu’objets [**CImageSample**](cimagesample.md) . Chaque exemple contient une image bitmap indépendante du périphérique GDI, à l’aide de la fonction GDI **CreateDIBSection** .

En interne, cette méthode appelle [**CImageAllocator :: CreateDIB**](cimageallocator-createdib.md) pour créer chaque DIB, et [**CImageAllocator :: CreateImageSample**](cimageallocator-createimagesample.md) pour créer chaque exemple.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImageAllocator, classe**](cimageallocator.md)
</dt> </dl>

 

 




