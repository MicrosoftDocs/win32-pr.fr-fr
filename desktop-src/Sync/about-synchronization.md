---
description: Pour synchroniser l’accès à une ressource, utilisez l’un des objets de synchronisation dans l’une des fonctions Wait.
ms.assetid: 0930bf12-6d5f-4f2c-914d-53e6e862d3bd
title: À propos de la synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ad53dc8c309d8ec55f37cef5f78839348071477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537045"
---
# <a name="about-synchronization"></a>À propos de la synchronisation

Pour synchroniser l’accès à une ressource, utilisez l’un des [objets de synchronisation](synchronization-objects.md) dans l’une des [fonctions Wait](wait-functions.md). L’état d’un objet de synchronisation est *signalé* ou non *signalé*. Les fonctions Wait permettent à un thread de bloquer sa propre exécution jusqu’à ce qu’un objet non signalé spécifié soit défini sur l’état signalé. Pour plus d’informations, consultez [synchronisation entre processus](interprocess-synchronization.md).

Les autres mécanismes de synchronisation sont les suivants :

-   [entrée et sortie avec chevauchement](synchronization-and-overlapped-input-and-output.md)
-   [appels de procédure asynchrone](asynchronous-procedure-calls.md)
-   [objets de section critique](critical-section-objects.md)
-   [variables de condition](condition-variables.md)
-   [verrous de lecture/écriture Slim](slim-reader-writer--srw--locks.md)
-   [initialisation unique](one-time-initialization.md)
-   [accès aux variables verrouillées](interlocked-variable-access.md)
-   [listes liées de façon isolée](interlocked-singly-linked-lists.md)
-   [files d’attente du minuteur](timer-queues.md)
-   la macro [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier)

Pour plus d’informations sur la synchronisation, consultez [problèmes liés à la synchronisation et aux multiprocesseurs](synchronization-and-multiprocessor-issues.md).

 

 
