---
description: Le fait de permettre aux utilisateurs d’annuler les demandes d’e/s qui sont lentes ou bloquées peut améliorer la convivialité et la robustesse de votre application.
ms.assetid: adfe6d05-f30b-40a1-b3b0-58e2593e7b25
title: Annulation d’opérations d’e/s en attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6ca0f938420888934dccb28c9837bdff5dd8515bbdeeb1b3acf4078ae558ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534119"
---
# <a name="canceling-pending-io-operations"></a>Annulation d’opérations d’e/s en attente

Le fait de permettre aux utilisateurs d’annuler les demandes d’e/s qui sont lentes ou bloquées peut améliorer la convivialité et la robustesse de votre application. Par exemple, si un appel à la fonction [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) est bloqué en raison de l’appel à un appareil très lent, l’annulation permet à l’appel d’être relancé, avec de nouveaux paramètres, sans arrêter l’application.

Windows Vista étend les fonctionnalités d’annulation et prend en charge l’annulation des opérations synchrones.

**Remarque**  L’appel de la fonction [**CancelIoEx**](cancelioex-func.md) ne garantit pas qu’une opération d’e/s sera annulée ; le pilote qui gère l’opération doit prendre en charge l’annulation et l’opération doit être dans un État qui peut être annulé.

## <a name="cancellation-considerations"></a>Considérations relatives à l’annulation

Quand vous programmez des appels d’annulation, gardez à l’esprit les considérations suivantes :

-   Il n’existe aucune garantie que les pilotes sous-jacents prennent en charge l’annulation correctement.
-   Lors de l’annulation des e/s asynchrones, quand aucune structure OVERLAPPED n’est fournie à la fonction [**CancelIoEx**](cancelioex-func.md) , la fonction tente d’annuler toutes les e/s en suspens sur le fichier sur tous les threads du processus. Chaque thread est traité individuellement. par conséquent, une fois qu’un thread a été traité, il peut démarrer une autre e/s sur le fichier avant que les e/s de tous les autres threads aient été annulées, provoquant des problèmes de synchronisation.
-   Lorsque vous annulez des e/s asynchrones, ne réutilisez pas les structures avec chevauchement ciblées avec l’annulation ciblée. Une fois l’opération d’e/s terminée (avec succès ou avec un état annulé), la structure OVERLAPPED n’est plus utilisée par le système et peut être réutilisée.
-   Lors de l’annulation des e/s synchrones, l’appel de la fonction [**CancelSynchronousIo**](cancelsynchronousio-func.md) tente d’annuler tout appel synchrone en cours sur le thread. Vous devez veiller à ce que la synchronisation des appels soit correcte. l’appel incorrect dans une série d’appels peut être annulé. Par exemple, si la fonction **CancelSynchronousIo** est appelée pour une opération synchrone, x, l’opération Y démarre uniquement après que l’opération x est terminée (normalement ou avec une erreur). Si le thread qui a appelé l’opération X démarre un autre appel synchrone à X, l’appel Cancel peut interrompre cette nouvelle requête d’e/s.
-   Lorsque vous annulez des e/s synchrones, sachez qu’une condition de concurrence peut exister chaque fois qu’un thread est partagé entre différentes parties d’une application, par exemple, avec un thread de pool de threads.

## <a name="operations-that-cannot-be-canceled"></a>Opérations qui ne peuvent pas être annulées

Certaines fonctions ne peuvent pas être annulées à l’aide de la fonction [**CancelIo**](cancelio.md), [**CancelIoEx**](cancelioex-func.md)ou [**CancelSynchronousIo**](cancelsynchronousio-func.md) . Certaines de ces fonctions ont été étendues pour permettre l’annulation (par exemple, la fonction [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) ) et vous devez les utiliser à la place. Outre la prise en charge de l’annulation, ces fonctions disposent également de rappels intégrés pour vous aider à suivre la progression de l’opération. Les fonctions suivantes ne prennent pas en charge l’annulation :

-   [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)— utilisez [ **CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
-   [**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile): utilisez [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa): utilisez [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

Pour plus d’informations, consultez [instructions d’achèvement/annulation d’e/s](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).

## <a name="canceling-asynchronous-io"></a>Annulation d’e/s asynchrones

Vous pouvez annuler des e/s asynchrones à partir de n’importe quel thread du processus qui a émis l’opération d’e/s. Vous devez spécifier le descripteur sur lequel l’e/s a été exécutée et, éventuellement, la structure OVERLAPPED qui a été utilisée pour effectuer les e/s. Vous pouvez déterminer si l’annulation s’est produite en examinant l’état retourné dans la structure OVERLAPPED ou dans le rappel d’achèvement. L’état **erreur \_ opération \_ abandonnée** indique que l’opération a été annulée.

L’exemple suivant montre une routine qui prend un délai d’attente et tente une opération de lecture, en l’annulant avec la fonction [**CancelIoEx**](cancelioex-func.md) si le délai d’attente expire.


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



## <a name="canceling-synchronous-io"></a>Annulation des e/s synchrones

Vous pouvez annuler des e/s synchrones à partir de n’importe quel thread du processus qui a émis l’opération d’e/s. Vous devez spécifier le descripteur du thread qui effectue actuellement l’opération d’e/s.

L’exemple suivant illustre deux routines :

-   La fonction **SynchronousIoWorker** est un thread de travail qui implémente des e/s de fichier synchrones, en commençant par un appel à la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) . Si la routine est réussie, la routine peut être suivie d’opérations supplémentaires, qui ne sont pas incluses ici. La variable globale *gCompletionStatus* peut être utilisée pour déterminer si toutes les opérations ont réussi ou si une opération a échoué ou a été annulée. La variable globale *dwOperationInProgress* indique si les e/s de fichier sont toujours en cours.

    **Remarque**  Dans cet exemple, le thread d’interface utilisateur peut également vérifier l’existence du thread de travail.

    Des vérifications manuelles supplémentaires, qui ne sont pas incluses ici, sont nécessaires dans la fonction **SynchronousIoWorker** pour s’assurer que si l’annulation a été demandée pendant les courtes périodes entre les appels d’e/s de fichier, les autres opérations seront annulées.

-   La fonction **MainUIThreadMessageHandler** simule le gestionnaire de messages dans la procédure de fenêtre d’un thread d’interface utilisateur. L’utilisateur demande un ensemble d’opérations de fichier synchrones en cliquant sur un contrôle, ce qui génère un message de fenêtre défini par l’utilisateur, (dans la section marquée par **WM \_ MYSYNCOPS**). Cela crée un nouveau thread à l’aide de la fonction **CreateFileThread** , qui démarre ensuite la fonction **SynchronousIoWorker** est. Le thread d’interface utilisateur continue de traiter les messages pendant que le thread de travail effectue l’e/s demandée. Si l’utilisateur décide d’annuler les opérations non terminées (en général, en cliquant sur un bouton Annuler), la routine (dans la section marquée par **WM \_ MYCANCEL**) appelle la fonction [**CancelSynchronousIo**](cancelsynchronousio-func.md) à l’aide du handle de thread retourné par la fonction **CreateFileThread** . La fonction **CancelSynchronousIo** retourne immédiatement après la tentative d’annulation. Enfin, l’utilisateur ou l’application peut demander ultérieurement une autre opération qui varie selon que les opérations de fichier sont terminées ou non. Dans ce cas, la routine (dans la section marquée par **WM \_ PROCESSDATA**) vérifie d’abord que les opérations sont terminées, puis exécute les opérations de nettoyage.

    **Remarque**  Dans cet exemple, étant donné que l’annulation aurait pu se produire n’importe où dans la séquence d’opérations, il peut être nécessaire que l’appelant s’assure que l’État est cohérent, ou au moins compris, avant de continuer.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[E/s synchrones et asynchrones](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

 



