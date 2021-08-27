---
description: La classe CTransInPlaceInputPin implémente une broche d’entrée qui est utilisée par la classe CTransInPlaceFilter.
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: CTransInPlaceInputPin, classe (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04d30b18d115e7ef03e88deb47355bafc795532a91afa14cf2f4392e658954f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076193"
---
# <a name="ctransinplaceinputpin-class"></a>CTransInPlaceInputPin, classe

![hiérarchie de la classe ctransinplaceinputpin](images/tsip01.png)

La `CTransInPlaceInputPin` classe implémente une broche d’entrée qui est utilisée par la classe [**CTransInPlaceFilter**](ctransinplacefilter.md) .

En règle générale, vous n’avez pas besoin de dériver de cette classe. Si vous le faites, vous devez substituer la méthode [**CTransInPlaceFilter :: GetPin**](ctransinplacefilter-getpin.md) du filtre pour créer des instances de votre classe dérivée.



| Variables membres protégées                                                          | Description                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**m \_ bReadOnly**](ctransinplaceinputpin-m-breadonly.md)                           | Indicateur qui spécifie si le flux d’entrée est en lecture seule. |
| [**m \_ pTIPFilter**](ctransinplaceinputpin-m-ptipfilter.md)                         | Pointeur vers le filtre qui a créé ce code confidentiel.               |
| M&#233;thodes publiques                                                                      | Description                                                |
| [**CTransInPlaceInputPin**](ctransinplaceinputpin-ctransinplaceinputpin.md)        | Méthode de constructeur.                                        |
| [**CheckMediaType**](ctransinplaceinputpin-checkmediatype.md)                      | Détermine si le code PIN accepte un type de média spécifique.       |
| [**PeekAllocator**](ctransinplaceinputpin-peekallocator.md)                        | Récupère un pointeur vers l’allocateur du pin.                |
| [**Seulement**](ctransinplaceinputpin-readonly.md)                                  | Indique si le flux d’entrée est en lecture seule.           |
| Méthodes IPin                                                                        | Description                                                |
| [**EnumMediaTypes**](ctransinplaceinputpin-enummediatypes.md)                      | Énumère les types de médias préférés du pin.                |
| Méthodes IMemInputPin                                                                | Description                                                |
| [**GetAllocator**](ctransinplaceinputpin-getallocator.md)                          | Récupère l’allocateur de mémoire proposé par ce code confidentiel.       |
| [**NotifyAllocator**](ctransinplaceinputpin-notifyallocator.md)                    | Spécifie un allocateur pour la connexion.                 |
| [**GetAllocatorRequirements**](ctransinplaceinputpin--getallocatorrequirements.md) | Récupère les propriétés d’allocateur demandées par le code confidentiel.   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




