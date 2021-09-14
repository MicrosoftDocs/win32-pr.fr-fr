---
description: Pour éviter les blocages et les conditions de concurrence, il est nécessaire de synchroniser l’accès de plusieurs threads aux ressources partagées. La synchronisation est également nécessaire pour s’assurer que le code interdépendance est exécuté dans l’ordre approprié.
ms.assetid: 74af0502-dae1-438c-8e4b-7663093b3fe3
title: Synchronisation de l’exécution de plusieurs threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6a1b3dd51d666d507771476792e679f7980fab8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007086"
---
# <a name="synchronizing-execution-of-multiple-threads"></a>Synchronisation de l’exécution de plusieurs threads

Pour éviter les blocages et les conditions de concurrence, il est nécessaire de synchroniser l’accès de plusieurs threads aux ressources partagées. La synchronisation est également nécessaire pour s’assurer que le code interdépendance est exécuté dans l’ordre approprié.

Il existe un certain nombre d’objets dont les descripteurs peuvent être utilisés pour synchroniser plusieurs threads. Ces objets sont les suivants :

-   Mémoires tampons d’entrée de la console
-   Événements
-   Mutex
-   Processus
-   Sémaphores
-   Threads
-   Minuteurs

L’état de chacun de ces objets est signalé ou n’est pas signalé. Lorsque vous spécifiez un handle à l’un de ces objets dans un appel à l’une des [fonctions d’attente](../sync/wait-functions.md), l’exécution du thread appelant est bloquée jusqu’à ce que l’état de l’objet spécifié soit signalé.

Certains de ces objets sont utiles pour bloquer un thread jusqu’à ce qu’un événement se produise. Par exemple, un descripteur de mémoire tampon d’entrée de console est signalé quand il y a une entrée non lue, telle qu’un clic de touche ou de bouton de la souris. Les handles de processus et de thread sont signalés lorsque le processus ou le thread se termine. Cela permet à un processus, par exemple, de créer un processus enfant, puis de bloquer sa propre exécution jusqu’à la fin du nouveau processus.

D’autres objets sont utiles pour protéger les ressources partagées de l’accès simultané. Par exemple, plusieurs threads peuvent avoir chacun un handle vers un objet Mutex. Avant d’accéder à une ressource partagée, les threads doivent appeler l’une des [fonctions Wait](../sync/wait-functions.md) pour attendre que l’état du mutex soit signalé. Lorsque le mutex est signalé, un seul thread en attente est libéré pour accéder à la ressource. L’état du mutex est immédiatement réinitialisé à non signalé, de sorte que tous les autres threads en attente restent bloqués. Une fois le thread terminé avec la ressource, il doit définir l’état du mutex comme étant signalé pour permettre à d’autres threads d’accéder à la ressource.

Pour les threads d’un processus unique, les objets de section critique offrent un moyen de synchronisation plus efficace que les mutex. Une section critique est utilisée comme un mutex pour permettre à un thread à la fois d’utiliser la ressource protégée. Un thread peut utiliser la fonction [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) pour demander la propriété d’une section critique. S’il est déjà détenu par un autre thread, le thread demandeur est bloqué. Un thread peut utiliser la fonction [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) pour demander la propriété d’une section critique, sans se bloquer en cas d’échec d’obtention de la section critique. Une fois la propriété reçue, le thread est libre d’utiliser la ressource protégée. L’exécution des autres threads du processus n’est pas affectée, à moins qu’ils ne tentent d’entrer dans la même section critique.

La fonction [**WaitForInputIdle**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle) fait en sorte qu’un thread attende jusqu’à ce qu’un processus spécifié soit initialisé et en attente d’une entrée utilisateur sans aucune entrée en attente. L’appel de **WaitForInputIdle** peut être utile pour synchroniser des processus parents et enfants, car [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) retourne sans attendre que le processus enfant termine son initialisation.

Pour plus d’informations, consultez [Synchronization](../sync/synchronization.md).

 

 
