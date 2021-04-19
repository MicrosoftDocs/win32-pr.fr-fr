---
description: Les e/s alertables sont la méthode par laquelle les threads d’application traitent les demandes d’e/s asynchrones uniquement lorsqu’elles sont dans un État alerté.
ms.assetid: d996f1cc-eeab-456b-818b-5307a79effd9
title: E/s alertables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb830dfadb97051c47b2472eb3e7a3c2d6a0bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518133"
---
# <a name="alertable-io"></a>E/s alertables

Les e/s alertables sont la méthode par laquelle les threads d’application traitent les demandes d’e/s asynchrones uniquement lorsqu’elles sont dans un État alerté.

Pour comprendre quand un thread est dans un état d’alerte, envisagez le scénario suivant :

1.  Un thread lance une requête de lecture asynchrone en appelant [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) avec un pointeur vers une fonction de rappel.
2.  Le thread lance une demande d’écriture asynchrone en appelant [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) avec un pointeur vers une fonction de rappel.
3.  Le thread appelle une fonction qui extrait une ligne de données à partir d’un serveur de base de données distant.

Dans ce scénario, les appels à [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) et [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) seront probablement retournés avant l’appel de fonction à l’étape 3. Dans ce cas, le noyau place les pointeurs vers les fonctions de rappel dans la file d’attente d’appels de procédure asynchrone (APC) du thread. Le noyau gère cette file d’attente spécifiquement pour conserver les données de requête d’e/s renvoyées jusqu’à ce qu’elle puisse être traitée par le thread correspondant.

Lorsque l’extraction de lignes est terminée et que le thread retourne de la fonction, sa priorité la plus élevée consiste à traiter les demandes d’e/s renvoyées sur la file d’attente en appelant les fonctions de rappel. Pour ce faire, il doit entrer un état d’alerte. Un thread ne peut le faire qu’en appelant l’une des fonctions suivantes avec les indicateurs appropriés :

-   [**SleepEx**](/windows/desktop/api/synchapi/nf-synchapi-sleepex)
-   [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)
-   [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)
-   [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)
-   [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex)

Lorsque le thread entre dans un état d’alerte, les événements suivants se produisent :

1.  Le noyau vérifie la file d’attente APC du thread. Si la file d’attente contient des pointeurs de fonction de rappel, le noyau supprime le pointeur de la file d’attente et l’envoie au thread.
2.  Le thread exécute la fonction de rappel.
3.  Les étapes 1 et 2 sont répétées pour chaque pointeur restant dans la file d’attente.
4.  Lorsque la file d’attente est vide, le thread retourne de la fonction qui l’a placée dans un état d’alerte.

Dans ce scénario, une fois que le thread entre dans un état d’alerte, il appellera les fonctions de rappel envoyées à [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) et [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex), puis le retour de la fonction qui l’a placée dans un état d’alerte.

Si un thread entre dans un état d’alerte alors que sa file d’attente APC est vide, l’exécution du thread est suspendue par le noyau jusqu’à ce que l’un des éléments suivants se produise :

-   L’objet de noyau attendu est signalé.
-   Un pointeur de fonction de rappel est placé dans la file d’attente APC.

Un thread qui utilise des e/s alertables traite les demandes d’e/s asynchrones plus efficacement que lorsqu’il attend simplement l’indicateur d’événement dans la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) à définir, et le mécanisme d’e/s d’alerte est moins compliqué que les [ports de terminaison d’e/s](i-o-completion-ports.md) à utiliser. Toutefois, les e/s alertables renvoient le résultat de la requête d’e/s uniquement au thread qui l’a lancée. Les ports de terminaison d’e/s n’ont pas cette limitation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appels de procédure asynchrone](/windows/desktop/Sync/asynchronous-procedure-calls)
</dt> </dl>

 

 
