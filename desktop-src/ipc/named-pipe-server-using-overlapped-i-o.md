---
description: Exemple de code d’un serveur de canal à thread unique qui utilise des opérations avec chevauchement pour traiter des connexions simultanées à plusieurs clients de canal.
ms.assetid: c0ac70cc-4ab9-47e5-b0e6-c0b373d16b25
title: Serveur de canaux nommés utilisant des e/s avec chevauchement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3f9134582a50c2053893cf6ee4908e447e3cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952137"
---
# <a name="named-pipe-server-using-overlapped-io"></a><span data-ttu-id="483a9-103">Serveur de canaux nommés utilisant des e/s avec chevauchement</span><span class="sxs-lookup"><span data-stu-id="483a9-103">Named Pipe Server Using Overlapped I/O</span></span>

<span data-ttu-id="483a9-104">Voici un exemple de serveur de canal à thread unique qui utilise des opérations avec chevauchement pour traiter des connexions simultanées à plusieurs clients de canal.</span><span class="sxs-lookup"><span data-stu-id="483a9-104">The following is an example of a single-threaded pipe server that uses overlapped operations to service simultaneous connections to multiple pipe clients.</span></span> <span data-ttu-id="483a9-105">Le serveur de canaux crée un nombre fixe d’instances de canal.</span><span class="sxs-lookup"><span data-stu-id="483a9-105">The pipe server creates a fixed number of pipe instances.</span></span> <span data-ttu-id="483a9-106">Chaque instance de canal peut être connectée à un client de canal distinct.</span><span class="sxs-lookup"><span data-stu-id="483a9-106">Each pipe instance can be connected to a separate pipe client.</span></span> <span data-ttu-id="483a9-107">Lorsqu’un client de canal a fini d’utiliser son instance de canal, le serveur se déconnecte du client et réutilise l’instance de canal pour se connecter à un nouveau client.</span><span class="sxs-lookup"><span data-stu-id="483a9-107">When a pipe client has finished using its pipe instance, the server disconnects from the client and reuses the pipe instance to connect to a new client.</span></span> <span data-ttu-id="483a9-108">Ce serveur de canaux peut être utilisé avec le client de canal décrit dans [client du canal nommé](named-pipe-client.md).</span><span class="sxs-lookup"><span data-stu-id="483a9-108">This pipe server can be used with the pipe client described in [Named Pipe Client](named-pipe-client.md).</span></span>

<span data-ttu-id="483a9-109">La structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) est spécifiée en tant que paramètre dans chaque opération [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)et [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) sur l’instance de canal.</span><span class="sxs-lookup"><span data-stu-id="483a9-109">The [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure is specified as a parameter in each [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), and [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) operation on the pipe instance.</span></span> <span data-ttu-id="483a9-110">Bien que l’exemple montre des opérations simultanées sur différentes instances de canal, il évite les opérations simultanées sur une instance de canal unique à l’aide de l’objet d’événement dans la structure **OVERLAPPED** .</span><span class="sxs-lookup"><span data-stu-id="483a9-110">Although the example shows simultaneous operations on different pipe instances, it avoids simultaneous operations on a single pipe instance by using the event object in the **OVERLAPPED** structure.</span></span> <span data-ttu-id="483a9-111">Étant donné que le même objet d’événement est utilisé pour les opérations de lecture, d’écriture et de connexion pour chaque instance, il n’existe aucun moyen de savoir quelle est l’achèvement de l’opération qui a provoqué la définition de l’événement à l’état signalé pour les opérations simultanées utilisant la même instance de canal.</span><span class="sxs-lookup"><span data-stu-id="483a9-111">Because the same event object is used for read, write, and connect operations for each instance, there is no way to know which operation's completion caused the event to be set to the signaled state for simultaneous operations using the same pipe instance.</span></span>

<span data-ttu-id="483a9-112">Les descripteurs d’événements pour chaque instance de canal sont stockés dans un tableau qui est passé à la fonction [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) .</span><span class="sxs-lookup"><span data-stu-id="483a9-112">The event handles for each pipe instance are stored in an array that is passed to the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function.</span></span> <span data-ttu-id="483a9-113">Cette fonction attend que l’un des événements soit signalé et retourne l’index de tableau de l’événement qui a provoqué l’exécution de l’opération d’attente.</span><span class="sxs-lookup"><span data-stu-id="483a9-113">This function waits for one of the events to be signaled, and returns the array index of the event that caused the wait operation to complete.</span></span> <span data-ttu-id="483a9-114">L’exemple de cette rubrique utilise cet index de tableau pour récupérer une structure contenant des informations pour l’instance de canal.</span><span class="sxs-lookup"><span data-stu-id="483a9-114">The example in this topic uses this array index to retrieve a structure containing information for the pipe instance.</span></span> <span data-ttu-id="483a9-115">Le serveur utilise le membre **fPendingIO** de la structure pour déterminer si l’opération d’e/s la plus récente sur l’instance était en attente, ce qui nécessite un appel à la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="483a9-115">The server uses the **fPendingIO** member of the structure to keep track of whether the most recent I/O operation on the instance was pending, which requires a call to the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="483a9-116">Le serveur utilise le membre **dwState** de la structure pour déterminer l’opération suivante qui doit être effectuée pour l’instance de canal.</span><span class="sxs-lookup"><span data-stu-id="483a9-116">The server uses the **dwState** member of the structure to determine the next operation that must be performed for the pipe instance.</span></span>

<span data-ttu-id="483a9-117">Les opérations [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)et [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) avec chevauchement peuvent se terminer au moment où la fonction retourne.</span><span class="sxs-lookup"><span data-stu-id="483a9-117">Overlapped [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), and [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) operations can finish by the time the function returns.</span></span> <span data-ttu-id="483a9-118">Sinon, si l’opération est en attente, l’objet d’événement dans la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) spécifiée est défini à l’état non signalé avant le retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="483a9-118">Otherwise, if the operation is pending, the event object in the specified [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure is set to the nonsignaled state before the function returns.</span></span> <span data-ttu-id="483a9-119">Lorsque l’opération en attente se termine, le système définit l’état de l’objet d’événement comme étant signalé.</span><span class="sxs-lookup"><span data-stu-id="483a9-119">When the pending operation finishes, the system sets the state of the event object to signaled.</span></span> <span data-ttu-id="483a9-120">L’état de l’objet d’événement n’est pas modifié si l’opération se termine avant le retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="483a9-120">The state of the event object is not changed if the operation finishes before the function returns.</span></span>

<span data-ttu-id="483a9-121">Étant donné que l’exemple utilise des objets d’événement à réinitialisation manuelle, l’état d’un objet d’événement n’est pas remplacé par la fonction [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) .</span><span class="sxs-lookup"><span data-stu-id="483a9-121">Because the example uses manual-reset event objects, the state of an event object is not changed to nonsignaled by the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function.</span></span> <span data-ttu-id="483a9-122">Cela est important, car l’exemple s’appuie sur les objets d’événement restants dans l’état signalé, sauf s’il existe une opération en attente.</span><span class="sxs-lookup"><span data-stu-id="483a9-122">This is important, because the example relies on the event objects remaining in the signaled state, except when there is a pending operation.</span></span>

<span data-ttu-id="483a9-123">Si l’opération est déjà terminée lorsque [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)ou [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) retourne, la valeur de retour de la fonction indique le résultat.</span><span class="sxs-lookup"><span data-stu-id="483a9-123">If the operation has already finished when [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), or [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) returns, the function's return value indicates the result.</span></span> <span data-ttu-id="483a9-124">Pour les opérations de lecture et d’écriture, le nombre d’octets transférés est également retourné.</span><span class="sxs-lookup"><span data-stu-id="483a9-124">For read and write operations, the number of bytes transferred is also returned.</span></span> <span data-ttu-id="483a9-125">Si l’opération est toujours en attente, la fonction **ReadFile**, **WriteFile** ou **ConnectNamedPipe** retourne zéro et la fonction [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne les \_ e/s d’erreur \_ en attente.</span><span class="sxs-lookup"><span data-stu-id="483a9-125">If the operation is still pending, the **ReadFile**, **WriteFile**, or **ConnectNamedPipe** function returns zero and the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns ERROR\_IO\_PENDING.</span></span> <span data-ttu-id="483a9-126">Dans ce cas, utilisez la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) pour récupérer les résultats une fois l’opération terminée.</span><span class="sxs-lookup"><span data-stu-id="483a9-126">In this case, use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to retrieve the results after the operation has finished.</span></span> <span data-ttu-id="483a9-127">**GetOverlappedResult** retourne uniquement les résultats des opérations en attente.</span><span class="sxs-lookup"><span data-stu-id="483a9-127">**GetOverlappedResult** returns only the results of pending operations.</span></span> <span data-ttu-id="483a9-128">Elle ne signale pas les résultats des opérations qui ont été effectuées avant le renvoi de la fonction **ReadFile**, **WriteFile** ou **ConnectNamedPipe** avec chevauchement.</span><span class="sxs-lookup"><span data-stu-id="483a9-128">It does not report the results of operations that were completed before the overlapped **ReadFile**, **WriteFile**, or **ConnectNamedPipe** function returned.</span></span>

<span data-ttu-id="483a9-129">Avant de vous déconnecter d’un client, vous devez attendre un signal indiquant que le client est terminé.</span><span class="sxs-lookup"><span data-stu-id="483a9-129">Before disconnecting from a client, you must wait for a signal indicating the client has finished.</span></span> <span data-ttu-id="483a9-130">(Le vidage des mémoires tampons de fichier aurait pour effet d’annuler l’objectif des e/s avec chevauchement, car l’opération de vidage bloquerait l’exécution du thread du serveur pendant qu’il attend que le client vide le canal.) Dans cet exemple, le signal est l’erreur générée en tentant de lire à partir du canal après que le client du canal a fermé son handle.</span><span class="sxs-lookup"><span data-stu-id="483a9-130">(Flushing the file buffers would defeat the purpose of overlapped I/O, because the flush operation would block the execution of the server thread while it waits for the client to empty the pipe.) In this example, the signal is the error generated by trying to read from the pipe after the pipe client closes its handle.</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <tchar.h>
#include <strsafe.h>
 
#define CONNECTING_STATE 0 
#define READING_STATE 1 
#define WRITING_STATE 2 
#define INSTANCES 4 
#define PIPE_TIMEOUT 5000
#define BUFSIZE 4096
 
typedef struct 
{ 
   OVERLAPPED oOverlap; 
   HANDLE hPipeInst; 
   TCHAR chRequest[BUFSIZE]; 
   DWORD cbRead;
   TCHAR chReply[BUFSIZE];
   DWORD cbToWrite; 
   DWORD dwState; 
   BOOL fPendingIO; 
} PIPEINST, *LPPIPEINST; 
 
 
VOID DisconnectAndReconnect(DWORD); 
BOOL ConnectToNewClient(HANDLE, LPOVERLAPPED); 
VOID GetAnswerToRequest(LPPIPEINST); 
 
PIPEINST Pipe[INSTANCES]; 
HANDLE hEvents[INSTANCES]; 
 
int _tmain(VOID) 
{ 
   DWORD i, dwWait, cbRet, dwErr; 
   BOOL fSuccess; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 
 
// The initial loop creates several instances of a named pipe 
// along with an event object for each instance.  An 
// overlapped ConnectNamedPipe operation is started for 
// each instance. 
 
   for (i = 0; i < INSTANCES; i++) 
   { 
 
   // Create an event object for this instance. 
 
      hEvents[i] = CreateEvent( 
         NULL,    // default security attribute 
         TRUE,    // manual-reset event 
         TRUE,    // initial state = signaled 
         NULL);   // unnamed event object 

      if (hEvents[i] == NULL) 
      {
         printf("CreateEvent failed with %d.\n", GetLastError()); 
         return 0;
      }
 
      Pipe[i].oOverlap.hEvent = hEvents[i]; 
 
      Pipe[i].hPipeInst = CreateNamedPipe( 
         lpszPipename,            // pipe name 
         PIPE_ACCESS_DUPLEX |     // read/write access 
         FILE_FLAG_OVERLAPPED,    // overlapped mode 
         PIPE_TYPE_MESSAGE |      // message-type pipe 
         PIPE_READMODE_MESSAGE |  // message-read mode 
         PIPE_WAIT,               // blocking mode 
         INSTANCES,               // number of instances 
         BUFSIZE*sizeof(TCHAR),   // output buffer size 
         BUFSIZE*sizeof(TCHAR),   // input buffer size 
         PIPE_TIMEOUT,            // client time-out 
         NULL);                   // default security attributes 

      if (Pipe[i].hPipeInst == INVALID_HANDLE_VALUE) 
      {
         printf("CreateNamedPipe failed with %d.\n", GetLastError());
         return 0;
      }
 
   // Call the subroutine to connect to the new client
 
      Pipe[i].fPendingIO = ConnectToNewClient( 
         Pipe[i].hPipeInst, 
         &Pipe[i].oOverlap); 
 
      Pipe[i].dwState = Pipe[i].fPendingIO ? 
         CONNECTING_STATE : // still connecting 
         READING_STATE;     // ready to read 
   } 
 
   while (1) 
   { 
   // Wait for the event object to be signaled, indicating 
   // completion of an overlapped read, write, or 
   // connect operation. 
 
      dwWait = WaitForMultipleObjects( 
         INSTANCES,    // number of event objects 
         hEvents,      // array of event objects 
         FALSE,        // does not wait for all 
         INFINITE);    // waits indefinitely 
 
   // dwWait shows which pipe completed the operation. 
 
      i = dwWait - WAIT_OBJECT_0;  // determines which pipe 
      if (i < 0 || i > (INSTANCES - 1)) 
      {
         printf("Index out of range.\n"); 
         return 0;
      }
 
   // Get the result if the operation was pending. 
 
      if (Pipe[i].fPendingIO) 
      { 
         fSuccess = GetOverlappedResult( 
            Pipe[i].hPipeInst, // handle to pipe 
            &Pipe[i].oOverlap, // OVERLAPPED structure 
            &cbRet,            // bytes transferred 
            FALSE);            // do not wait 
 
         switch (Pipe[i].dwState) 
         { 
         // Pending connect operation 
            case CONNECTING_STATE: 
               if (! fSuccess) 
               {
                   printf("Error %d.\n", GetLastError()); 
                   return 0;
               }
               Pipe[i].dwState = READING_STATE; 
               break; 
 
         // Pending read operation 
            case READING_STATE: 
               if (! fSuccess || cbRet == 0) 
               { 
                  DisconnectAndReconnect(i); 
                  continue; 
               }
               Pipe[i].cbRead = cbRet;
               Pipe[i].dwState = WRITING_STATE; 
               break; 
 
         // Pending write operation 
            case WRITING_STATE: 
               if (! fSuccess || cbRet != Pipe[i].cbToWrite) 
               { 
                  DisconnectAndReconnect(i); 
                  continue; 
               } 
               Pipe[i].dwState = READING_STATE; 
               break; 
 
            default: 
            {
               printf("Invalid pipe state.\n"); 
               return 0;
            }
         }  
      } 
 
   // The pipe state determines which operation to do next. 
 
      switch (Pipe[i].dwState) 
      { 
      // READING_STATE: 
      // The pipe instance is connected to the client 
      // and is ready to read a request from the client. 
 
         case READING_STATE: 
            fSuccess = ReadFile( 
               Pipe[i].hPipeInst, 
               Pipe[i].chRequest, 
               BUFSIZE*sizeof(TCHAR), 
               &Pipe[i].cbRead, 
               &Pipe[i].oOverlap); 
 
         // The read operation completed successfully. 
 
            if (fSuccess && Pipe[i].cbRead != 0) 
            { 
               Pipe[i].fPendingIO = FALSE; 
               Pipe[i].dwState = WRITING_STATE; 
               continue; 
            } 
 
         // The read operation is still pending. 
 
            dwErr = GetLastError(); 
            if (! fSuccess && (dwErr == ERROR_IO_PENDING)) 
            { 
               Pipe[i].fPendingIO = TRUE; 
               continue; 
            } 
 
         // An error occurred; disconnect from the client. 
 
            DisconnectAndReconnect(i); 
            break; 
 
      // WRITING_STATE: 
      // The request was successfully read from the client. 
      // Get the reply data and write it to the client. 
 
         case WRITING_STATE: 
            GetAnswerToRequest(&Pipe[i]); 
 
            fSuccess = WriteFile( 
               Pipe[i].hPipeInst, 
               Pipe[i].chReply, 
               Pipe[i].cbToWrite, 
               &cbRet, 
               &Pipe[i].oOverlap); 
 
         // The write operation completed successfully. 
 
            if (fSuccess && cbRet == Pipe[i].cbToWrite) 
            { 
               Pipe[i].fPendingIO = FALSE; 
               Pipe[i].dwState = READING_STATE; 
               continue; 
            } 
 
         // The write operation is still pending. 
 
            dwErr = GetLastError(); 
            if (! fSuccess && (dwErr == ERROR_IO_PENDING)) 
            { 
               Pipe[i].fPendingIO = TRUE; 
               continue; 
            } 
 
         // An error occurred; disconnect from the client. 
 
            DisconnectAndReconnect(i); 
            break; 
 
         default: 
         {
            printf("Invalid pipe state.\n"); 
            return 0;
         }
      } 
  } 
 
  return 0; 
} 
 
 
// DisconnectAndReconnect(DWORD) 
// This function is called when an error occurs or when the client 
// closes its handle to the pipe. Disconnect from this client, then 
// call ConnectNamedPipe to wait for another client to connect. 
 
VOID DisconnectAndReconnect(DWORD i) 
{ 
// Disconnect the pipe instance. 
 
   if (! DisconnectNamedPipe(Pipe[i].hPipeInst) ) 
   {
      printf("DisconnectNamedPipe failed with %d.\n", GetLastError());
   }
 
// Call a subroutine to connect to the new client. 
 
   Pipe[i].fPendingIO = ConnectToNewClient( 
      Pipe[i].hPipeInst, 
      &Pipe[i].oOverlap); 
 
   Pipe[i].dwState = Pipe[i].fPendingIO ? 
      CONNECTING_STATE : // still connecting 
      READING_STATE;     // ready to read 
} 
 
// ConnectToNewClient(HANDLE, LPOVERLAPPED) 
// This function is called to start an overlapped connect operation. 
// It returns TRUE if an operation is pending or FALSE if the 
// connection has been completed. 
 
BOOL ConnectToNewClient(HANDLE hPipe, LPOVERLAPPED lpo) 
{ 
   BOOL fConnected, fPendingIO = FALSE; 
 
// Start an overlapped connection for this pipe instance. 
   fConnected = ConnectNamedPipe(hPipe, lpo); 
 
// Overlapped ConnectNamedPipe should return zero. 
   if (fConnected) 
   {
      printf("ConnectNamedPipe failed with %d.\n", GetLastError()); 
      return 0;
   }
 
   switch (GetLastError()) 
   { 
   // The overlapped connection in progress. 
      case ERROR_IO_PENDING: 
         fPendingIO = TRUE; 
         break; 
 
   // Client is already connected, so signal an event. 
 
      case ERROR_PIPE_CONNECTED: 
         if (SetEvent(lpo->hEvent)) 
            break; 
 
   // If an error occurs during the connect operation... 
      default: 
      {
         printf("ConnectNamedPipe failed with %d.\n", GetLastError());
         return 0;
      }
   } 
 
   return fPendingIO; 
}

VOID GetAnswerToRequest(LPPIPEINST pipe)
{
   _tprintf( TEXT("[%d] %s\n"), pipe->hPipeInst, pipe->chRequest);
   StringCchCopy( pipe->chReply, BUFSIZE, TEXT("Default answer from server") );
   pipe->cbToWrite = (lstrlen(pipe->chReply)+1)*sizeof(TCHAR);
}

```



## <a name="related-topics"></a><span data-ttu-id="483a9-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="483a9-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="483a9-132">Client de canal nommé</span><span class="sxs-lookup"><span data-stu-id="483a9-132">Named Pipe Client</span></span>](named-pipe-client.md)
</dt> </dl>

 

 
