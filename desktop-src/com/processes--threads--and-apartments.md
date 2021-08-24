---
title: Processus, threads et Apartments
description: Un processus est une collection d’espaces de mémoire virtuelle, de code, de données et de ressources système.
ms.assetid: cb62412a-d079-40f9-89dc-cce0bf3889af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320b09d76200739c77c7202af4d53a35089b2eca2e6fd282dd507f048aa7a10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130031"
---
# <a name="processes-threads-and-apartments"></a>Processus, threads et Apartments

Un *processus* est une collection d’espaces de mémoire virtuelle, de code, de données et de ressources système. Un *thread* est du code qui doit être exécuté en série au sein d’un processus. Un processeur exécute les threads, pas les processus, de sorte que chaque application a au moins un processus, et un processus a toujours au moins un thread d’exécution, appelé thread principal. Un processus peut avoir plusieurs threads en plus du thread principal.

Les processus communiquent entre eux par le biais de messages, en utilisant la technologie d’appel de procédure distante (RPC) de Microsoft pour transmettre les informations les unes aux autres. Il n’existe aucune différence de l’appelant entre un appel provenant d’un processus sur un ordinateur distant et un appel provenant d’un autre processus sur le même ordinateur.

Quand un thread commence à s’exécuter, il continue jusqu’à ce qu’il soit supprimé ou jusqu’à ce qu’il soit interrompu par un thread avec une priorité plus élevée (par une action de l’utilisateur ou le planificateur de threads du noyau). Chaque thread peut exécuter des sections de code distinctes, ou plusieurs threads peuvent exécuter la même section de code. Les threads qui exécutent le même bloc de code maintiennent des piles distinctes. Chaque thread dans un processus partage les ressources et les variables globales de ce processus.

Le planificateur de threads détermine quand et à quelle fréquence exécuter un thread, en fonction d’une combinaison de l’attribut de classe de priorité du processus et de la priorité de base du thread. Vous définissez l’attribut de classe de priorité d’un processus en appelant la fonction [**SetPriorityClass**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) , et vous définissez la priorité de base d’un thread à l’aide d’un appel à [**SetThreadPriority**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadpriority).

Les applications multithread doivent éviter deux problèmes de thread : les *interblocages* et les *concurrences*. Un blocage se produit lorsque chaque thread attend que l’autre effectue une opération. Le contrôle d’appel COM permet d’éviter les interblocages dans les appels entre les objets. Une condition de concurrence se produit lorsqu’un thread se termine avant un autre dont il dépend, ce qui provoque l’utilisation d’une valeur non initialisée par la première, car cette dernière n’a pas encore fourni de valeur valide. COM fournit certaines fonctions spécifiquement conçues pour éviter les conditions de concurrence dans les serveurs hors processus. (Voir [assistances pour l’implémentation de serveur hors processus](out-of-process-server-implementation-helpers.md).)

## <a name="the-apartment-and-the-com-threading-architecture"></a>Architecture de cloisonnement et de thread COM

Bien que COM prenne en charge le modèle à un seul thread par processus avant l’introduction de plusieurs threads d’exécution, vous pouvez écrire du code pour tirer parti de plusieurs threads, ce qui permet d’obtenir des applications plus efficaces, en autorisant l’exécution d’un thread pendant qu’un autre thread attend la fin d’une opération de longue durée.

> [!Note]  
> L’utilisation de plusieurs threads n’est pas une garantie de meilleures performances. En fait, étant donné que la factorisation des threads est un problème difficile, l’utilisation de plusieurs threads entraîne souvent des problèmes de performances. La clé consiste à utiliser plusieurs threads uniquement si vous êtes très sûr de ce que vous faites.

 

En général, le moyen le plus simple d’afficher l’architecture du thread COM consiste à considérer tous les objets COM du processus comme divisés en groupes appelés *Apartments*. Un objet COM se trouve dans un seul cloisonnement, dans le sens où ses méthodes peuvent légalement être appelées directement uniquement par un thread qui appartient à ce cloisonnement. Tout autre thread qui souhaite appeler l’objet doit passer par un proxy.

Il existe deux types de cloisonnements : les cloisonnements [à thread unique](single-threaded-apartments.md)et les [cloisonnements](multithreaded-apartments.md)multithread.

-   Les Apartments à thread unique sont constitués d’un seul thread, donc tous les objets COM qui résident dans un cloisonnement à thread unique peuvent recevoir des appels de méthode uniquement à partir du thread qui appartient à ce cloisonnement. Tous les appels de méthode à un objet COM dans un cloisonnement à thread unique sont synchronisés avec la file d’attente de messages Windows pour le thread du cloisonnement à thread unique. Un processus avec un seul thread d’exécution est simplement un cas particulier de ce modèle.
-   Les cloisonnements multithread se composent d’un ou plusieurs threads, donc tous les objets COM qui résident dans un cloisonnement multithread peuvent recevoir des appels de méthode directement à partir de l’un des threads qui appartiennent au cloisonnement multithread. Les threads d’un cloisonnement multithread utilisent un modèle appelé *libre-Threading*. Les appels aux objets COM dans un cloisonnement multithread sont synchronisés par les objets eux-mêmes.

> [!Note]  
> Pour obtenir une description de la communication entre les cloisonnements à thread unique et les cloisonnements multithread dans le même processus, consultez [communication monothread et](single-threaded-and-multithreaded-communication.md)multithread.

 

Un processus peut avoir zéro ou plusieurs cloisonnements à thread unique et zéro ou un cloisonnement multithread.

Dans un processus, le cloisonnement principal est le premier à être initialisé. Dans un processus à thread unique, il s’agit du seul cloisonnement. Les paramètres d’appel sont marshalés entre des Apartments et COM gère la synchronisation par le biais de la messagerie. Si vous désignez plusieurs threads dans un processus pour qu’ils soient libres de threads, tous les threads libres résident dans un seul cloisonnement, les paramètres sont transmis directement à n’importe quel thread du cloisonnement, et vous devez gérer toute la synchronisation. Dans un processus avec des threads libres et de threads cloisonnés, tous les threads libres résident dans un seul cloisonnement et tous les autres cloisonnements sont des cloisonnements à thread unique. Un processus qui effectue un travail COM est une collection de cloisonnements avec, au plus, un cloisonnement multithread, mais un nombre quelconque de Apartments (STA) à thread unique.

Les modèles de thread dans COM fournissent le mécanisme pour les clients et les serveurs qui utilisent différentes architectures de thread pour travailler ensemble. Les appels entre objets avec différents modèles de thread dans des processus différents sont naturellement pris en charge. Du point de vue de l’objet appelant, tous les appels aux objets en dehors d’un processus se comportent de la même façon, quelle que soit la façon dont l’objet appelé est thread. De même, du point de vue de l’objet appelé, les appels entrants se comportent de la même façon, quel que soit le modèle de thread de l’appelant.

L’interaction entre un client et un objet hors processus est simple, même lorsqu’ils utilisent des modèles de thread différents, car le client et l’objet se trouvent dans des processus différents. COM, entre le client et le serveur, peut fournir le code pour que les modèles de threads interopèrent à l’aide du marshaling standard et de RPC. Par exemple, si un objet à thread unique est appelé simultanément par plusieurs clients à thread libre, les appels sont synchronisés par COM en plaçant les messages de fenêtre correspondants dans la file d’attente de messages du serveur. Le cloisonnement de l’objet reçoit un appel chaque fois qu’il récupère et distribue des messages. Toutefois, il est nécessaire de veiller à ce que les serveurs in-process interagissent correctement avec leurs clients. (Voir [problèmes de Threading de serveur in-process](in-process-server-threading-issues.md).)

Le problème le plus important en matière de programmation avec un modèle multithread consiste à rendre votre code sécurisé au niveau du thread afin que les messages destinés à un thread particulier passent uniquement à ce thread et que l’accès aux threads soit protégé.

Pour plus d'informations, voir les rubriques suivantes :

-   [Choix du modèle de thread](choosing-the-threading-model.md)
-   [Apartments (cloisonnés) à thread unique](single-threaded-apartments.md)
-   [Apartments (cloisonnés) multithread](multithreaded-apartments.md)
-   [Communication monothread et multithread](single-threaded-and-multithreaded-communication.md)
-   [Problèmes liés aux threads du serveur in-process](in-process-server-threading-issues.md)
-   [Accès aux interfaces à travers les Apartments](accessing-interfaces-across-apartments.md)

 

 