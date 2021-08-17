---
description: Le planificateur gère une file d’attente de threads exécutables pour chaque niveau de priorité.
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: Commutateurs de contexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c15f5d762525fd4a80030ea10e128e2c30a1ab914e9f17d0f954d80ecfd2e204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143132"
---
# <a name="context-switches"></a>Commutateurs de contexte

Le planificateur gère une file d’attente de threads exécutables pour chaque niveau de priorité. Il s’agit de *Threads prêts* à l’emploi. Lorsqu’un processeur devient disponible, le système effectue un *changement de contexte*. Les étapes d’un changement de contexte sont les suivantes :

1.  Enregistrez le contexte du thread dont l’exécution vient d’être terminée.
2.  Placez le thread qui vient d’être exécuté à la fin de la file d’attente pour sa priorité.
3.  Recherche la file d’attente dont la priorité est la plus élevée et qui contient des threads prêts.
4.  Supprimez le thread situé à l’en-tête de la file d’attente, chargez son contexte et exécutez-le.

Les classes de threads suivantes ne sont pas des threads prêts.

-   Threads créés avec l' \_ indicateur de création suspendu
-   Threads interrompus pendant l’exécution avec la fonction [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) ou [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)
-   Threads en attente d’un objet ou d’une entrée de synchronisation.

Tant que les threads suspendus ou bloqués ne sont pas prêts à être exécutés, le planificateur n’alloue pas de temps processeur à eux, quelle que soit leur priorité.

Les raisons les plus courantes d’un changement de contexte sont les suivantes :

-   La tranche de temps s’est écoulée.
-   Un thread avec une priorité plus élevée est prêt à être exécuté.
-   Un thread en cours d’exécution doit attendre.

Quand un thread en cours d’exécution doit attendre, il abandonne le reste de sa tranche de temps.

 

 
