---
description: Le planificateur gère une file d’attente de threads exécutables pour chaque niveau de priorité.
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: Commutateurs de contexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7628ee9e659cdbc2369b5f69d25847e8864dbd62
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096542"
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

 

 
