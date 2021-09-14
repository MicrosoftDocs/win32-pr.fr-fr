---
description: Un pool de threads est une collection de threads de travail qui exécutent efficacement des rappels asynchrones pour le compte de l’application.
ms.assetid: abe0798a-0b60-4bdb-a61e-45393f1e958d
title: Pools de threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690aa3eb6fd3ce7a99d71e0f57118529ef79113f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007071"
---
# <a name="thread-pools"></a>Pools de threads

Un *pool de threads* est une collection de threads de travail qui exécutent efficacement des rappels asynchrones pour le compte de l’application. Le pool de threads est principalement utilisé pour réduire le nombre de threads d’application et assurer la gestion des threads de travail. Les applications peuvent effectuer la mise en file d’attente des éléments de travail, associer un travail à des handles pouvant être programmés, effectuer la file d’attente automatiquement en fonction d’un minuteur et établir une liaison avec

## <a name="thread-pool-architecture"></a>Architecture du pool de threads

Les applications suivantes peuvent tirer parti de l’utilisation d’un pool de threads :

-   Une application hautement parallèle et pouvant distribuer un grand nombre de petits éléments de travail de façon asynchrone (par exemple, la recherche d’index distribuée ou les e/s réseau).
-   Application qui crée et détruit un grand nombre de threads qui s’exécutent chacun pendant une brève période. L’utilisation du pool de threads peut réduire la complexité de la gestion des threads et la surcharge impliquée dans la création et la destruction de threads.
-   Application qui traite les éléments de travail indépendants en arrière-plan et en parallèle (tels que le chargement de plusieurs onglets).
-   Application qui doit effectuer une attente exclusive sur les objets de noyau ou un bloc sur les événements entrants sur un objet. L’utilisation du pool de threads peut réduire la complexité de la gestion des threads et améliorer les performances en réduisant le nombre de changements de contexte.
-   Application qui crée des threads d’attente personnalisés à attendre sur les événements.

le pool de threads d’origine a été complètement remanié dans Windows Vista. Le nouveau pool de threads est amélioré, car il fournit un seul type de thread de travail (prend en charge les e/s et non-e/s), n’utilise pas de thread de minuterie, fournit une file d’attente de minuteur unique et fournit un thread persistant dédié. Il fournit également des groupes de nettoyage, des performances supérieures, plusieurs pools par processus qui sont planifiés indépendamment et une nouvelle API de pool de threads.

L’architecture du pool de threads se compose des éléments suivants :

-   Threads de travail qui exécutent les fonctions de rappel
-   Threads d’attente qui attendent plusieurs handles d’attente
-   Une file d’attente de travail
-   Pool de threads par défaut pour chaque processus
-   Une fabrique de travail qui gère les threads de travail

## <a name="best-practices"></a>Bonnes pratiques

La nouvelle [API de pool de threads](thread-pool-api.md) offre plus de souplesse et de contrôle que l' [API de pool de threads d’origine](thread-pooling.md). Toutefois, il existe quelques différences subtiles mais importantes. Dans l’API d’origine, la réinitialisation de l’attente était automatique ; dans la nouvelle API, l’attente doit être explicitement réinitialisée à chaque fois. L’API d’origine gérait l’emprunt d’identité automatiquement, en transférant le contexte de sécurité du processus appelant au thread. Avec la nouvelle API, l’application doit définir explicitement le contexte de sécurité.

Voici les meilleures pratiques lors de l’utilisation d’un pool de threads :

-   Les threads d’un processus partagent le pool de threads. Un seul thread de travail peut exécuter plusieurs fonctions de rappel, une à la fois. Ces threads de travail sont gérés par le pool de threads. Par conséquent, ne terminez pas un thread du pool de threads en appelant [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) sur le thread ou en appelant [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) à partir d’une fonction de rappel.
-   Une requête d’e/s peut s’exécuter sur n’importe quel thread du pool de threads. L’annulation d’e/s sur un thread de pool de threads nécessite une synchronisation, car la fonction Cancel peut s’exécuter sur un thread différent de celui qui gère la requête d’e/s, ce qui peut entraîner l’annulation d’une opération inconnue. Pour éviter cela, fournissez toujours la structure avec [**chevauchement**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) avec laquelle une demande d’e/s a été initialisée lors de l’appel de [**CancelIoEx**](/windows/win32/api/ioapiset/nf-ioapiset-cancelioex) pour les e/s asynchrones, ou utilisez votre propre synchronisation pour vous assurer qu’aucune autre e/s ne peut être démarrée sur le thread cible avant d’appeler la fonction [**CancelSynchronousIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelsynchronousio) ou **CancelIoEx** .
-   Nettoyez toutes les ressources créées dans la fonction de rappel avant de retourner à partir de la fonction. Celles-ci incluent le protocole TLS, les contextes de sécurité, la priorité des threads et l’inscription COM. Les fonctions de rappel doivent également restaurer l’état du thread avant de retourner.
-   Maintenez les handles d’attente et leurs objets associés actifs jusqu’à ce que le pool de threads ait signalé qu’il s’est terminé avec le descripteur.
-   Marquez tous les threads en attente d’opérations de longue durée (par exemple, les vidages d’e/s ou le nettoyage des ressources) afin que le pool de threads puisse allouer de nouveaux threads au lieu d’attendre celui-ci.
-   Avant de décharger une DLL qui utilise le pool de threads, annulez tous les éléments de travail, les e/s, les opérations d’attente et les minuteurs, puis attendez la fin de l’exécution des rappels.
-   Évitez les interblocages en éliminant les dépendances entre les éléments de travail et entre les rappels, en vérifiant qu’un rappel n’attend pas son exécution et en préservant la priorité du thread.
-   Ne pas mettre trop d’éléments en file d’attente trop rapidement dans un processus avec d’autres composants à l’aide du pool de threads par défaut. Il existe un pool de threads par défaut par processus, y compris Svchost.exe. Par défaut, chaque pool de threads a un maximum de 500 threads de travail. Le pool de threads tente de créer plus de threads de travail lorsque le nombre de threads de travail dans l’état prêt/en cours d’exécution doit être inférieur au nombre de processeurs.
-   Évitez le modèle COM à thread unique cloisonné, car il est incompatible avec le pool de threads. STA crée l’état du thread qui peut affecter l’élément de travail suivant pour le thread. La valeur STA est généralement à durée de vie longue et a une affinité de thread, qui est l’inverse du pool de threads.
-   Créez un pool de threads pour contrôler la priorité et l’isolation des threads, créer des caractéristiques personnalisées et éventuellement améliorer la réactivité. Toutefois, les pools de threads supplémentaires nécessitent davantage de ressources système (threads, mémoire du noyau). Un trop grand nombre de pools augmente le risque de contention de l’UC.
-   Si possible, utilisez un objet d’attente au lieu d’un mécanisme APC pour signaler un thread de pool de threads. Les APC ne fonctionnent pas aussi bien avec les threads de pool de threads que les autres mécanismes de signalisation car le système contrôle la durée de vie des threads de pool de threads. il est donc possible qu’un thread se termine avant la remise de la notification.
-   Utilisez l’extension du débogueur du pool de threads, ! TP. L’utilisation de cette commande est la suivante :

    -   *indicateurs* d' *adresse* du pool
    -   *indicateurs* d' *adresse* obj
    -   *indicateurs* d' *adresse* timpossible
    -   *adresse* d’attente
    -   *adresse* du Worker

    Pour les pools, les Waiters et les Worker, si l’adresse est égale à zéro, la commande fait un dump de tous les objets. Pour l’attente et le Worker, l’omission de l’adresse vide le thread actuel. Les indicateurs suivants sont définis : 0x1 (sortie sur une seule ligne), 0X2 (membres dump) et 0x4 (file d’attente de travail du pool de vidage).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API du pool de threads](thread-pool-api.md)
</dt> <dt>

[Utilisation des fonctions de pool de threads](using-the-thread-pool-functions.md)
</dt> </dl>

 

 
