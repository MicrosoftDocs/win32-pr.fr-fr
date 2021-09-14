---
description: 'Il existe deux types de synchronisation d’entrée/sortie (e/s) : e/s synchrone et e/s asynchrones. Les e/s asynchrones sont également appelées e/s avec chevauchement.'
ms.assetid: ade51d98-cc9d-4b33-9c52-559a9cb14707
title: E/s synchrones et asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 071dd2943537dcb6aff67a95cb5e2c3d514f4c1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009830"
---
# <a name="synchronous-and-asynchronous-io"></a>E/s synchrones et asynchrones

Consultez également [les exemples d’applications liées aux e/s](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winbase/io).

Il existe deux types de synchronisation d’entrée/sortie (e/s) : e/s synchrone et e/s asynchrones. Les e/s asynchrones sont également appelées e/s avec chevauchement.

Dans les *e/s de fichier synchrones*, un thread démarre une opération d’e/s et entre immédiatement dans un état d’attente jusqu’à ce que la demande d’e/s soit terminée. Un thread effectuant des *e/s de fichier asynchrones* envoie une requête d’e/s au noyau en appelant une fonction appropriée. Si la demande est acceptée par le noyau, le thread appelant continue à traiter un autre travail jusqu’à ce que le noyau signale au thread que l’opération d’e/s est terminée. Il interrompt ensuite son travail en cours et traite les données de l’opération d’e/s en fonction des besoins.

Les deux types de synchronisation sont illustrés dans la figure suivante.

![e/s synchrones et asynchrones](images/fig2bedit.png)

Dans les situations où une demande d’e/s est supposée prendre beaucoup de temps, par exemple une actualisation ou une sauvegarde d’une base de données volumineuse ou d’une liaison de communication lente, les e/s asynchrones constituent généralement un bon moyen d’optimiser l’efficacité du traitement. Toutefois, pour les opérations d’e/s relativement rapides, la surcharge liée au traitement des demandes d’e/s de noyau et des signaux de noyau peut rendre les e/s asynchrones moins bénéfiques, en particulier si de nombreuses opérations d’e/s rapides doivent être effectuées. Dans ce cas, les e/s synchrones seraient préférables. Les mécanismes et les détails d’implémentation de l’exécution de ces tâches varient en fonction du type de descripteur d’appareil utilisé et des besoins spécifiques de l’application. En d’autres termes, il existe généralement plusieurs façons de résoudre le problème.

## <a name="synchronous-and-asynchronous-io-considerations"></a>Considérations relatives aux e/s synchrones et asynchrones

Si un fichier ou un appareil est ouvert pour des e/s synchrones (c’est-à-dire que l' **indicateur de fichier \_ \_ OVERLAPPED** n’est pas spécifié), les appels suivants à des fonctions telles que [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) peuvent bloquer l’exécution du thread appelant jusqu’à ce que l’un des événements suivants se produise :

-   L’opération d’e/s se termine (dans cet exemple, une écriture de données).
-   Une erreur d’E/S se produit. (Par exemple, le canal est fermé à partir de l’autre extrémité.)
-   Une erreur s’est produite dans l’appel lui-même (par exemple, un ou plusieurs paramètres ne sont pas valides).
-   Un autre thread du processus appelle la fonction [**CancelSynchronousIo**](cancelsynchronousio-func.md) à l’aide du handle de thread du thread bloqué, qui met fin à l’e/s de ce thread, ce qui a échoué lors de l’opération d’e/s.
-   Le thread bloqué se termine par le système ; par exemple, le processus lui-même est terminé, ou un autre thread appelle la fonction [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) à l’aide du handle du thread bloqué. (Il s’agit généralement d’un dernier recours et non d’une conception d’application correcte.)

Dans certains cas, ce délai peut être inacceptable pour la conception et l’objectif de l’application, de sorte que les concepteurs d’applications doivent envisager d’utiliser des e/s asynchrones avec des objets de synchronisation de threads appropriés, tels que les [ports de terminaison d’e/s](i-o-completion-ports.md). Pour plus d’informations sur la synchronisation des threads, consultez [à propos](/windows/desktop/Sync/about-synchronization)de la synchronisation.

Un processus ouvre un fichier pour les e/s asynchrones dans son appel à [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) en spécifiant l’indicateur de **\_ \_ chevauchement** de l’indicateur de fichier dans le paramètre *dwFlagsAndAttributes* . Si l' **indicateur de fichier avec \_ \_ chevauchement** n’est pas spécifié, le fichier est ouvert pour les e/s synchrones. Quand le fichier a été ouvert pour des e/s asynchrones, un pointeur vers une structure [**OVERLAPPED**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) est passé dans l’appel à [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) et [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile). Lors de l’exécution d’e/s synchrones, cette structure n’est pas requise dans les appels à **ReadFile** et **WriteFile**.

> [!Note]  
> Si un fichier ou un appareil est ouvert pour des e/s asynchrones, les appels suivants à des fonctions telles que [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) à l’aide de ce handle sont généralement retournés immédiatement, mais peuvent également se comporter de façon synchrone en ce qui concerne l’exécution bloquée. Pour plus d’informations, consultez [https://support.microsoft.com/kb/156932](https://support.microsoft.com/kb/156932).

 

Bien que [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) soit la fonction la plus courante à utiliser pour ouvrir des fichiers, des volumes de disque, des canaux anonymes et d’autres périphériques similaires, les opérations d’e/s peuvent également être effectuées à l’aide d’un descripteur de *conversion* à partir d’autres objets système tels qu’un socket créé par le [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) ou des fonctions [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) .

Les handles des objets d’annuaire sont obtenus en appelant la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) avec l’attribut sémantique de sauvegarde de l' **indicateur de fichier \_ \_ \_** . Les handles de répertoires sont presque jamais utilisés : les applications de sauvegarde sont l’une des quelques applications qui les utilisent généralement.

Après l’ouverture de l’objet fichier pour les e/s asynchrones, une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) doit être correctement créée, initialisée et transmise à chaque appel à des fonctions telles que [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) et [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile). Gardez à l’esprit les points suivants lors de l’utilisation de la structure [**OVERLAPPED**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) dans des opérations de lecture et d’écriture asynchrones :

-   Ne libérez pas ou ne modifiez pas la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) ou la mémoire tampon de données tant que toutes les opérations d’e/s asynchrones n’ont pas été effectuées sur l’objet fichier.
-   Si vous déclarez votre pointeur vers la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) en tant que variable locale, ne quittez pas la fonction locale tant que toutes les opérations d’e/s asynchrones n’ont pas été effectuées sur l’objet fichier. Si la fonction locale est fermée prématurément, la structure **OVERLAPPED** est hors de portée et elle est inaccessible aux fonctions [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) ou [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) qu’elle rencontre en dehors de cette fonction.

Vous pouvez également créer un événement et placer le descripteur dans la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) ; les [fonctions Wait](/windows/desktop/Sync/wait-functions) peuvent ensuite être utilisées pour attendre que l’opération d’e/s se termine en attendant le handle d’événement.

Comme indiqué précédemment, lors de l’utilisation d’un descripteur asynchrone, les applications doivent faire attention au moment où il faut libérer des ressources associées à une opération d’e/s spécifiée sur ce handle. Si le descripteur est libéré prématurément, [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) ou [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) peut signaler de façon incorrecte que l’opération d’e/s est terminée. En outre, la fonction **WriteFile** retourne parfois **true** avec une valeur [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) de **\_ succès d’erreur**, même si elle utilise un handle asynchrone (qui peut également retourner **false** avec l' **erreur \_ e/s \_ en attente**). Les programmeurs habitués à la conception d’e/s synchrones vont généralement libérer des **ressources de tampon** de données à ce stade, car la **\_ réussite** et l’erreur signifient que l’opération est terminée. Toutefois, si les [ports de terminaison d’e/s](i-o-completion-ports.md) sont utilisés avec ce handle asynchrone, un paquet d’achèvement est également envoyé même si l’opération d’e/s a été effectuée immédiatement. En d’autres termes, si l’application libère des ressources après que **WriteFile** a retourné la **valeur true** avec une **erreur de \_ réussite** en plus de dans la routine de port de terminaison d’e/s, elle aura une condition d’erreur double. Dans cet exemple, il est recommandé de permettre à la routine de port de fin d’être entièrement responsable de toutes les opérations de libération pour ces ressources.

Le système ne conserve pas le pointeur de fichier sur les handles asynchrones des fichiers et des appareils qui prennent en charge les pointeurs de fichier (autrement dit, les périphériques de recherche). par conséquent, la position de fichier doit être passée aux fonctions de lecture et d’écriture dans les membres de données de décalage associés de la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . Pour plus d’informations, consultez [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) et [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile).

La position du pointeur de fichier pour un handle synchrone est conservée par le système lorsque les données sont lues ou écrites et peut également être mise à jour à l’aide de la fonction [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) ou [**SetFilePointerEx**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointerex) .

Une application peut également attendre le descripteur de fichier pour synchroniser l’achèvement d’une opération d’e/s, mais cela nécessite une extrême prudence. Chaque fois qu’une opération d’e/s démarre, le système d’exploitation définit le descripteur de fichier à l’état non signalé. À chaque fois qu’une opération d’e/s est terminée, le système d’exploitation définit le descripteur de fichier à l’état signalé. Par conséquent, si une application démarre deux opérations d’e/s et attend le descripteur de fichier, il n’existe aucun moyen de déterminer l’opération qui se termine lorsque le descripteur est défini sur l’état signalé. Si une application doit effectuer plusieurs opérations d’e/s asynchrones sur un seul fichier, elle doit attendre le handle d’événement dans la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) spécifique pour chaque opération d’e/s, plutôt que sur le descripteur de fichier commun.

Pour annuler toutes les opérations d’e/s asynchrones en attente, utilisez l’une des deux opérations suivantes :

-   [**CancelIo**](cancelio.md): cette fonction annule uniquement les opérations émises par le thread appelant pour le handle de fichier spécifié.
-   [**CancelIoEx**](cancelioex-func.md): cette fonction annule toutes les opérations émises par les threads pour le handle de fichier spécifié.

Utilisez [**CancelSynchronousIo**](cancelsynchronousio-func.md) pour annuler les opérations d’e/s synchrones en attente.

Les fonctions [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) et [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) permettent à une application de spécifier une routine à exécuter (consultez [**FileIOCompletionRoutine**](/windows/win32/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine)) lorsque la requête d’e/s asynchrone est terminée.

 

 
