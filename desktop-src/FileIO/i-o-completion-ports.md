---
description: Les ports de terminaison d’e/s fournissent un modèle de thread efficace pour traiter plusieurs demandes d’e/s asynchrones sur un système multiprocesseur.
ms.assetid: 213c48e8-bb21-43ed-9c00-2a5cf8ac25f0
title: Ports de terminaison d’e/s
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 882363ef99821a0b0b40810f45d609c5b5f7760c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530742"
---
# <a name="io-completion-ports"></a>Ports de terminaison d’e/s

Les ports de terminaison d’e/s fournissent un modèle de thread efficace pour traiter plusieurs demandes d’e/s asynchrones sur un système multiprocesseur. Lorsqu’un processus crée un port de terminaison d’e/s, le système crée un objet de file d’attente associé pour les demandes dont l’unique objectif est de traiter ces demandes. Les processus qui gèrent de nombreuses demandes d’e/s asynchrones simultanées peuvent le faire plus rapidement et efficacement en utilisant des ports de terminaison d’e/s conjointement à un pool de threads pré-alloués que en créant des threads au moment où ils reçoivent une demande d’e/s.

## <a name="how-io-completion-ports-work"></a>Fonctionnement des ports de terminaison d’e/s

La fonction [**CreateIoCompletionPort**](createiocompletionport.md) crée un port de terminaison d’e/s et associe un ou plusieurs descripteurs de fichiers à ce port. Lorsqu’une opération d’e/s asynchrone sur l’un de ces descripteurs de fichiers se termine, un paquet d’achèvement d’e/s est mis en file d’attente dans l’ordre FIFO (premier entré, premier sorti) du port d’achèvement d’e/s associé. Une utilisation puissante de ce mécanisme consiste à combiner le point de synchronisation pour plusieurs descripteurs de fichiers en un seul objet, bien qu’il y ait également d’autres applications utiles. Notez que, si les paquets sont mis en file d’attente dans l’ordre FIFO, ils peuvent être déplacés dans la file d’attente dans un ordre différent.

> [!Note]
>
> Le terme *descripteur de fichier* utilisé ici fait référence à une abstraction système représentant un point de terminaison d’e/s avec chevauchement, et non un fichier sur le disque. Par exemple, il peut s’agir d’un point de terminaison réseau, d’un socket TCP, d’un canal nommé ou d’un emplacement de messagerie. Tout objet système qui prend en charge les e/s avec chevauchement peut être utilisé. Pour obtenir la liste des fonctions d’e/s associées, consultez la fin de cette rubrique.

 

Lorsqu’un descripteur de fichier est associé à un port de terminaison, le bloc d’état transmis n’est pas mis à jour tant que le paquet n’a pas été supprimé du port de terminaison. La seule exception est si l’opération d’origine retourne en mode synchrone avec une erreur. Un thread (soit créé par le thread principal, soit le thread principal lui-même) utilise la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) pour attendre la mise en file d’attente d’un paquet d’achèvement vers le port de terminaison d’e/s, au lieu d’attendre directement la fin des e/s asynchrones. Les threads qui bloquent leur exécution sur un port de terminaison d’e/s sont libérés dans l’ordre LIFO (dernier entré, premier sorti) et le paquet d’achèvement suivant est extrait de la file d’attente FIFO du port de terminaison d’e/s pour ce thread. Cela signifie que, lorsqu’un paquet de saisie semi-automatique est libéré sur un thread, le système libère le dernier thread (le plus récent) associé à ce port, en lui transmettant les informations de saisie semi-automatique des e/s les plus anciennes.

Même si un nombre quelconque de threads peut appeler [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) pour un port de terminaison d’e/s spécifié, lorsqu’un thread spécifié appelle **GetQueuedCompletionStatus** la première fois, il est associé au port de terminaison d’e/s spécifié jusqu’à ce que l’un des trois événements se produise : le thread se termine, spécifie un autre port de terminaison d’e En d’autres termes, un seul thread peut être associé, au plus, à un port de terminaison d’e/s.

Lorsqu’un paquet de saisie semi-automatique est mis en file d’attente sur un port de terminaison d’e/s, le système vérifie d’abord le nombre de threads associés à ce port en cours d’exécution. Si le nombre de threads en cours d’exécution est inférieur à la valeur d’accès concurrentiel (décrite dans la section suivante), l’un des threads en attente (le plus récent) est autorisé à traiter le paquet d’achèvement. Lorsqu’un thread en cours d’exécution termine son traitement, il appelle généralement à nouveau [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) , à savoir qu’il retourne avec le paquet d’achèvement suivant ou attend si la file d’attente est vide.

Les threads peuvent utiliser la fonction [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) pour placer les paquets de saisie semi-automatique dans la file d’attente d’un port de terminaison d’e/s. En procédant ainsi, le port de terminaison peut être utilisé pour recevoir des communications d’autres threads du processus, en plus de recevoir des paquets de terminaison d’e/s du système d’e/s. La fonction **PostQueuedCompletionStatus** permet à une application de faire la file d’attente de ses propres paquets d’achèvement à usage spécial sur le port de terminaison d’e/s sans démarrer une opération d’e/s asynchrone. Cela est utile pour notifier les threads de travail des événements externes, par exemple.

Le descripteur de port de terminaison d’e/s et chaque descripteur de fichier associé à ce port de terminaison d’e/s particulier sont appelés *références au port de terminaison d’e/s*. Le port de terminaison d’e/s est libéré lorsqu’il n’y a plus de références à celui-ci. Par conséquent, tous ces handles doivent être correctement fermés pour libérer le port de terminaison d’e/s et les ressources système qui lui sont associées. Une fois ces conditions satisfaites, une application doit fermer le descripteur de port de terminaison d’e/s en appelant la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .

> [!Note]
>
> Un port de terminaison d’e/s est associé au processus qui l’a créé et il n’est pas partageable entre les processus. Toutefois, un seul descripteur peut être partagé entre les threads du même processus.

 

## <a name="threads-and-concurrency"></a>Threads et accès concurrentiel

La propriété la plus importante d’un port de terminaison d’e/s à prendre en compte avec soin est la valeur d’accès concurrentiel. La valeur d’accès concurrentiel d’un port de terminaison est spécifiée lorsqu’elle est créée avec [**CreateIoCompletionPort**](createiocompletionport.md) via le paramètre *NumberOfConcurrentThreads* . Cette valeur limite le nombre de threads exécutables associés au port de terminaison. Lorsque le nombre total de threads exécutables associés au port de terminaison atteint la valeur d’accès concurrentiel, le système bloque l’exécution de tous les threads suivants associés à ce port de terminaison jusqu’à ce que le nombre de threads exécutables descend sous la valeur d’accès concurrentiel.

Le scénario le plus efficace se produit lorsqu’il y a des paquets d’achèvement en attente dans la file d’attente, mais qu’aucune attente ne peut être satisfaite, car le port a atteint sa limite de concurrence. Examinez ce qui se passe avec une valeur d’accès concurrentiel d’un et plusieurs threads en attente dans l’appel de fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) . Dans ce cas, si la file d’attente a toujours des paquets d’achèvement en attente, lorsque le thread en cours d’exécution appelle **GetQueuedCompletionStatus**, il ne bloque pas l’exécution car, comme mentionné précédemment, la file d’attente de threads est LIFO. Au lieu de cela, ce thread récupère immédiatement le paquet de fin de mise en file d’attente suivant. Aucun changement de contexte de thread ne se produit, car le thread en cours d’exécution collecte continuellement des paquets d’achèvement et les autres threads ne peuvent pas s’exécuter.

> [!Note]
>
> Dans l’exemple précédent, les threads supplémentaires semblent inutiles et ne s’exécutent jamais, mais cela suppose que le thread en cours d’exécution n’est jamais placé en état d’attente par un autre mécanisme, se termine ou ferme le port de terminaison d’e/s associé. Tenez compte de toutes ces ramifications d’exécution de thread lors de la conception de l’application.

 

La meilleure valeur globale maximale à sélectionner pour la valeur d’accès concurrentiel est le nombre de processeurs sur l’ordinateur. Si votre transaction requiert un calcul de longue durée, une plus grande valeur d’accès concurrentiel permettra l’exécution d’un plus grand nombre de threads. Chaque paquet d’achèvement peut durer plus longtemps, mais plus de paquets d’achèvement seront traités en même temps. Vous pouvez expérimenter la valeur d’accès concurrentiel conjointement avec les outils de profilage pour obtenir le meilleur effet pour votre application.

Le système permet également à un thread qui attend [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) de traiter un paquet d’achèvement si un autre thread en cours d’exécution associé au même port de terminaison d’e/s entre dans un état d’attente pour d’autres raisons, par exemple la fonction [**SuspendThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-suspendthread) . Lorsque le thread de l’état d’attente commence à s’exécuter à nouveau, il peut y avoir une courte période lorsque le nombre de threads actifs dépasse la valeur d’accès concurrentiel. Toutefois, le système réduit rapidement ce nombre en n’autorisant pas de nouveaux threads actifs jusqu’à ce que le nombre de threads actifs passe sous la valeur d’accès concurrentiel. C’est l’une des raisons pour lesquelles votre application crée plus de threads dans son pool de threads que la valeur d’accès concurrentiel. La gestion des pools de threads dépasse le cadre de cette rubrique, mais une bonne règle empirique consiste à avoir un minimum de deux fois plus de threads dans le pool de threads qu’il n’y a de processeurs sur le système. Pour plus d’informations sur le regroupement de threads, consultez [pools de threads](/windows/desktop/ProcThread/thread-pools).

## <a name="supported-io-functions"></a>Fonctions d’e/s prises en charge

Les fonctions suivantes peuvent être utilisées pour démarrer des opérations d’e/s qui se terminent à l’aide de ports de terminaison d’e/s. Vous devez passer à la fonction une instance de la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) et un handle de fichier précédemment associé à un port de terminaison d’e/s (par un appel à [**CreateIoCompletionPort**](createiocompletionport.md)) pour activer le mécanisme de port de terminaison d’e/s :

-   [**ConnectNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
-   [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
-   [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
-   [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
-   [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
-   [**TransactNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
-   [**WaitCommEvent**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
-   [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
-   [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)
-   [**WSASendTo**](/windows/desktop/api/winsock2/nf-winsock2-wsasendto)
-   [**WSASend**](/windows/desktop/api/winsock2/nf-winsock2-wsasend)
-   [**WSARecvFrom**](/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom)
-   [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
-   [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>


</dt> <dt>

[À propos des processus et des threads](/windows/desktop/ProcThread/about-processes-and-threads)
</dt> <dt>

[**BindIoCompletionCallback**](/windows/desktop/api/winbase/nf-winbase-bindiocompletioncallback)
</dt> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> </dl>

 

 
