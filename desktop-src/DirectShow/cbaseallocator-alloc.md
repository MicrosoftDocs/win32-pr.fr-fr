---
description: 'Méthode CBaseAllocator. Alloc : la méthode Alloc alloue de la mémoire pour les mémoires tampons.'
ms.assetid: a22c97ef-6a8d-4cad-b5a5-3e6b225f5c81
title: CBaseAllocator. Alloc, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b53dc461a520b4e8c890a36fca6d73c2c836499f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094846"
---
# <a name="cbaseallocatoralloc-method"></a>CBaseAllocator. Alloc, méthode

La `Alloc` méthode alloue de la mémoire pour les mémoires tampons.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** suivantes.



| Code de retour                                                                                       | Description                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>           | Les exigences de mémoire tampon n’ont pas changé.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>              | Les exigences en matière de mémoire tampon ont changé.<br/>     |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | Les exigences de mémoire tampon n’ont pas été définies.<br/>     |



 

## <a name="remarks"></a>Notes

Cette méthode est appelée par la méthode [**CBaseAllocator :: Commit**](cbaseallocator-commit.md) .

Dans la classe de base, cette méthode n’alloue pas de mémoire. Elle retourne une erreur si les exigences de la mémoire tampon n’ont pas été définies, S \_ false si les spécifications n’ont pas été modifiées et s \_ OK si les spécifications ont été modifiées.

Une classe dérivée doit substituer cette méthode pour effectuer l’allocation de mémoire réelle. En règle générale, la classe dérivée effectue les étapes suivantes :

1.  Appelez l’implémentation de la classe de base pour déterminer si la mémoire doit être réellement allouée.
2.  Allouez de la mémoire.
3.  Créez les objets [**CMediaSample**](cmediasample.md) qui contiennent des blocs de mémoire de l’étape 2.
4.  Ajoutez chaque objet **CMediaSample** à la liste des exemples gratuits ([**CBaseAllocator :: m \_ lFree**](cbaseallocator-m-lfree.md)).

Pour obtenir un exemple, consultez [**CMemAllocator :: Alloc**](cmemallocator-alloc.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




