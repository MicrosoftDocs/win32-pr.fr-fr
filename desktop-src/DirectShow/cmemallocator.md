---
description: Implémente un allocateur qui prend en charge l’interface IMemAllocator.
ms.assetid: c40eccef-d915-4bf3-81b2-b20e000718fb
title: CMemAllocator, classe (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bb94d5fae92d7494a4ac347591e9d571a7765d2be88072559fd74687eea87e97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915929"
---
# <a name="cmemallocator-class"></a>CMemAllocator, classe

![hiérarchie de la classe cmemallocator](images/filter10.png)

Implémente un allocateur qui prend en charge l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

Cette classe dérive de [**CBaseAllocator**](cbaseallocator.md). Pour plus d’informations sur les allocators, reportez-vous à la documentation de [**CBaseAllocator**](cbaseallocator.md).



| Variables membres protégées                              | Description                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [**m \_ pbuffer**](cmemallocator-m-pbuffer.md)           | Pointeur vers le bloc de mémoire qui contient les mémoires tampons.                   |
| Méthodes protégées                                       | Description                                                              |
| [**Gratuit**](cmemallocator-free.md)                      | Méthode d’espace réservé ; appelée pendant une opération de dévalidation.                  |
| [**ReallyFree**](cmemallocator-reallyfree.md)          | Libère la mémoire pour les mémoires tampons.                                     |
| [**Utilis**](cmemallocator-alloc.md)                    | Alloue de la mémoire pour les mémoires tampons.                                        |
| M&#233;thodes publiques                                          | Description                                                              |
| [**CMemAllocator**](cmemallocator-cmemallocator.md)    | Méthode de constructeur.                                                      |
| [**~ CMemAllocator**](cmemallocator--cmemallocator.md) | Méthode de destructeur.                                                       |
| [**CreateInstance**](cmemallocator-createinstance.md)  | Crée une nouvelle instance de la classe **CMemAllocator** .                   |
| Méthodes IMemAllocator                                   | Description                                                              |
| [**SetProperties**](cmemallocator-setproperties.md)    | Spécifie le nombre de mémoires tampons à allouer et la taille de chaque mémoire tampon. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fourniture d’un allocateur personnalisé](providing-a-custom-allocator.md)
</dt> </dl>

 

 




