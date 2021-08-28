---
description: La classe CTransformInputPin implémente une broche d’entrée qui est utilisée par la classe CTransformFilter.
ms.assetid: 032da1bb-448d-48ea-ab3d-f721d790637f
title: CTransformInputPin, classe (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3df5da0ee6e80dd1da147563ef698a520222531de5cee9656ec52cb14301f66e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087012"
---
# <a name="ctransforminputpin-class"></a>CTransformInputPin, classe

![hiérarchie de la classe ctransforminputpin](images/tfrm01.png)

La `CTransformInputPin` classe implémente une broche d’entrée qui est utilisée par la classe [**CTransformFilter**](ctransformfilter.md) .

En règle générale, vous n’avez pas besoin de dériver de cette classe. La plupart des méthodes de cette classe appellent les méthodes correspondantes sur la classe **CTransformFilter** , que vous pouvez substituer. Si vous dérivez de cette classe, vous devez substituer la méthode [**CTransformFilter :: GetPin**](ctransformfilter-getpin.md) du filtre pour créer des instances de votre classe dérivée.



| Variables membres protégées                                           | Description                                                                            |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ pTransformFilter**](ctransforminputpin-m-ptransformfilter.md) | Pointeur désignant le filtre propriétaire.                                                          |
| M&#233;thodes publiques                                                       | Description                                                                            |
| [**CTransformInputPin**](ctransforminputpin-ctransforminputpin.md)  | Méthode de constructeur.                                                                    |
| [**CheckConnect**](ctransforminputpin-checkconnect.md)              | Détermine si une connexion de code confidentiel est appropriée.                                       |
| [**BreakConnect**](ctransforminputpin-breakconnect.md)              | Libère le code confidentiel d’une connexion.                                                    |
| [**CompleteConnect**](ctransforminputpin-completeconnect.md)        | Termine une connexion à un autre code confidentiel.                                                 |
| [**CheckMediaType**](ctransforminputpin-checkmediatype.md)          | Détermine si le code PIN accepte un type de média spécifique.                                   |
| [**SetMediaType**](ctransforminputpin-setmediatype.md)              | Définit le type de média pour la connexion.                                                |
| [**CheckStreaming**](ctransforminputpin-checkstreaming.md)          | Détermine si le code confidentiel peut accepter des exemples. Virtuels.                                |
| [**CurrentMediaType**](ctransforminputpin-currentmediatype.md)      | Récupère le type de média pour la connexion de code confidentiel actuelle.                               |
| Méthodes IPin                                                         | Description                                                                            |
| [**QueryId**](ctransforminputpin-queryid.md)                        | Récupère un identificateur pour le code confidentiel.                                                   |
| [**EndOfStream**](ctransforminputpin-endofstream.md)                | Notifie le code confidentiel qu’aucune donnée supplémentaire n’est attendue.                                  |
| [**BeginFlush**](ctransforminputpin-beginflush.md)                  | Commence une opération de vidage.                                                              |
| [**EndFlush**](ctransforminputpin-endflush.md)                      | Termine une opération de vidage.                                                                |
| [**NewSegment**](ctransforminputpin-newsegment.md)                  | Avertit le code confidentiel que les exemples de supports reçus après cet appel sont regroupés en tant que segment. |
| Méthodes IMemInputPin                                                 | Description                                                                            |
| [**Çoive**](ctransforminputpin-receive.md)                        | Reçoit l’échantillon de média suivant dans le flux.                                          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




