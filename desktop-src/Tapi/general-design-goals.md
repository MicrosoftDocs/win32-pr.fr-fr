---
description: La liste suivante répertorie les objectifs de la conception de MSP pour TAPI.
ms.assetid: 286b96c1-047b-4cb9-a189-af2818cfec58
title: Objectifs de conception généraux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 984f897e5ad701e89c6ebf489ebd10828bf207e4f19ca186ca41e780b2e03cba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140572"
---
# <a name="general-design-goals"></a>Objectifs de conception généraux

La liste suivante répertorie les objectifs de la conception de MSP pour TAPI.

-   Les classes de base sont restées simples, avec les membres et les méthodes introduits uniquement lorsque cela est absolument nécessaire.
-   Héritage simple. Aucun héritage multiple entre les classes, bien que l’héritage multiple soit utilisé pour les interfaces.
-   Le verrouillage ne se produit que dans une seule direction pour empêcher tout interblocage. Les méthodes sur l’objet d’appel qui requièrent le verrou sur l’appel peuvent appeler des méthodes sur le flux qui requièrent le verrou sur le flux. Toutefois, les méthodes sur le flux qui requièrent le verrou sur le flux n’appellera jamais une méthode sur l’appel qui requiert un verrou sur l’appel.
-   Les refCounts sont utilisés pour protéger l’accès. Tous les rappels postés dans le pool de threads détiennent refCounts. Le refcount est annulé lorsque l’attente est annulée. L’objet Address contient refCounts sur les terminaux. Les objets d’appel ont des refCounts sur l’adresse et sur Flux. Les objets de flux ont des refCounts sur les appels et les terminaux. Les terminaux ont des refCounts sur Flux. L’refCounts circulaire s’arrête lorsque la méthode Shutdown sur les objets Address et Call est appelée.

 

 



