---
description: Le fait de permettre aux utilisateurs d’annuler les demandes d’e/s qui sont lentes ou bloquées peut améliorer la convivialité et la robustesse de votre application.
ms.assetid: adfe6d05-f30b-40a1-b3b0-58e2593e7b25
title: Annulation d’opérations d’e/s en attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d108409eea32cf18a94f83bf7aacd282c60d3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545096"
---
# <a name="canceling-pending-io-operations"></a><span data-ttu-id="c3b22-103">Annulation d’opérations d’e/s en attente</span><span class="sxs-lookup"><span data-stu-id="c3b22-103">Canceling Pending I/O Operations</span></span>

<span data-ttu-id="c3b22-104">Le fait de permettre aux utilisateurs d’annuler les demandes d’e/s qui sont lentes ou bloquées peut améliorer la convivialité et la robustesse de votre application.</span><span class="sxs-lookup"><span data-stu-id="c3b22-104">Allowing users to cancel I/O requests that are slow or blocked can enhance the usability and robustness of your application.</span></span> <span data-ttu-id="c3b22-105">Par exemple, si un appel à la fonction [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) est bloqué en raison de l’appel à un appareil très lent, l’annulation permet à l’appel d’être relancé, avec de nouveaux paramètres, sans arrêter l’application.</span><span class="sxs-lookup"><span data-stu-id="c3b22-105">For example, if a call to the [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) function is blocked because the call is to a very slow device, canceling it enables the call to be made again, with new parameters, without terminating the application.</span></span>

<span data-ttu-id="c3b22-106">Windows Vista étend les fonctionnalités d’annulation et prend en charge l’annulation des opérations synchrones.</span><span class="sxs-lookup"><span data-stu-id="c3b22-106">Windows Vista extends the cancellation capabilities and includes support for canceling synchronous operations.</span></span>

<span data-ttu-id="c3b22-107">**Remarque**  L’appel de la fonction [**CancelIoEx**](cancelioex-func.md) ne garantit pas qu’une opération d’e/s sera annulée ; le pilote qui gère l’opération doit prendre en charge l’annulation et l’opération doit être dans un État qui peut être annulé.</span><span class="sxs-lookup"><span data-stu-id="c3b22-107">**Note**  Calling the [**CancelIoEx**](cancelioex-func.md) function does not guarantee that an I/O operation will be canceled; the driver which is handling the operation must support cancellation and the operation must be in a state that can be canceled.</span></span>

## <a name="cancellation-considerations"></a><span data-ttu-id="c3b22-108">Considérations relatives à l’annulation</span><span class="sxs-lookup"><span data-stu-id="c3b22-108">Cancellation Considerations</span></span>

<span data-ttu-id="c3b22-109">Quand vous programmez des appels d’annulation, gardez à l’esprit les considérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c3b22-109">When programming cancellation calls, keep in mind the following considerations:</span></span>

-   <span data-ttu-id="c3b22-110">Il n’existe aucune garantie que les pilotes sous-jacents prennent en charge l’annulation correctement.</span><span class="sxs-lookup"><span data-stu-id="c3b22-110">There is no guarantee that underlying drivers correctly support cancellation.</span></span>
-   <span data-ttu-id="c3b22-111">Lors de l’annulation des e/s asynchrones, quand aucune structure OVERLAPPED n’est fournie à la fonction [**CancelIoEx**](cancelioex-func.md) , la fonction tente d’annuler toutes les e/s en suspens sur le fichier sur tous les threads du processus.</span><span class="sxs-lookup"><span data-stu-id="c3b22-111">When canceling asynchronous I/O, when no overlapped structure is supplied to the [**CancelIoEx**](cancelioex-func.md) function, the function attempts to cancel all outstanding I/O on the file on all threads in the process.</span></span> <span data-ttu-id="c3b22-112">Chaque thread est traité individuellement. par conséquent, une fois qu’un thread a été traité, il peut démarrer une autre e/s sur le fichier avant que les e/s de tous les autres threads aient été annulées, provoquant des problèmes de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="c3b22-112">Each thread is processed individually, so after a thread has been processed it may start another I/O on the file before all the other threads have had their I/O for the file canceled, causing synchronization issues.</span></span>
-   <span data-ttu-id="c3b22-113">Lorsque vous annulez des e/s asynchrones, ne réutilisez pas les structures avec chevauchement ciblées avec l’annulation ciblée.</span><span class="sxs-lookup"><span data-stu-id="c3b22-113">When canceling asynchronous I/O, do not reuse overlapped structures with targeted cancellation.</span></span> <span data-ttu-id="c3b22-114">Une fois l’opération d’e/s terminée (avec succès ou avec un état annulé), la structure OVERLAPPED n’est plus utilisée par le système et peut être réutilisée.</span><span class="sxs-lookup"><span data-stu-id="c3b22-114">Once the I/O operation completes (either successfully or with a canceled status) then the overlapped structure is no longer in use by the system and can be reused.</span></span>
-   <span data-ttu-id="c3b22-115">Lors de l’annulation des e/s synchrones, l’appel de la fonction [**CancelSynchronousIo**](cancelsynchronousio-func.md) tente d’annuler tout appel synchrone en cours sur le thread.</span><span class="sxs-lookup"><span data-stu-id="c3b22-115">When canceling synchronous I/O, calling the [**CancelSynchronousIo**](cancelsynchronousio-func.md) function attempts to cancel any current synchronous call on the thread.</span></span> <span data-ttu-id="c3b22-116">Vous devez veiller à ce que la synchronisation des appels soit correcte. l’appel incorrect dans une série d’appels peut être annulé.</span><span class="sxs-lookup"><span data-stu-id="c3b22-116">You must take care to ensure the synchronization of the calls is correct; the wrong call in a series of calls could get canceled.</span></span> <span data-ttu-id="c3b22-117">Par exemple, si la fonction **CancelSynchronousIo** est appelée pour une opération synchrone, x, l’opération Y démarre uniquement après que l’opération x est terminée (normalement ou avec une erreur).</span><span class="sxs-lookup"><span data-stu-id="c3b22-117">For example, if the **CancelSynchronousIo** function is called for a synchronous operation, X, operation Y only starts after that operation X is completed (normally or with an error).</span></span> <span data-ttu-id="c3b22-118">Si le thread qui a appelé l’opération X démarre un autre appel synchrone à X, l’appel Cancel peut interrompre cette nouvelle requête d’e/s.</span><span class="sxs-lookup"><span data-stu-id="c3b22-118">If the thread that called operation X then starts another synchronous call to X, the cancel call could interrupt this new I/O request.</span></span>
-   <span data-ttu-id="c3b22-119">Lorsque vous annulez des e/s synchrones, sachez qu’une condition de concurrence peut exister chaque fois qu’un thread est partagé entre différentes parties d’une application, par exemple, avec un thread de pool de threads.</span><span class="sxs-lookup"><span data-stu-id="c3b22-119">When canceling synchronous I/O, be aware that a race condition can exist whenever a thread is shared between different parts of an application, for example, with a thread-pool thread.</span></span>

## <a name="operations-that-cannot-be-canceled"></a><span data-ttu-id="c3b22-120">Opérations qui ne peuvent pas être annulées</span><span class="sxs-lookup"><span data-stu-id="c3b22-120">Operations That Cannot Be Canceled</span></span>

<span data-ttu-id="c3b22-121">Certaines fonctions ne peuvent pas être annulées à l’aide de la fonction [**CancelIo**](cancelio.md), [**CancelIoEx**](cancelioex-func.md)ou [**CancelSynchronousIo**](cancelsynchronousio-func.md) .</span><span class="sxs-lookup"><span data-stu-id="c3b22-121">Some functions cannot be canceled using the [**CancelIo**](cancelio.md), [**CancelIoEx**](cancelioex-func.md), or [**CancelSynchronousIo**](cancelsynchronousio-func.md) function.</span></span> <span data-ttu-id="c3b22-122">Certaines de ces fonctions ont été étendues pour permettre l’annulation (par exemple, la fonction [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) ) et vous devez les utiliser à la place.</span><span class="sxs-lookup"><span data-stu-id="c3b22-122">Some of these functions have been extended to allow cancellation (for example, the [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) function) and you should use these instead.</span></span> <span data-ttu-id="c3b22-123">Outre la prise en charge de l’annulation, ces fonctions disposent également de rappels intégrés pour vous aider à suivre la progression de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c3b22-123">In addition to supporting cancellation, these functions also have built-in callbacks to support you when tracking the progress of the operation.</span></span> <span data-ttu-id="c3b22-124">Les fonctions suivantes ne prennent pas en charge l’annulation :</span><span class="sxs-lookup"><span data-stu-id="c3b22-124">The following functions do not support cancellation:</span></span>

-   <span data-ttu-id="c3b22-125">[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)— utilisez [ **CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)</span><span class="sxs-lookup"><span data-stu-id="c3b22-125">[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)—use [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)</span></span>
-   <span data-ttu-id="c3b22-126">[**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile): utilisez [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span><span class="sxs-lookup"><span data-stu-id="c3b22-126">[**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)—use [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span></span>
-   <span data-ttu-id="c3b22-127">[**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa): utilisez [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span><span class="sxs-lookup"><span data-stu-id="c3b22-127">[**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)—use [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span></span>
-   [<span data-ttu-id="c3b22-128">**ReplaceFile**</span><span class="sxs-lookup"><span data-stu-id="c3b22-128">**ReplaceFile**</span></span>](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

<span data-ttu-id="c3b22-129">Pour plus d’informations, consultez [instructions d’achèvement/annulation d’e/s](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span><span class="sxs-lookup"><span data-stu-id="c3b22-129">For more information, see [I/O Completion/Cancellation Guidelines](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span></span>

## <a name="canceling-asynchronous-io"></a><span data-ttu-id="c3b22-130">Annulation d’e/s asynchrones</span><span class="sxs-lookup"><span data-stu-id="c3b22-130">Canceling Asynchronous I/O</span></span>

<span data-ttu-id="c3b22-131">Vous pouvez annuler des e/s asynchrones à partir de n’importe quel thread du processus qui a émis l’opération d’e/s.</span><span class="sxs-lookup"><span data-stu-id="c3b22-131">You can cancel asynchronous I/O from any thread in the process that issued the I/O operation.</span></span> <span data-ttu-id="c3b22-132">Vous devez spécifier le descripteur sur lequel l’e/s a été exécutée et, éventuellement, la structure OVERLAPPED qui a été utilisée pour effectuer les e/s.</span><span class="sxs-lookup"><span data-stu-id="c3b22-132">You must specify the handle which the I/O was performed on and, optionally, the overlapped structure that was used to perform the I/O.</span></span> <span data-ttu-id="c3b22-133">Vous pouvez déterminer si l’annulation s’est produite en examinant l’état retourné dans la structure OVERLAPPED ou dans le rappel d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="c3b22-133">You can determine if the cancel occurred by examining the status returned in the overlapped structure or in the completion callback.</span></span> <span data-ttu-id="c3b22-134">L’état **erreur \_ opération \_ abandonnée** indique que l’opération a été annulée.</span><span class="sxs-lookup"><span data-stu-id="c3b22-134">A status of **ERROR\_OPERATION\_ABORTED** indicates that the operation was canceled.</span></span>

<span data-ttu-id="c3b22-135">L’exemple suivant montre une routine qui prend un délai d’attente et tente une opération de lecture, en l’annulant avec la fonction [**CancelIoEx**](cancelioex-func.md) si le délai d’attente expire.</span><span class="sxs-lookup"><span data-stu-id="c3b22-135">The following example shows a routine that takes a timeout and attempts a read operation, canceling it with the [**CancelIoEx**](cancelioex-func.md) function if the timeout expires.</span></span>


```C++
#include <windows.h>

BOOL DoCancelableRead(HANDLE hFile,
                 LPVOID lpBuffer,
                 DWORD nNumberOfBytesToRead,
                 LPDWORD lpNumberOfBytesRead,
                 LPOVERLAPPED lpOverlapped,
                 DWORD dwTimeout,
                 LPBOOL pbCancelCalled)
//
// Parameters:
//
//      hFile - An open handle to a readable file or device.
//
//      lpBuffer - A pointer to the buffer to store the data being read.
//
//      nNumberOfBytesToRead - The number of bytes to read from the file or 
//          device. Must be less than or equal to the actual size of
//          the buffer referenced by lpBuffer.
//
//      lpNumberOfBytesRead - A pointer to a DWORD to receive the number 
//          of bytes read after all I/O is complete or canceled.
//
//      lpOverlapped - A pointer to a preconfigured OVERLAPPED structure that
//          has a valid hEvent.
//          If the caller does not properly initialize this structure, this
//          routine will fail.
//
//      dwTimeout - The desired time-out, in milliseconds, for the I/O read.
//          After this time expires, the I/O is canceled.
// 
//      pbCancelCalled - A pointer to a Boolean to notify the caller if this
//          routine attempted to perform an I/O cancel.
//
// Return Value:
//
//      TRUE on success, FALSE on failure.
//
{
    BOOL result;
    DWORD waitTimer;
    BOOL bIoComplete = FALSE;
    const DWORD PollInterval = 100; // milliseconds

    // Initialize "out" parameters
    *pbCancelCalled = FALSE;
    *lpNumberOfBytesRead = 0;

    // Perform the I/O, in this case a read operation.
    result = ReadFile(hFile,
                  lpBuffer,
                  nNumberOfBytesToRead,
                  lpNumberOfBytesRead,
                  lpOverlapped );

    if (result == FALSE) 
    {
        if (GetLastError() != ERROR_IO_PENDING) 
        {
            // The function call failed. ToDo: Error logging and recovery.
            return FALSE; 
        }
    } 
    else 
    {
        // The I/O completed, done.
        return TRUE;
    }
        
    // The I/O is pending, so wait and see if the call times out.
    // If so, cancel the I/O using the CancelIoEx function.

    for (waitTimer = 0; waitTimer < dwTimeout; waitTimer += PollInterval)
    {
        result = GetOverlappedResult( hFile, lpOverlapped, lpNumberOfBytesRead, FALSE );
        if (result == FALSE)
        {
            if (GetLastError() != ERROR_IO_PENDING)
            {
                // The function call failed. ToDo: Error logging and recovery.
                return FALSE;
            }
            Sleep(PollInterval);
        }
        else
        {
            bIoComplete = TRUE;
            break;
        }
    }

    if (bIoComplete == FALSE) 
    {
        result = CancelIoEx( hFile, lpOverlapped );
        
        *pbCancelCalled = TRUE;

        if (result == TRUE || GetLastError() != ERROR_NOT_FOUND) 
        {
            // Wait for the I/O subsystem to acknowledge our cancellation.
            // Depending on the timing of the calls, the I/O might complete with a
            // cancellation status, or it might complete normally (if the ReadFile was
            // in the process of completing at the time CancelIoEx was called, or if
            // the device does not support cancellation).
            // This call specifies TRUE for the bWait parameter, which will block
            // until the I/O either completes or is canceled, thus resuming execution, 
            // provided the underlying device driver and associated hardware are functioning 
            // properly. If there is a problem with the driver it is better to stop 
            // responding here than to try to continue while masking the problem.

            result = GetOverlappedResult( hFile, lpOverlapped, lpNumberOfBytesRead, TRUE );

            // ToDo: check result and log errors. 
        }
    }

    return result;
}
```



## <a name="canceling-synchronous-io"></a><span data-ttu-id="c3b22-136">Annulation des e/s synchrones</span><span class="sxs-lookup"><span data-stu-id="c3b22-136">Canceling Synchronous I/O</span></span>

<span data-ttu-id="c3b22-137">Vous pouvez annuler des e/s synchrones à partir de n’importe quel thread du processus qui a émis l’opération d’e/s.</span><span class="sxs-lookup"><span data-stu-id="c3b22-137">You can cancel synchronous I/O from any thread in the process that issued the I/O operation.</span></span> <span data-ttu-id="c3b22-138">Vous devez spécifier le descripteur du thread qui effectue actuellement l’opération d’e/s.</span><span class="sxs-lookup"><span data-stu-id="c3b22-138">You must specify the handle to the thread which is currently performing the I/O operation.</span></span>

<span data-ttu-id="c3b22-139">L’exemple suivant illustre deux routines :</span><span class="sxs-lookup"><span data-stu-id="c3b22-139">The following example shows two routines:</span></span>

-   <span data-ttu-id="c3b22-140">La fonction **SynchronousIoWorker** est un thread de travail qui implémente des e/s de fichier synchrones, en commençant par un appel à la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="c3b22-140">The **SynchronousIoWorker** function is a worker thread that implements some synchronous file I/O, starting with a call to the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="c3b22-141">Si la routine est réussie, la routine peut être suivie d’opérations supplémentaires, qui ne sont pas incluses ici.</span><span class="sxs-lookup"><span data-stu-id="c3b22-141">If the routine is successful, the routine can be followed by additional operations, which are not included here.</span></span> <span data-ttu-id="c3b22-142">La variable globale *gCompletionStatus* peut être utilisée pour déterminer si toutes les opérations ont réussi ou si une opération a échoué ou a été annulée.</span><span class="sxs-lookup"><span data-stu-id="c3b22-142">The global variable *gCompletionStatus* can be used to determine whether all operations succeeded or whether an operation failed or was canceled.</span></span> <span data-ttu-id="c3b22-143">La variable globale *dwOperationInProgress* indique si les e/s de fichier sont toujours en cours.</span><span class="sxs-lookup"><span data-stu-id="c3b22-143">The global variable *dwOperationInProgress* indicates whether file I/O is still in progress.</span></span>

    <span data-ttu-id="c3b22-144">**Remarque**  Dans cet exemple, le thread d’interface utilisateur peut également vérifier l’existence du thread de travail.</span><span class="sxs-lookup"><span data-stu-id="c3b22-144">**Note**  In this example, the UI thread could also check for the existence of the worker thread.</span></span>

    <span data-ttu-id="c3b22-145">Des vérifications manuelles supplémentaires, qui ne sont pas incluses ici, sont nécessaires dans la fonction **SynchronousIoWorker** pour s’assurer que si l’annulation a été demandée pendant les courtes périodes entre les appels d’e/s de fichier, les autres opérations seront annulées.</span><span class="sxs-lookup"><span data-stu-id="c3b22-145">Additional manual checks, which are not included here, are required in the **SynchronousIoWorker** function is to ensure that if the cancellation was requested during the brief periods between file I/O calls, the rest of the operations will be canceled.</span></span>

-   <span data-ttu-id="c3b22-146">La fonction **MainUIThreadMessageHandler** simule le gestionnaire de messages dans la procédure de fenêtre d’un thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c3b22-146">The **MainUIThreadMessageHandler** function simulates the message handler within a UI thread's window procedure.</span></span> <span data-ttu-id="c3b22-147">L’utilisateur demande un ensemble d’opérations de fichier synchrones en cliquant sur un contrôle, ce qui génère un message de fenêtre défini par l’utilisateur, (dans la section marquée par **WM \_ MYSYNCOPS**).</span><span class="sxs-lookup"><span data-stu-id="c3b22-147">The user requests a set of synchronous file operations by clicking a control, which generates a user-defined window message, (in the section marked by **WM\_MYSYNCOPS**).</span></span> <span data-ttu-id="c3b22-148">Cela crée un nouveau thread à l’aide de la fonction **CreateFileThread** , qui démarre ensuite la fonction **SynchronousIoWorker** est.</span><span class="sxs-lookup"><span data-stu-id="c3b22-148">This creates a new thread using the **CreateFileThread** function, which then starts the **SynchronousIoWorker** function is.</span></span> <span data-ttu-id="c3b22-149">Le thread d’interface utilisateur continue de traiter les messages pendant que le thread de travail effectue l’e/s demandée.</span><span class="sxs-lookup"><span data-stu-id="c3b22-149">The UI thread continues to process messages while the worker thread performs the requested I/O.</span></span> <span data-ttu-id="c3b22-150">Si l’utilisateur décide d’annuler les opérations non terminées (en général, en cliquant sur un bouton Annuler), la routine (dans la section marquée par **WM \_ MYCANCEL**) appelle la fonction [**CancelSynchronousIo**](cancelsynchronousio-func.md) à l’aide du handle de thread retourné par la fonction **CreateFileThread** .</span><span class="sxs-lookup"><span data-stu-id="c3b22-150">If the user decides to cancel the unfinished operations (typically by clicking a cancel button), the routine (in the section marked by **WM\_MYCANCEL**) calls the [**CancelSynchronousIo**](cancelsynchronousio-func.md) function using the thread handle returned by the **CreateFileThread** function.</span></span> <span data-ttu-id="c3b22-151">La fonction **CancelSynchronousIo** retourne immédiatement après la tentative d’annulation.</span><span class="sxs-lookup"><span data-stu-id="c3b22-151">The **CancelSynchronousIo** function returns immediately after the cancellation attempt.</span></span> <span data-ttu-id="c3b22-152">Enfin, l’utilisateur ou l’application peut demander ultérieurement une autre opération qui varie selon que les opérations de fichier sont terminées ou non.</span><span class="sxs-lookup"><span data-stu-id="c3b22-152">Finally, the user or application may later request some other operation that depends on whether the file operations have completed.</span></span> <span data-ttu-id="c3b22-153">Dans ce cas, la routine (dans la section marquée par **WM \_ PROCESSDATA**) vérifie d’abord que les opérations sont terminées, puis exécute les opérations de nettoyage.</span><span class="sxs-lookup"><span data-stu-id="c3b22-153">In this case, the routine (in the section marked by **WM\_PROCESSDATA**) first verifies that the operations have completed and then executes the clean-up operations.</span></span>

    <span data-ttu-id="c3b22-154">**Remarque**  Dans cet exemple, étant donné que l’annulation aurait pu se produire n’importe où dans la séquence d’opérations, il peut être nécessaire que l’appelant s’assure que l’État est cohérent, ou au moins compris, avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="c3b22-154">**Note**  In this example, since the cancellation could have occurred anywhere in the sequence of operations, it may be necessary for the caller to ensure that the state is consistent, or at least understood, before proceeding.</span></span>


```C++
// User-defined codes for the message-pump, which is outside the scope 
// of this sample. Windows messaging and message pumps are well-documented
// elsewhere.
#define WM_MYSYNCOPS    1
#define WM_MYCANCEL     2
#define WM_PROCESSDATA  3

VOID SynchronousIoWorker( VOID *pv )
{
    LPCSTR lpFileName = (LPCSTR)pv;
    HANDLE hFile;
    g_dwOperationInProgress = TRUE;    
    g_CompletionStatus = ERROR_SUCCESS;
     
    hFile = CreateFileA(lpFileName,
                        GENERIC_READ,
                        0,
                        NULL,
                        OPEN_EXISTING,
                        0,
                        NULL);


    if (hFile != INVALID_HANDLE_VALUE) 
    {
        BOOL result = TRUE;
        // TODO: CreateFile succeeded. 
        // Insert your code to make more synchronous calls with hFile.
        // The result variable is assumed to act as the error flag here,
        // but can be whatever your code needs.
        
        if (result == FALSE) 
        {
            // An operation failed or was canceled. If it was canceled,
            // GetLastError() returns ERROR_OPERATION_ABORTED.

            g_CompletionStatus = GetLastError();            
        }
             
        CloseHandle(hFile);
    } 
    else 
    {
        // CreateFile failed or was canceled. If it was canceled,
        // GetLastError() returns ERROR_OPERATION_ABORTED.
        g_CompletionStatus = GetLastError();
    }

    g_dwOperationInProgress = FALSE;
}  


LRESULT
CALLBACK
MainUIThreadMessageHandler(HWND hwnd,
                           UINT uMsg,
                           WPARAM wParam,
                           LPARAM lParam)
{
    UNREFERENCED_PARAMETER(hwnd);
    UNREFERENCED_PARAMETER(wParam);
    UNREFERENCED_PARAMETER(lParam);
    HANDLE syncThread = INVALID_HANDLE_VALUE;

    //  Insert your initializations here.

    switch (uMsg) 
    {
        // User requested an operation on a file.  Insert your code to 
        // retrieve filename from parameters.
        case WM_MYSYNCOPS:    
            syncThread = CreateThread(
                          NULL,
                          0,
                          (LPTHREAD_START_ROUTINE)SynchronousIoWorker,
                          &g_lpFileName,
                          0,
                          NULL);

            if (syncThread == INVALID_HANDLE_VALUE) 
            {
                // Insert your code to handle the failure.
            }
        break;
    
        // User clicked a cancel button.
        case WM_MYCANCEL:
            if (syncThread != INVALID_HANDLE_VALUE) 
            {
                CancelSynchronousIo(syncThread);
            }
        break;

        // User requested other operations.
        case WM_PROCESSDATA:
            if (!g_dwOperationInProgress) 
            {
                if (g_CompletionStatus == ERROR_OPERATION_ABORTED) 
                {
                    // Insert your cleanup code here.
                } 
                else
                {
                    // Insert code to handle other cases.
                }
            }
        break;
    } 

    return TRUE;
} 
```



## <a name="related-topics"></a><span data-ttu-id="c3b22-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3b22-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3b22-156">E/s synchrones et asynchrones</span><span class="sxs-lookup"><span data-stu-id="c3b22-156">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

 



