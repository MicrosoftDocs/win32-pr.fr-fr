---
description: La classe CBaseRendererInputPin implémente une broche d’entrée pour la classe CBaseRenderer. Sauf indication contraire, les méthodes de cette classe délèguent aux méthodes correspondantes sur la classe CBaseRenderer.
ms.assetid: da3e6aba-c2cc-4fd4-b382-fc4bc7fef774
title: CRendererInputPin, classe (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2cfeb61d075804d61ba515d86641e56bf3cd9e1ab6aa6de826a8bb7206be4fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908243"
---
# <a name="crendererinputpin-class"></a>CRendererInputPin, classe

![hiérarchie de la classe crendererinput pin](images/rbase01.png)

La classe **CBaseRendererInputPin** implémente une broche d’entrée pour la classe [**CBaseRenderer**](cbaserenderer.md) . Sauf indication contraire, les méthodes de cette classe délèguent aux méthodes correspondantes sur la classe **CBaseRenderer** .



| Variables membres protégées                                       | Description                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ pRenderer**](crendererinputpin-m-prenderer.md)            | Pointeur vers le filtre.                                                                 |
| M&#233;thodes publiques                                                   | Description                                                                            |
| [**CRendererInputPin**](crendererinputpin-crendererinputpin.md) | Méthode de constructeur.                                                                    |
| [**BreakConnect**](crendererinputpin-breakconnect.md)           | Ajoute du code personnalisé lors de la rupture d’une connexion.                                       |
| [**CompleteConnect**](crendererinputpin-completeconnect.md)     | Termine la connexion.                                                              |
| [**CheckMediaType**](crendererinputpin-checkmediatype.md)       | Détermine si le code confidentiel peut prendre en charge un type de média spécifique.                               |
| [**Actif**](crendererinputpin-active.md)                       | Bascule le code PIN sur le mode actif (en pause ou en cours d’exécution).                               |
| [**Inactive**](crendererinputpin-inactive.md)                   | Bascule le code confidentiel vers un état inactif et libère la mémoire de l’allocateur.        |
| [**SetMediaType**](crendererinputpin-setmediatype.md)           | Définit le type de média du code confidentiel.                                                        |
| [**Allocateur**](crendererinputpin-allocator.md)                 | Récupère un pointeur vers l’allocateur de mémoire par défaut.                                   |
| Méthodes IPin                                                     | Description                                                                            |
| [**QueryId**](crendererinputpin-queryid.md)                     | Récupère un identificateur pour le code confidentiel.                                                   |
| [**EndOfStream**](crendererinputpin-endofstream.md)             | Informe le code confidentiel qu’aucune donnée supplémentaire n’est attendue tant qu’une nouvelle commande d’exécution n’est pas émise. |
| [**BeginFlush**](crendererinputpin-beginflush.md)               | Indique au code PIN de commencer une opération de vidage.                                            |
| [**EndFlush**](crendererinputpin-endflush.md)                   | Informe le code confidentiel pour terminer une opération de vidage.                                              |
| Méthodes IMemInputPin                                             | Description                                                                            |
| [**Çoive**](crendererinputpin-receive.md)                     | Récupère le bloc de données suivant à partir du flux.                                      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




