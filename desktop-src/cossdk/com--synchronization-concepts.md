---
description: En règle générale, la synchronisation n’est pas requise lorsque vous avez un thread cloisonné (STA, Single-Threaded Apartment) car le cloisonnement fournit la synchronisation pour vous.
ms.assetid: a05de040-0115-44aa-80e2-55eff2ec894d
title: Concepts de synchronisation COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaca81050e67c76e3de6ad4845543b9230d2a24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748877"
---
# <a name="com-synchronization-concepts"></a>Concepts de synchronisation COM+

En règle générale, la synchronisation n’est pas requise lorsque vous avez un thread cloisonné (STA, Single-Threaded Apartment) car le cloisonnement fournit la synchronisation pour vous. La synchronisation devient importante lorsque vous avez un cloisonnement multithread (MTA) et un objet à thread libre. Dans le passé, les objets à thread libre devaient gérer le verrouillage. Vous pouvez éliminer la nécessité d’utiliser le verrouillage en définissant l’attribut de synchronisation d’un composant.

La synchronisation a les propriétés suivantes :

-   Permet à un appelant d’entrer le composant à la fois.
-   Interdit le passage d’un processus à un autre.
-   Passe du composant au composant au sein d’un processus.
-   Autorise la réentrance à partir du même appelant.

Contrairement aux cloisonnements, les activités couvrent les contextes de plusieurs processus et hôtes. La synchronisation détermine l’activité qui contiendra un objet. Les objets peuvent résider dans l’une des activités suivantes :

-   Activité du créateur
-   Nouvelle activité
-   Aucune activité

COM+ garantit la concurrence par une série de verrous pour chaque activité. Si un appelant tente d’entrer dans un composant COM+ synchronisé qui est déjà utilisé par un autre appelant, l’appel est bloqué jusqu’à ce que le verrou soit libéré. Ce comportement de blocage n’expire pas et ne peut pas être configuré pour expirer. Si le verrou n’est pas utilisé, le verrou est acquis et l’appel est traité. Une fois l’exécution terminée, le verrou est libéré pour l’appelant suivant. Pour éviter les verrous mortels, COM+ gère l’accès à tous les objets entre les activités par une série imbriquée d’appels chaînés sur le réseau.

COM+ fournit les paramètres de synchronisation suivants :

-   Désactivé
-   Non pris en charge
-   Prise en charge
-   Obligatoire
-   Nouveau requis

> [!Note]  
> Certains paramètres de synchronisation fonctionnent conjointement avec d’autres paramètres de composant COM+. Par exemple, la synchronisation est requise si le service [d’activation juste-à-temps (JIT) com+](com--just-in-time-activation.md) est activé. JIT est requis si vous activez des transactions ; par conséquent, le [traitement des transactions](com--transactions.md) com+ requiert également une synchronisation. Ainsi, les classes avec le paramètre de JIT = true doivent également avoir la valeur Synchronization = Required ou Synchronization = RequiresNew.

 

Pour obtenir des instructions sur la définition des options de synchronisation à l’aide de l’outil d’administration Services de composants, consultez [définition de l’attribut de synchronisation](setting-the-synchronization-attribute.md).

Pour obtenir plus d’informations sur l’utilisation de la bibliothèque d’administration COM+ pour définir les options de synchronisation, consultez automatisation de l' [administration com+](automating-com--administration.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches de synchronisation COM+](com--synchronization-tasks.md)
</dt> </dl>

 

 



