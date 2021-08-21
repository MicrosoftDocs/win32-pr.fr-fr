---
title: Apartments (cloisonnés) multithread
description: Apartments (cloisonnés) multithread
ms.assetid: d3e6acd9-cd5c-4a2c-8526-4f43db3b606b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69271b4fb6447d48c15fa9005d39020075af09bcc327b12ce539a739c33f8d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047917"
---
# <a name="multithreaded-apartments"></a>Apartments (cloisonnés) multithread

Dans un modèle à cloisonnement multithread, tous les threads du processus qui ont été initialisés en tant que threads libres résident dans un seul cloisonnement. Par conséquent, il n’est pas nécessaire d’effectuer un marshaling entre les threads. Les threads n’ont pas besoin de récupérer et de distribuer les messages, car COM n’utilise pas les messages de fenêtre dans ce modèle.

Les appels aux méthodes d’objets dans le cloisonnement multithread peuvent être exécutés sur n’importe quel thread du cloisonnement. Il n’existe aucune sérialisation des appels ; de nombreux appels peuvent se produire simultanément à la même méthode ou au même objet. Les objets créés dans le cloisonnement multithread doivent être en mesure de gérer des appels sur leurs méthodes à tout moment à partir d’autres threads.

Étant donné que les appels aux objets ne sont pas sérialisés, l’accès concurrentiel aux objets multithread offre les meilleures performances et tire le meilleur parti du matériel multiprocesseur pour les appels inter-threads, inter-processus et inter-ordinateurs. Cela signifie, toutefois, que le code pour les objets doit assurer la synchronisation dans leurs implémentations d’interface, en général à l’aide des primitives de synchronisation telles que les objets d’événement, les sections critiques, les mutex ou les sémaphores, qui sont décrits plus loin dans cette section. En outre, étant donné que l’objet ne contrôle pas la durée de vie des threads qui y accèdent, aucun État spécifique au thread ne peut être stocké dans l’objet (dans le stockage local des threads).

Voici quelques considérations importantes concernant la synchronisation pour les Apartments multithread :

-   COM assure la synchronisation des appels uniquement pour les cloisonnements à thread unique.
-   Les Apartments (cloisonnés) multithread ne reçoivent pas d’appels lors d’appels (sur le même thread).
-   Les Apartments multithread ne peuvent pas effectuer d’appels synchronisés en entrée.
-   Les appels asynchrones sont convertis en appels synchrones dans des Apartments multithread.
-   Le filtre de messages n’est appelé pour aucun thread dans un cloisonnement multithread.

Pour initialiser un thread en tant que thread libre, appelez [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), en spécifiant l’appel de manière multithread \_ . Pour plus d’informations sur les threads de serveur in-process, consultez [problèmes de Threading de serveur in-process](in-process-server-threading-issues.md).

Plusieurs clients peuvent appeler simultanément, à partir de différents threads, un objet qui prend en charge le Threading libre. Dans les serveurs hors processus libres de threads, COM, via le sous-système RPC, crée un pool de threads dans le processus serveur et un appel client (ou plusieurs appels client) peut être remis à tout moment par l’un de ces threads. Un serveur out-of-process doit également implémenter la synchronisation dans sa fabrique de classe. Les objets en thread libre, in-process, peuvent recevoir des appels directs à partir de plusieurs threads du client.

Le client peut effectuer un travail COM dans plusieurs threads. Tous les threads appartiennent au même cloisonnement multithread. Les pointeurs d’interface sont passés directement du thread au thread dans un cloisonnement multithread, de sorte que les pointeurs d’interface ne sont pas marshalés entre ses threads. Les filtres de messages (implémentations de [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)) ne sont pas utilisés dans les cloisonnements multithread. Le thread client s’interrompt lorsqu’il effectue un appel COM aux objets hors cloisonnement et reprendra lorsque l’appel sera retourné. Les appels entre les processus sont toujours gérés par RPC.

Les threads initialisés avec le modèle à thread libre doivent implémenter leur propre synchronisation. comme mentionné plus haut dans cette section, Windows active cette implémentation via les primitives de synchronisation suivantes :

-   Les objets d’événement offrent un moyen de signaler un ou plusieurs threads qu’un événement s’est produit. Tout thread dans un processus peut créer un objet d’événement. Un descripteur de l’événement est retourné par la fonction de création d’événements, [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa). Une fois qu’un objet d’événement a été créé, les threads avec un handle de l’objet peuvent attendre avant de poursuivre l’exécution.
-   Les sections critiques sont utilisées pour une section de code qui nécessite un accès exclusif à un ensemble de données partagées avant de pouvoir être exécutée et qui est utilisée uniquement par les threads dans un processus unique. Une section critique est comme un tourniquet par lequel un seul thread à la fois peut réussir, en procédant comme suit :
    -   Pour garantir qu’un seul thread à la fois accède à des données partagées, le thread principal d’un processus alloue une structure de \_ données de section critique globale et initialise ses membres. Un thread entrant dans une section critique appelle la fonction [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) et modifie les membres de la structure de données.
    -   Un thread tentant d’entrer dans une section critique appelle [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) , qui vérifie si la structure de données de la \_ section critique a été modifiée. Dans ce cas, un autre thread est actuellement dans la section critique et le thread suivant est mis en veille. Un thread quittant une section critique appelle [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection), qui réinitialise la structure de données. Quand un thread quitte une section critique, le système sort l’un des threads en veille, qui entre ensuite dans la section critique.
-   Les mutex effectuent la même fonction qu’une section critique, sauf que le mutex est accessible aux threads exécutés dans des processus différents. La possession d’un objet mutex revient à avoir le plancher dans un débat. Un processus crée un objet mutex en appelant la fonction [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) , qui retourne un handle. Le premier thread qui demande un objet mutex obtient la propriété de celui-ci. Lorsque le thread a terminé avec le mutex, la propriété passe à d’autres threads sur la base du premier arrivé, premier servi.
-   Les sémaphores sont utilisés pour conserver un décompte de références sur une ressource disponible. Un thread crée un sémaphore pour une ressource en appelant la fonction [**CreateSemaphore,**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea) et en passant un pointeur vers la ressource, un nombre de ressources initial et le nombre maximal de ressources. Cette fonction retourne un handle. Un thread demandant une ressource passe son handle de sémaphore dans un appel à la fonction [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) . L’objet Semaphore interroge la ressource pour déterminer si elle est disponible. Si c’est le cas, le sémaphore décrémente le nombre de ressources et sort le thread en attente. Si le nombre est égal à zéro, le thread reste en veille jusqu’à ce qu’un autre thread libère une ressource, ce qui amène le sémaphore à incrémenter le nombre à un.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès aux interfaces à travers les Apartments](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Choix du modèle de thread](choosing-the-threading-model.md)
</dt> <dt>

[Problèmes liés aux threads du serveur in-process](in-process-server-threading-issues.md)
</dt> <dt>

[Processus, threads et Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Communication monothread et multithread](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartments (cloisonnés) à thread unique](single-threaded-apartments.md)
</dt> </dl>

 

 