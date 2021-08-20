---
description: La classe CTransInPlaceOutputPin implémente une broche de sortie qui est utilisée par la classe CTransInPlaceFilter.
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: CTransInPlaceOutputPin, classe (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2462843f9ad42793a9e0666dd96aaf7387a1f5f0f1749f97cc4e2ca4d3ed051a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076152"
---
# <a name="ctransinplaceoutputpin-class"></a>CTransInPlaceOutputPin, classe

![hiérarchie de la classe ctransinplaceoutputpin](images/tsip02.png)

La `CTransInPlaceOutputPin` classe implémente une broche de sortie qui est utilisée par la classe [**CTransInPlaceFilter**](ctransinplacefilter.md) .

En règle générale, vous n’avez pas besoin de dériver de cette classe. Si vous le faites, vous devez substituer la méthode [**CTransInPlaceFilter :: GetPin**](ctransinplacefilter-getpin.md) du filtre pour créer des instances de votre classe dérivée.



| Variables membres protégées                                                      | Description                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [**m \_ pTIPFilter**](ctransinplaceoutputpin-m-ptipfilter.md)                    | Pointeur vers le filtre qui a créé ce code confidentiel.         |
| M&#233;thodes publiques                                                                  | Description                                          |
| [**CTransInPlaceOutputPin**](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | Méthode de constructeur.                                  |
| [**CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md)                 | Détermine si le code PIN accepte un type de média spécifique. |
| [**SetAllocator**](ctransinplaceoutputpin-setallocator.md)                     | Spécifie un allocateur pour la connexion.           |
| [**ConnectedIMemInputPin**](ctransinplaceoutputpin-connectedimeminputpin.md)   | Récupère un pointeur vers la broche d’entrée en aval.     |
| [**PeekAllocator**](ctransinplaceoutputpin-peekallocator.md)                   | Récupère un pointeur vers l’allocateur du pin.          |
| Méthodes IPin                                                                    | Description                                          |
| [**EnumMediaTypes**](ctransinplaceoutputpin-enummediatypes.md)                 | Énumère les types de médias préférés du pin.          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




