---
description: Une barrière de synchronisation permet à plusieurs threads d’attendre que tous les threads aient atteint un point d’exécution particulier avant la poursuite d’un thread.
ms.assetid: 3A76E6F7-C38B-4843-9496-36F3C78B700C
title: Barrières de synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1247d7ab3b20d4fe89763aea0429d742e8ce1c4d11030088316d4e9f3272556b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885981"
---
# <a name="synchronization-barriers"></a>Barrières de synchronisation

Une barrière de synchronisation permet à plusieurs threads d’attendre que tous les threads aient atteint un point d’exécution particulier avant la poursuite d’un thread. Les barrières de synchronisation ne peuvent pas être partagées entre les processus.

Les barrières de synchronisation sont utiles pour les calculs échelonnés, dans lesquels les threads qui exécutent le même code en parallèle doivent tous effectuer une phase avant de passer à l’étape suivante.

Pour créer une barrière de synchronisation, appelez la fonction [**InitializeSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-initializesynchronizationbarrier) et spécifiez un nombre maximal de threads et le nombre de fois qu’un thread doit tourner avant de se bloquer. Lancez ensuite les threads qui utiliseront le cloisonnement. Une fois que chaque thread a terminé son travail, il appelle [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) pour attendre le cloisonnement. La fonction **EnterSynchronizationBarrier** bloque chaque thread jusqu’à ce que le nombre de threads bloqués dans le cloisonnement atteigne le nombre maximal de threads pour le cloisonnement, auquel cas **EnterSynchronizationBarrier** débloque tous les threads. La fonction **EnterSynchronizationBarrier** retourne la **valeur true** pour un seul des threads qui ont entré le cloisonnement et retourne **false** pour tous les autres threads.

Pour libérer une barrière de synchronisation lorsqu’elle n’est plus nécessaire, appelez [**DeleteSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier). Il est possible d’appeler cette fonction immédiatement après l’appel de [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) , car cette fonction garantit que tous les threads ont terminé d’utiliser le cloisonnement avant qu’il ne soit libéré.

Si une barrière de synchronisation ne sera jamais supprimée, les threads peuvent spécifier l’indicateur de **barrière de synchronisation \_ indicateurs de \_ \_ \_ suppression** lorsqu’ils entrent dans le cloisonnement. Tous les threads qui utilisent le cloisonnement doivent spécifier cet indicateur. Si un thread ne le fait pas, l’indicateur est ignoré. Cet indicateur force la fonction à ignorer le travail supplémentaire requis pour la sécurité de la suppression, ce qui peut améliorer les performances. Notez que la suppression d’un cloisonnement alors que cet indicateur est activé peut entraîner un accès géré non valide et un ou plusieurs threads bloqués de manière permanente.

 

 



