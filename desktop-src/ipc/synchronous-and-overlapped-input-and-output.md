---
description: E/s de canal synchrone et e/s de canal asynchrone. Les fonctions ReadFile, WriteFile, TransactNamedPipe et ConnectNamedPipe peuvent effectuer des opérations d’entrée et de sortie sur un canal de manière synchrone ou asynchrone.
ms.assetid: 5ab9bb7f-1f99-4041-bba8-2863f34dbcaf
title: E/s de canal synchrones et avec chevauchement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3becfb19dfe5fa49d4121246a576fb3200226b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522419"
---
# <a name="synchronous-and-overlapped-pipe-io"></a>E/s de canal synchrones et avec chevauchement

Les fonctions [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)et [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) peuvent effectuer des opérations d’entrée et de sortie sur un canal de manière synchrone ou asynchrone. Lorsqu’une fonction est exécutée de façon synchrone, elle n’est pas retournée tant que l’opération qu’elle exécute n’est pas terminée. Cela signifie que l’exécution du thread appelant peut être bloquée pendant une période indéterminée pendant qu’elle attend la fin d’une opération longue. Lorsqu’une fonction s’exécute de façon asynchrone, elle est retournée immédiatement, même si l’opération n’a pas été effectuée. Cela permet d’exécuter une opération qui prend du temps en arrière-plan pendant que le thread appelant est libre d’effectuer d’autres tâches.

L’utilisation d’e/s asynchrones permet à un serveur de canal d’utiliser une boucle qui effectue les étapes suivantes :

1.  Spécifiez plusieurs objets d’événement dans un appel à la fonction Wait et attendez que l’un des objets soit défini sur l’état signalé.
2.  Utilisez la valeur de retour de la fonction Wait pour déterminer l’opération Overlapped terminée.
3.  Effectuez les tâches nécessaires pour nettoyer l’opération terminée et initier l’opération suivante pour ce handle de canal. Cela peut impliquer le démarrage d’une autre opération avec chevauchement pour le même handle de canal.

Les opérations avec chevauchement permettent à un canal de lire et d’écrire des données simultanément et à un thread unique d’effectuer des opérations d’e/s simultanées sur plusieurs descripteurs de canal. Cela permet à un serveur de canal à thread unique de gérer efficacement les communications avec plusieurs clients de canal. Pour obtenir un exemple, consultez [serveur de canal nommé utilisant des e/s avec chevauchement](named-pipe-server-using-overlapped-i-o.md).

Pour qu’un serveur de canaux utilise des opérations synchrones pour communiquer avec plusieurs clients, il doit créer un thread distinct pour chaque client de canal afin qu’un ou plusieurs threads puissent s’exécuter pendant que d’autres threads sont en attente. Pour obtenir un exemple de serveur de canaux multithread qui utilise des opérations synchrones, consultez [serveur de canal multithread](multithreaded-pipe-server.md).

## <a name="enabling-asynchronous-operation"></a>Activation de l’opération asynchrone

Les fonctions [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)et [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) peuvent être exécutées de façon asynchrone uniquement si vous activez le mode avec chevauchement pour le handle de canal spécifié et spécifiez un pointeur valide vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . Si le pointeur **OVERLAPPED** a la valeur **null**, la valeur de retour de la fonction peut indiquer de manière incorrecte que l’opération a été effectuée. Par conséquent, il est fortement recommandé que si vous créez un handle avec un indicateur de fichier qui \_ \_ chevauche et que vous souhaitiez un comportement asynchrone, vous devez toujours spécifier une structure **OVERLAPPED** valide.

Le membre **hEvent** de la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) spécifiée doit contenir un handle vers un objet d’événement de réinitialisation manuelle. Il s’agit d’un objet de synchronisation créé par la fonction [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) . Le thread qui lance l’opération Overlapped utilise l’objet d’événement pour déterminer à quel moment l’opération est terminée. Vous ne devez pas utiliser le handle de canal pour la synchronisation lors de l’exécution d’opérations simultanées sur le même handle, car il n’existe aucun moyen de connaître l’achèvement de l’opération qui a provoqué le signalement du handle de canal. La seule technique fiable pour effectuer des opérations simultanées sur le même handle de canal consiste à utiliser une structure **OVERLAPPED** distincte avec son propre objet d’événement pour chaque opération. Pour plus d’informations sur les objets d’événement, consultez [Synchronization](/windows/desktop/Sync/synchronization).

En outre, vous pouvez être averti lorsqu’une opération avec chevauchement se termine à l’aide des fonctions [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) ou [**GetQueuedCompletionStatusEx**](/windows/desktop/FileIO/getqueuedcompletionstatusex-func) . Dans ce cas, vous n’avez pas besoin d’assigner l’événement de réinitialisation manuelle dans la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , et la saisie semi-automatique se produit sur le handle de canal de la même façon qu’une opération asynchrone de lecture ou d’écriture. Pour plus d’informations, consultez [ports de terminaison d’e/s](/windows/desktop/FileIO/i-o-completion-ports).

Quand les opérations [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)et [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) sont exécutées de façon asynchrone, l’une des actions suivantes se produit :

-   Si l’opération est terminée lorsque la fonction retourne, la valeur de retour indique la réussite ou l’échec de l’opération. Si une erreur se produit, la valeur de retour est égale à zéro et la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une valeur autre que erreur d' \_ e/s \_ en attente.
-   Si l’opération n’est pas terminée lorsque la fonction retourne, la valeur de retour est zéro et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne les \_ e/s d’erreur \_ en attente. Dans ce cas, le thread appelant doit attendre la fin de l’opération. Le thread appelant doit ensuite appeler la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) pour déterminer les résultats.

## <a name="using-completion-routines"></a>Utilisation des routines de saisie semi-automatique

Les fonctions [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) et [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) fournissent une autre forme d’e/s avec chevauchement. Contrairement aux fonctions [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) et [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) qui se chevauchent, qui utilisent un objet d’événement pour signaler l’achèvement, les fonctions étendues spécifient une *routine de saisie semi-automatique*. Une routine de saisie semi-automatique est une fonction qui est mise en file d’attente pour l’exécution lorsque l’opération de lecture ou d’écriture est terminée. La routine d’achèvement n’est pas exécutée tant que le thread qui a appelé **ReadFileEx** et **WriteFileEx** n’a pas démarré une opération d' *attente d’alerte* en appelant l’une des [fonctions d’attente alertables](/windows/desktop/Sync/wait-functions) avec le paramètre *fAlertable* défini sur **true**. Dans une opération d’attente d’alerte, les fonctions retournent également quand une routine de saisie semi-automatique **ReadFileEx** ou **WriteFileEx** est mise en file d’attente pour exécution. Un serveur de canaux peut utiliser les fonctions étendues pour exécuter une séquence d’opérations de lecture et d’écriture pour chaque client qui se connecte à ce dernier. Chaque opération de lecture ou d’écriture dans la séquence spécifie une routine de saisie semi-automatique, et chaque routine de saisie semi-automatique lance l’étape suivante dans la séquence. Pour obtenir un exemple, consultez [serveur de canaux nommés utilisant les routines de saisie semi-automatique](named-pipe-server-using-completion-routines.md).

 

 
