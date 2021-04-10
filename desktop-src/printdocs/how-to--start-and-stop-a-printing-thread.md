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
# <a name="how-to-start-and-stop-a-printing-thread"></a><span data-ttu-id="545b3-103">Comment : Démarrer et arrêter un thread d’impression</span><span class="sxs-lookup"><span data-stu-id="545b3-103">How To: Start and Stop a Printing Thread</span></span>

<span data-ttu-id="545b3-104">Cette rubrique décrit comment démarrer et arrêter le thread de traitement du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="545b3-104">This topic describes how to start and stop the print job processing thread.</span></span>

## <a name="overview"></a><span data-ttu-id="545b3-105">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="545b3-105">Overview</span></span>

<span data-ttu-id="545b3-106">Pour empêcher les activités d’impression de bloquer la réponse de l’interface utilisateur, créez un thread distinct pour traiter le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="545b3-106">To prevent printing activities from blocking the user interface response, create a separate thread to process the print job.</span></span> <span data-ttu-id="545b3-107">Le thread qui est démarré lorsque le programme est démarré, est le thread qui gère les messages de fenêtre qui résultent de l’interaction de l’utilisateur, et est par conséquent le thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="545b3-107">The thread that is started when the program is started, is the thread that handles the window messages that result from user interaction, and is therefore the UI thread.</span></span> <span data-ttu-id="545b3-108">Le programme doit traiter ces messages sans délai pour que l’interface utilisateur réponde en temps utile à la souris et au clavier de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="545b3-108">The program must process these messages without delay for the user interface to respond to the user's mouse and keyboard input in a timely manner.</span></span> <span data-ttu-id="545b3-109">Pour que le programme puisse répondre rapidement à ces messages, la quantité de traitement qui peut être effectuée pendant un message est limitée.</span><span class="sxs-lookup"><span data-stu-id="545b3-109">For the program to be able to respond to these messages quickly, the amount of processing that can be performed during any one message is limited.</span></span> <span data-ttu-id="545b3-110">Quand une demande de l’utilisateur requiert un traitement extensif, un thread différent doit effectuer ce traitement pour permettre au programme de traiter l’interaction utilisateur suivante.</span><span class="sxs-lookup"><span data-stu-id="545b3-110">When a user request requires extensive processing, a different thread must perform that processing to allow subsequent user interaction to be handled by the program.</span></span>

<span data-ttu-id="545b3-111">Le traitement des données dans un thread distinct nécessite que le programme coordonne l’opération du thread d’interface utilisateur et du thread de traitement.</span><span class="sxs-lookup"><span data-stu-id="545b3-111">Processing data in a separate thread requires the program to coordinate the operation of user interface thread and the processing thread.</span></span> <span data-ttu-id="545b3-112">Par exemple, pendant que le thread de traitement traite les données, le thread principal ne doit pas modifier ces données.</span><span class="sxs-lookup"><span data-stu-id="545b3-112">For example, while the processing thread is processing the data, the main thread must not alter that data.</span></span> <span data-ttu-id="545b3-113">Une façon de gérer cela consiste à utiliser des objets de synchronisation thread-safe tels que des sémaphores, des événements et des mutex.</span><span class="sxs-lookup"><span data-stu-id="545b3-113">One way to manage this is through thread-safe synchronization objects such as semaphores, events, and mutexes.</span></span>

<span data-ttu-id="545b3-114">En même temps, certaines interactions de l’utilisateur doivent être évitées pendant l’exécution du thread de traitement.</span><span class="sxs-lookup"><span data-stu-id="545b3-114">At the same time, some user interaction must be prevented while the processing thread is running.</span></span> <span data-ttu-id="545b3-115">Dans l’exemple de programme, les données d’application sont protégées et l’interaction de l’utilisateur est limitée en faisant en sorte que le traitement du travail d’impression soit géré par la boîte de dialogue de progression modale.</span><span class="sxs-lookup"><span data-stu-id="545b3-115">In the sample program, the application data is protected and the user interaction is limited by having the print job processing be managed by the modal progress dialog box.</span></span> <span data-ttu-id="545b3-116">Une boîte de dialogue modale empêche l’utilisateur d’interagir avec la fenêtre principale du programme, ce qui empêche l’utilisateur de modifier les données du programme d’application pendant que les données sont imprimées.</span><span class="sxs-lookup"><span data-stu-id="545b3-116">A modal dialog box prevents the user from interacting with the program's main window, which prevents the user from altering the application program data while the data is printed.</span></span>

<span data-ttu-id="545b3-117">La seule action que l’utilisateur peut effectuer pendant le traitement d’un travail d’impression est d’annuler le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="545b3-117">The only action the user can perform while a print job is processing is to cancel the print job.</span></span> <span data-ttu-id="545b3-118">Cette restriction est signalée à l’utilisateur par la forme de curseur.</span><span class="sxs-lookup"><span data-stu-id="545b3-118">This restriction is signaled to the user by the cursor shape.</span></span> <span data-ttu-id="545b3-119">Lorsque le curseur se trouve sur le bouton **Annuler** , un curseur en flèche s’affiche, indiquant que l’utilisateur peut cliquer sur ce bouton.</span><span class="sxs-lookup"><span data-stu-id="545b3-119">When the cursor is over the **Cancel** button, an arrow cursor is displayed, which indicates that the user can click this button.</span></span> <span data-ttu-id="545b3-120">Lorsque le curseur se trouve sur une autre partie de la zone de fenêtre du programme, un curseur d’attente s’affiche, ce qui indique que le programme est occupé et ne peut pas répondre aux entrées de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="545b3-120">When the cursor is over any other part of the program's window area, a wait cursor is displayed, which indicates that the program is busy and cannot respond to user input.</span></span>

## <a name="creating-the-printing-thread-procedure"></a><span data-ttu-id="545b3-121">Création de la procédure de thread d’impression</span><span class="sxs-lookup"><span data-stu-id="545b3-121">Creating the Printing Thread Procedure</span></span>

<span data-ttu-id="545b3-122">Nous vous recommandons d’inclure ces fonctionnalités pendant le traitement de l’impression.</span><span class="sxs-lookup"><span data-stu-id="545b3-122">We recommend including these features while print processing.</span></span>

-   <span data-ttu-id="545b3-123">**Le traitement de l’impression est divisé en étapes.**</span><span class="sxs-lookup"><span data-stu-id="545b3-123">**Print processing is divided into steps**</span></span>

    <span data-ttu-id="545b3-124">Vous pouvez diviser le traitement d’impression en étapes de traitement discrètes que vous pouvez interrompre si l’utilisateur clique sur le bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="545b3-124">You can divide the print processing into discrete processing steps that you can interrupt if the user clicks the **Cancel** button.</span></span> <span data-ttu-id="545b3-125">Cela est utile, car le traitement de l’impression peut inclure des opérations nécessitant de nombreuses ressources du processeur.</span><span class="sxs-lookup"><span data-stu-id="545b3-125">This is useful because print processing can include processor-intensive operations.</span></span> <span data-ttu-id="545b3-126">Le fractionnement de ce traitement en étapes peut empêcher le traitement de l’impression de bloquer ou de retarder d’autres threads ou processus.</span><span class="sxs-lookup"><span data-stu-id="545b3-126">Breaking this processing into steps can prevent the print processing from blocking or delaying other threads or processes.</span></span> <span data-ttu-id="545b3-127">Le fait de décomposer le traitement en étapes logiques permet également de mettre fin au traitement de l’impression à tout moment, afin que l’arrêt d’un travail d’impression avant la fin ne laisse aucune ressource orpheline.</span><span class="sxs-lookup"><span data-stu-id="545b3-127">Breaking the processing into logical steps also makes it possible to cleanly terminate the print processing at any point, so that ending a print job before it has finished will not leave any orphaned resources.</span></span>

    <span data-ttu-id="545b3-128">Il s’agit d’un exemple de liste d’étapes d’impression.</span><span class="sxs-lookup"><span data-stu-id="545b3-128">This is an example list of print steps.</span></span>

    ```C++
    HRESULT PrintStep_1_StartJob (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_2_DoOnePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_3_DoOneDoc (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_4_DoOnePage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_5_ClosePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_6_CloseJob (PPRINTTHREADINFO threadInfo);
    ```

    

-   <span data-ttu-id="545b3-129">**Rechercher un événement d’annulation entre les étapes**</span><span class="sxs-lookup"><span data-stu-id="545b3-129">**Check for a cancel event between steps**</span></span>

    <span data-ttu-id="545b3-130">Quand l’utilisateur clique sur le bouton **Annuler** , le thread d’interface utilisateur signale l’événement d’annulation.</span><span class="sxs-lookup"><span data-stu-id="545b3-130">When the user clicks the **Cancel** button, the user interface thread signals the cancel event.</span></span> <span data-ttu-id="545b3-131">Le thread de traitement doit vérifier régulièrement l’événement d’annulation pour savoir quand un utilisateur a cliqué sur le bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="545b3-131">The processing thread must check the cancel event periodically to know when a user clicked the **Cancel** button.</span></span> <span data-ttu-id="545b3-132">Les instructions [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) effectuent cette vérification et permettent également à d’autres programmes de s’exécuter afin que le traitement du travail d’impression ne bloque pas ou ne retarde pas d’autres threads ou processus.</span><span class="sxs-lookup"><span data-stu-id="545b3-132">The [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) statements perform this check and they also give other programs a chance to run so that the print job processing doesn't block or delay other threads or processes.</span></span>

    <span data-ttu-id="545b3-133">L’exemple de code suivant illustre l’un des tests pour voir si l’événement d’annulation s’est produit.</span><span class="sxs-lookup"><span data-stu-id="545b3-133">The following code example illustrates one of the tests to see whether the cancel event has occurred.</span></span>

    ```C++
    waitStatus = WaitForSingleObject (
                    threadInfo->quitEvent, 
                    stepDelay);
    if (WAIT_OBJECT_0 == waitStatus)
    {
        hr = E_ABORT;
    }
    ```

    

-   <span data-ttu-id="545b3-134">**Envoyer des mises à jour d’État au thread d’interface utilisateur**</span><span class="sxs-lookup"><span data-stu-id="545b3-134">**Send status updates to user interface thread**</span></span>

    <span data-ttu-id="545b3-135">À chaque étape de traitement d’impression, le thread de traitement d’impression envoie des messages de mise à jour à la boîte de dialogue d’avancement de l’impression afin qu’il puisse mettre à jour la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="545b3-135">As each print processing step, the print processing thread sends update messages to the print progress dialog box so that it can update the progress bar.</span></span> <span data-ttu-id="545b3-136">Notez que la boîte de dialogue progression de l’impression s’exécute dans le thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="545b3-136">Note that the print progress dialog box is running in the UI thread.</span></span>

    <span data-ttu-id="545b3-137">L’exemple de code suivant illustre l’un des appels de message de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="545b3-137">The following code example illustrates one of the update message calls.</span></span>

    ```C++
    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    ```

    

## <a name="starting-the-printing-thread"></a><span data-ttu-id="545b3-138">Démarrage du thread d’impression</span><span class="sxs-lookup"><span data-stu-id="545b3-138">Starting the Printing Thread</span></span>

<span data-ttu-id="545b3-139">Le thread de traitement d’impression s’exécute jusqu’à ce que la fonction PrintThreadProc retourne.</span><span class="sxs-lookup"><span data-stu-id="545b3-139">The print processing thread runs until the PrintThreadProc function returns.</span></span> <span data-ttu-id="545b3-140">Les étapes suivantes démarrent le thread d’impression.</span><span class="sxs-lookup"><span data-stu-id="545b3-140">The following steps start the printing thread.</span></span>

1.  <span data-ttu-id="545b3-141">**Préparez les éléments de données et d’interface utilisateur pour l’impression.**</span><span class="sxs-lookup"><span data-stu-id="545b3-141">**Prepare the data and user interface elements for printing.**</span></span>

    <span data-ttu-id="545b3-142">Avant de démarrer le thread de traitement d’impression, vous devez initialiser les éléments de données qui décrivent le travail d’impression et les éléments de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="545b3-142">Before starting the print processing thread, you must initialize the data elements that describe the print job and the user interface elements.</span></span> <span data-ttu-id="545b3-143">Ces éléments incluent l’état du curseur, afin que le curseur d’attente s’affiche correctement.</span><span class="sxs-lookup"><span data-stu-id="545b3-143">These elements include the cursor state, so that the wait cursor will be displayed appropriately.</span></span> <span data-ttu-id="545b3-144">Vous devez également configurer la barre de progression pour refléter la taille du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="545b3-144">You must also configure the progress bar to reflect the size of the print job.</span></span> <span data-ttu-id="545b3-145">Ces étapes de préparation sont décrites en détail dans [Guide pratique pour collecter des informations de travail d’impression auprès de l’utilisateur](preparing-to-print.md).</span><span class="sxs-lookup"><span data-stu-id="545b3-145">These preparation steps are described in detail in [How To: Collect Print Job Information from the User](preparing-to-print.md).</span></span>

    <span data-ttu-id="545b3-146">L’exemple de code suivant montre comment configurer la barre de progression pour refléter la taille du travail d’impression que l’utilisateur a demandé.</span><span class="sxs-lookup"><span data-stu-id="545b3-146">The following code example shows how to configure the progress bar to reflect the size of the print job that the user requested.</span></span>

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

    

2.  <span data-ttu-id="545b3-147">**Démarrez le thread de traitement de l’impression.**</span><span class="sxs-lookup"><span data-stu-id="545b3-147">**Start the print processing thread.**</span></span>

    <span data-ttu-id="545b3-148">Appelez [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) pour démarrer le thread de traitement.</span><span class="sxs-lookup"><span data-stu-id="545b3-148">Call [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) to start the processing thread.</span></span>

    <span data-ttu-id="545b3-149">L’exemple de code suivant démarre le thread de traitement.</span><span class="sxs-lookup"><span data-stu-id="545b3-149">The following code example starts the processing thread.</span></span>

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

    

3.  <span data-ttu-id="545b3-150">**Vérifiez si le démarrage du traitement de l’impression a échoué.**</span><span class="sxs-lookup"><span data-stu-id="545b3-150">**Check whether print processing failed on start.**</span></span>

    <span data-ttu-id="545b3-151">[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) retourne un handle au thread créé si le thread a été créé avec succès.</span><span class="sxs-lookup"><span data-stu-id="545b3-151">[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) returns a handle to the created thread if the thread was created successfully.</span></span> <span data-ttu-id="545b3-152">La fonction PrintThreadProc qui a été démarrée dans le nouveau thread vérifie certaines conditions avant de démarrer le traitement réel du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="545b3-152">The PrintThreadProc function that was started in the new thread checks some conditions before it starts the actual print job processing.</span></span> <span data-ttu-id="545b3-153">S’il détecte des erreurs dans ces vérifications, PrintThreadProc peut retourner sans traiter les données du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="545b3-153">If it detects any errors in these checks, PrintThreadProc could return without processing any print job data.</span></span> <span data-ttu-id="545b3-154">Le thread d’interface utilisateur peut vérifier si le thread de traitement a démarré avec succès en attendant le handle de thread pendant une période plus longue que celle nécessaire pour effectuer les tests initiaux, mais pas plus longtemps que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="545b3-154">The UI thread can check whether the processing thread started successfully by waiting on the thread handle for a period of time that is longer than it takes to perform the initial tests but no longer than necessary.</span></span> <span data-ttu-id="545b3-155">Lorsque le thread se termine, le handle du thread est signalé.</span><span class="sxs-lookup"><span data-stu-id="545b3-155">When the thread exits, the handle to the thread becomes signaled.</span></span> <span data-ttu-id="545b3-156">Le code vérifie l’état du thread pendant un bref laps de temps après le démarrage du thread de traitement.</span><span class="sxs-lookup"><span data-stu-id="545b3-156">The code checks the thread's state for a short period of time after it starts the processing thread.</span></span> <span data-ttu-id="545b3-157">La fonction [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) retourne lorsque le délai d’attente se produit ou que le handle de thread est signalé.</span><span class="sxs-lookup"><span data-stu-id="545b3-157">The [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function returns when either the timeout occurs or the thread handle is signaled.</span></span> <span data-ttu-id="545b3-158">Si la fonction **WaitForSingleObject** retourne un état d' **\_ objet wait \_ 0** , le thread s’est arrêté tôt et vous devez donc fermer la boîte de dialogue d’avancement de l’impression, comme le montre l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="545b3-158">If the **WaitForSingleObject** function returns a **WAIT\_OBJECT\_0** status, the thread exited early and so you should close the print progress dialog, as the following code example shows.</span></span>

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

    

## <a name="stopping-the-printing-thread"></a><span data-ttu-id="545b3-159">Arrêt du thread d’impression</span><span class="sxs-lookup"><span data-stu-id="545b3-159">Stopping the Printing Thread</span></span>

<span data-ttu-id="545b3-160">Quand l’utilisateur clique sur le bouton **Annuler** dans la boîte de dialogue d’avancement de l’impression, le thread d’impression est notifié afin qu’il puisse arrêter le traitement du travail d’impression de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="545b3-160">When the user clicks the **Cancel** button in the print progress dialog box, the printing thread is notified so that it can stop processing the print job in an orderly manner.</span></span> <span data-ttu-id="545b3-161">Tandis que le bouton **Annuler** et l’événement **quitEvent** sont des aspects importants de ce traitement, vous devez concevoir l’intégralité de la séquence de traitement pour qu’elle soit interrompue avec succès.</span><span class="sxs-lookup"><span data-stu-id="545b3-161">While the **Cancel** button and the **quitEvent** event are important aspects of this processing, you must design the entire processing sequence to be interrupted successfully.</span></span> <span data-ttu-id="545b3-162">Cela signifie que les étapes de la séquence ne doivent pas quitter les ressources allouées qui ne sont pas libérées si un utilisateur annule la séquence avant qu’elle ne soit terminée.</span><span class="sxs-lookup"><span data-stu-id="545b3-162">This means that the steps in the sequence must not leave any allocated resources that are not freed if a user cancels the sequence before it had completed.</span></span>

<span data-ttu-id="545b3-163">L’exemple de code suivant montre comment l’exemple de programme vérifie le **quitEvent** avant de traiter chaque page du document en cours d’impression.</span><span class="sxs-lookup"><span data-stu-id="545b3-163">The following code example shows how the sample program checks the **quitEvent** before it processes each page in the document being printed.</span></span> <span data-ttu-id="545b3-164">Si le **quitEvent** est signalé ou si une erreur a été détectée, le traitement de l’impression s’arrête.</span><span class="sxs-lookup"><span data-stu-id="545b3-164">If the **quitEvent** is signaled or an error was detected, print processing stops.</span></span>


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



 

 
