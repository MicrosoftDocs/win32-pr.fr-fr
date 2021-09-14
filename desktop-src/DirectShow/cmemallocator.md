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
ms.openlocfilehash: 5adf390b7abf8fcbdb017ecde04bde76bf4bc001
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296747"
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



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fourniture d’un allocateur personnalisé](providing-a-custom-allocator.md)
</dt> </dl>

 

 




