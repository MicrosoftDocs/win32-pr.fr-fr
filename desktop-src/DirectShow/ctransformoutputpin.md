---
description: La classe CTransformOutputPin implémente une broche de sortie qui est utilisée par la classe CTransformFilter.
ms.assetid: 76f9a981-8f0d-45d4-b901-c5ec5b5ac9ee
title: CTransformOutputPin, classe (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c55c57fbec0a8441b80398370542d94b2b70c1ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224657"
---
# <a name="ctransformoutputpin-class"></a>CTransformOutputPin, classe

![hiérarchie de la classe ctransformoutputpin](images/tfrm02.png)

La `CTransformOutputPin` classe implémente une broche de sortie qui est utilisée par la classe [**CTransformFilter**](ctransformfilter.md) .

En règle générale, vous n’avez pas besoin de dériver de cette classe. La plupart des méthodes de cette classe appellent les méthodes correspondantes sur la classe **CTransformFilter** , que vous pouvez substituer. Si vous dérivez de cette classe, vous devez substituer la méthode [**CTransformFilter :: GetPin**](ctransformfilter-getpin.md) du filtre pour créer des instances de votre classe dérivée.

Cette classe expose les interfaces **IMediaSeeking** et **IMediaPosition** via l’objet [**CPosPassThru**](cpospassthru.md) . Elle transmet toutes les demandes de recherche au filtre suivant en amont.



| Variables membres protégées                                               | Description                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**m \_ pTransformFilter**](ctransformoutputpin-m-ptransformfilter.md)    | Pointeur désignant le filtre propriétaire.                            |
| Variables membres publiques                                                  | Description                                              |
| [**m \_ pPosition**](ctransformoutputpin-m-pposition.md)                  | Objet d’assistance pour passer les commandes de recherche en amont.            |
| M&#233;thodes publiques                                                           | Description                                              |
| [**CTransformOutputPin**](ctransformoutputpin-ctransformoutputpin.md)   | Méthode de constructeur.                                      |
| [**~ CTransformOutputPin**](ctransformoutputpin--ctransformoutputpin.md) | Méthode de destructeur.                                       |
| [**CheckConnect**](ctransformoutputpin-checkconnect.md)                 | Détermine si une connexion de code confidentiel est appropriée.         |
| [**BreakConnect**](ctransformoutputpin-breakconnect.md)                 | Libère le code confidentiel d’une connexion.                      |
| [**CompleteConnect**](ctransformoutputpin-completeconnect.md)           | Termine une connexion à un autre code confidentiel.                   |
| [**CheckMediaType**](ctransformoutputpin-checkmediatype.md)             | Détermine si le code PIN accepte un type de média spécifique.     |
| [**SetMediaType**](ctransformoutputpin-setmediatype.md)                 | Définit le type de média pour la connexion.                  |
| [**DecideBufferSize**](ctransformoutputpin-decidebuffersize.md)         | Définit les exigences de la mémoire tampon.                            |
| [**GetMediaType**](ctransformoutputpin-getmediatype.md)                 | Récupère un type de média par défaut, par valeur d’index.        |
| [**CurrentMediaType**](ctransformoutputpin-currentmediatype.md)         | Récupère le type de média pour la connexion de code confidentiel actuelle. |
| Méthodes IPin                                                             | Description                                              |
| [**QueryId**](ctransformoutputpin-queryid.md)                           | Récupère un identificateur pour le code confidentiel.                     |
| Méthodes IQualityControl                                                  | Description                                              |
| [**Notifier**](ctransformoutputpin-notify.md)                             | Notifie le code confidentiel qu’une modification de qualité est demandée.     |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




