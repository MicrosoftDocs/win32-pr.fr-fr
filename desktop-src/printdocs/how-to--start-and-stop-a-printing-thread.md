---
description: Cette rubrique décrit comment démarrer et arrêter le thread de traitement du travail d’impression.
ms.assetid: CA3A81D6-332F-4867-881F-AC6859A076CF
title: 'Comment : Démarrer et arrêter un thread d’impression'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9a47f81e384a135bb70e6deabefe15a3408a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210471"
---
# <a name="how-to-start-and-stop-a-printing-thread"></a>Comment : Démarrer et arrêter un thread d’impression

Cette rubrique décrit comment démarrer et arrêter le thread de traitement du travail d’impression.

## <a name="overview"></a>Vue d’ensemble

Pour empêcher les activités d’impression de bloquer la réponse de l’interface utilisateur, créez un thread distinct pour traiter le travail d’impression. Le thread qui est démarré lorsque le programme est démarré, est le thread qui gère les messages de fenêtre qui résultent de l’interaction de l’utilisateur, et est par conséquent le thread d’interface utilisateur. Le programme doit traiter ces messages sans délai pour que l’interface utilisateur réponde en temps utile à la souris et au clavier de l’utilisateur. Pour que le programme puisse répondre rapidement à ces messages, la quantité de traitement qui peut être effectuée pendant un message est limitée. Quand une demande de l’utilisateur requiert un traitement extensif, un thread différent doit effectuer ce traitement pour permettre au programme de traiter l’interaction utilisateur suivante.

Le traitement des données dans un thread distinct nécessite que le programme coordonne l’opération du thread d’interface utilisateur et du thread de traitement. Par exemple, pendant que le thread de traitement traite les données, le thread principal ne doit pas modifier ces données. Une façon de gérer cela consiste à utiliser des objets de synchronisation thread-safe tels que des sémaphores, des événements et des mutex.

En même temps, certaines interactions de l’utilisateur doivent être évitées pendant l’exécution du thread de traitement. Dans l’exemple de programme, les données d’application sont protégées et l’interaction de l’utilisateur est limitée en faisant en sorte que le traitement du travail d’impression soit géré par la boîte de dialogue de progression modale. Une boîte de dialogue modale empêche l’utilisateur d’interagir avec la fenêtre principale du programme, ce qui empêche l’utilisateur de modifier les données du programme d’application pendant que les données sont imprimées.

La seule action que l’utilisateur peut effectuer pendant le traitement d’un travail d’impression est d’annuler le travail d’impression. Cette restriction est signalée à l’utilisateur par la forme de curseur. Lorsque le curseur se trouve sur le bouton **Annuler** , un curseur en flèche s’affiche, indiquant que l’utilisateur peut cliquer sur ce bouton. Lorsque le curseur se trouve sur une autre partie de la zone de fenêtre du programme, un curseur d’attente s’affiche, ce qui indique que le programme est occupé et ne peut pas répondre aux entrées de l’utilisateur.

## <a name="creating-the-printing-thread-procedure"></a>Création de la procédure de thread d’impression

Nous vous recommandons d’inclure ces fonctionnalités pendant le traitement de l’impression.

-   **Le traitement de l’impression est divisé en étapes.**

    Vous pouvez diviser le traitement d’impression en étapes de traitement discrètes que vous pouvez interrompre si l’utilisateur clique sur le bouton **Annuler** . Cela est utile, car le traitement de l’impression peut inclure des opérations nécessitant de nombreuses ressources du processeur. Le fractionnement de ce traitement en étapes peut empêcher le traitement de l’impression de bloquer ou de retarder d’autres threads ou processus. Le fait de décomposer le traitement en étapes logiques permet également de mettre fin au traitement de l’impression à tout moment, afin que l’arrêt d’un travail d’impression avant la fin ne laisse aucune ressource orpheline.

    Il s’agit d’un exemple de liste d’étapes d’impression.

    ```C++
    HRESULT PrintStep_1_StartJob (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_2_DoOnePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_3_DoOneDoc (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_4_DoOnePage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_5_ClosePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_6_CloseJob (PPRINTTHREADINFO threadInfo);
    ```

    

-   **Rechercher un événement d’annulation entre les étapes**

    Quand l’utilisateur clique sur le bouton **Annuler** , le thread d’interface utilisateur signale l’événement d’annulation. Le thread de traitement doit vérifier régulièrement l’événement d’annulation pour savoir quand un utilisateur a cliqué sur le bouton **Annuler** . Les instructions [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) effectuent cette vérification et permettent également à d’autres programmes de s’exécuter afin que le traitement du travail d’impression ne bloque pas ou ne retarde pas d’autres threads ou processus.

    L’exemple de code suivant illustre l’un des tests pour voir si l’événement d’annulation s’est produit.

    ```C++
    waitStatus = WaitForSingleObject (
                    threadInfo->quitEvent, 
                    stepDelay);
    if (WAIT_OBJECT_0 == waitStatus)
    {
        hr = E_ABORT;
    }
    ```

    

-   **Envoyer des mises à jour d’État au thread d’interface utilisateur**

    À chaque étape de traitement d’impression, le thread de traitement d’impression envoie des messages de mise à jour à la boîte de dialogue d’avancement de l’impression afin qu’il puisse mettre à jour la barre de progression. Notez que la boîte de dialogue progression de l’impression s’exécute dans le thread d’interface utilisateur.

    L’exemple de code suivant illustre l’un des appels de message de mise à jour.

    ```C++
    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    ```

    

## <a name="starting-the-printing-thread"></a>Démarrage du thread d’impression

Le thread de traitement d’impression s’exécute jusqu’à ce que la fonction PrintThreadProc retourne. Les étapes suivantes démarrent le thread d’impression.

1.  **Préparez les éléments de données et d’interface utilisateur pour l’impression.**

    Avant de démarrer le thread de traitement d’impression, vous devez initialiser les éléments de données qui décrivent le travail d’impression et les éléments de l’interface utilisateur. Ces éléments incluent l’état du curseur, afin que le curseur d’attente s’affiche correctement. Vous devez également configurer la barre de progression pour refléter la taille du travail d’impression. Ces étapes de préparation sont décrites en détail dans [Guide pratique pour collecter des informations de travail d’impression auprès de l’utilisateur](preparing-to-print.md).

    L’exemple de code suivant montre comment configurer la barre de progression pour refléter la taille du travail d’impression que l’utilisateur a demandé.

    ```C++
    // Compute the number of steps in this job.
    stepCount = (((
                // One copy of a document contains
                //  one step for each page +
                //  one step for the document
                ((threadInfo->documentContent)->pages + 1) * 
                // Each copy of the document includes
                //  two steps to open and close the document
                threadInfo->copies) + 2) * 
                // Each job includes one step to start the job
                threadInfo->packages) + 1;
    // Send the total number of steps to the progress bar control.
    SendMessage (
        dlgInfo->progressBarWindow, 
        PBM_SETRANGE32, 
        0L, 
        (stepCount));
    ```

    

2.  **Démarrez le thread de traitement de l’impression.**

    Appelez [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) pour démarrer le thread de traitement.

    L’exemple de code suivant démarre le thread de traitement.

    ```C++
    // Start the printing thread
    threadInfo->printThreadHandle = CreateThread (
                    NULL, 
                    0L, 
                    (LPTHREAD_START_ROUTINE)PrintThreadProc,
                    (LPVOID)threadInfo, 
                    0L, 
                    &threadInfo->printThreadId);
    ```

    

3.  **Vérifiez si le démarrage du traitement de l’impression a échoué.**

    [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) retourne un handle au thread créé si le thread a été créé avec succès. La fonction PrintThreadProc qui a été démarrée dans le nouveau thread vérifie certaines conditions avant de démarrer le traitement réel du travail d’impression. S’il détecte des erreurs dans ces vérifications, PrintThreadProc peut retourner sans traiter les données du travail d’impression. Le thread d’interface utilisateur peut vérifier si le thread de traitement a démarré avec succès en attendant le handle de thread pendant une période plus longue que celle nécessaire pour effectuer les tests initiaux, mais pas plus longtemps que nécessaire. Lorsque le thread se termine, le handle du thread est signalé. Le code vérifie l’état du thread pendant un bref laps de temps après le démarrage du thread de traitement. La fonction [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) retourne lorsque le délai d’attente se produit ou que le handle de thread est signalé. Si la fonction **WaitForSingleObject** retourne un état d' **\_ objet wait \_ 0** , le thread s’est arrêté tôt et vous devez donc fermer la boîte de dialogue d’avancement de l’impression, comme le montre l’exemple de code suivant.

    ```C++
    // Make sure the printing thread started OK
    //  by waiting to see if it is still running after
    //  a short period of time. This time delay should be
    //  long enough to know that it's running but shorter
    //  than the shortest possible print job.
    waitStatus = WaitForSingleObject (
        threadInfo->printThreadHandle, 
        THREAD_START_WAIT);

    // If the object is signaled, that means that the
    //  thread terminated before the timeout period elapsed.
    if (WAIT_OBJECT_0 == waitStatus)
    {
        // The thread exited, so post close messages.
        PostMessage (hDlg, USER_PRINT_CLOSING, 0L, (LPARAM)E_FAIL);
        PostMessage (hDlg, USER_PRINT_COMPLETE, 0L, (LPARAM)E_FAIL);
    }
    ```

    

## <a name="stopping-the-printing-thread"></a>Arrêt du thread d’impression

Quand l’utilisateur clique sur le bouton **Annuler** dans la boîte de dialogue d’avancement de l’impression, le thread d’impression est notifié afin qu’il puisse arrêter le traitement du travail d’impression de manière ordonnée. Tandis que le bouton **Annuler** et l’événement **quitEvent** sont des aspects importants de ce traitement, vous devez concevoir l’intégralité de la séquence de traitement pour qu’elle soit interrompue avec succès. Cela signifie que les étapes de la séquence ne doivent pas quitter les ressources allouées qui ne sont pas libérées si un utilisateur annule la séquence avant qu’elle ne soit terminée.

L’exemple de code suivant montre comment l’exemple de programme vérifie le **quitEvent** avant de traiter chaque page du document en cours d’impression. Si le **quitEvent** est signalé ou si une erreur a été détectée, le traitement de l’impression s’arrête.


```C++
// While no errors and the user hasn't clicked cancel...
while (((waitStatus = WaitForSingleObject (
                        threadInfo->quitEvent, 
                        stepDelay)) == WAIT_TIMEOUT) &&
        SUCCEEDED(hr))
{
    // ...print one page
    hr = PrintStep_4_DoOnePage (threadInfo);

    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    

    if (threadInfo->currentPage < (threadInfo->documentContent)->pages)
    {
        // More pages, so continue to the next one
        threadInfo->currentPage++;
    }
    else
    {
        // Last page printed so exit loop and close
        break;
    }
}
```



 

 
