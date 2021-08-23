---
description: L’exemple de code est un serveur de canal à thread unique qui crée un canal de type de message et utilise des opérations avec chevauchement.
ms.assetid: 8b73485c-c6f7-44df-9e53-308df2c752e7
title: Serveur de canaux nommés utilisant les routines de saisie semi-automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61ddd1a5213de8593a5697341ef3aed4988b7a700c02db9eba83440f40634627
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611199"
---
# <a name="named-pipe-server-using-completion-routines"></a>Serveur de canaux nommés utilisant les routines de saisie semi-automatique

L’exemple suivant est un serveur de canal à thread unique qui crée un canal de type message et utilise des opérations avec chevauchement. Elle utilise les fonctions étendues [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) et [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) pour effectuer des e/s avec chevauchement à l’aide d’une routine de saisie semi-automatique, qui est mise en file d’attente pour l’exécution lorsque l’opération est terminée. Le serveur de canaux utilise la fonction [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) , qui effectue une opération d’attente d’alerte qui retourne lorsqu’une routine de saisie semi-automatique est prête à être exécutée. La fonction Wait retourne également lorsqu’un objet d’événement est signalé, ce qui, dans cet exemple, indique que l’opération [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) avec chevauchement est terminée (un nouveau client s’est connecté). Ce serveur de canaux peut être utilisé avec le client de canal décrit dans [client du canal nommé](named-pipe-client.md).

Initialement, le serveur de canaux crée une seule instance du canal et démarre une opération [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) avec chevauchement. Lorsqu’un client se connecte, le serveur alloue une structure pour fournir le stockage pour cette instance de canal, puis appelle la fonction [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) pour démarrer une séquence d’opérations d’e/s afin de gérer les communications avec le client. Chaque opération spécifie une routine de saisie semi-automatique qui effectue l’opération suivante dans la séquence. La séquence se termine lorsque le client est déconnecté et que l’instance de canal est fermée. Après le démarrage de la séquence d’opérations pour le nouveau client, le serveur crée une autre instance de canal et attend que le client suivant se connecte.

Les paramètres des fonctions [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) et [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) spécifient une routine de saisie semi-automatique et un pointeur vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . Ce pointeur est passé à la routine d’achèvement dans son paramètre *lpOverLap* . Étant donné que la structure **OVERLAPPED** pointe vers le premier membre de la structure allouée pour chaque instance de canal, la routine d’achèvement peut utiliser son paramètre *lpOverLap* pour accéder à la structure de l’instance de canal.


```C++
#include <windows.h> 
#include <stdio.h>
#include <tchar.h>
#include <strsafe.h>

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
} PIPEINST, *LPPIPEINST; 
 
VOID DisconnectAndClose(LPPIPEINST); 
BOOL CreateAndConnectInstance(LPOVERLAPPED); 
BOOL ConnectToNewClient(HANDLE, LPOVERLAPPED); 
VOID GetAnswerToRequest(LPPIPEINST); 

VOID WINAPI CompletedWriteRoutine(DWORD, DWORD, LPOVERLAPPED); 
VOID WINAPI CompletedReadRoutine(DWORD, DWORD, LPOVERLAPPED); 
 
HANDLE hPipe; 
 
int _tmain(VOID) 
{ 
   HANDLE hConnectEvent; 
   OVERLAPPED oConnect; 
   LPPIPEINST lpPipeInst; 
   DWORD dwWait, cbRet; 
   BOOL fSuccess, fPendingIO; 
 
// Create one event object for the connect operation. 
 
   hConnectEvent = CreateEvent( 
      NULL,    // default security attribute
      TRUE,    // manual reset event 
      TRUE,    // initial state = signaled 
      NULL);   // unnamed event object 

   if (hConnectEvent == NULL) 
   {
      printf("CreateEvent failed with %d.\n", GetLastError()); 
      return 0;
   }
 
   oConnect.hEvent = hConnectEvent; 
 
// Call a subroutine to create one instance, and wait for 
// the client to connect. 
 
   fPendingIO = CreateAndConnectInstance(&oConnect); 
 
   while (1) 
   { 
   // Wait for a client to connect, or for a read or write 
   // operation to be completed, which causes a completion 
   // routine to be queued for execution. 
 
      dwWait = WaitForSingleObjectEx( 
         hConnectEvent,  // event object to wait for 
         INFINITE,       // waits indefinitely 
         TRUE);          // alertable wait enabled 
 
      switch (dwWait) 
      { 
      // The wait conditions are satisfied by a completed connect 
      // operation. 
         case 0: 
         // If an operation is pending, get the result of the 
         // connect operation. 
 
         if (fPendingIO) 
         { 
            fSuccess = GetOverlappedResult( 
               hPipe,     // pipe handle 
               &oConnect, // OVERLAPPED structure 
               &cbRet,    // bytes transferred 
               FALSE);    // does not wait 
            if (!fSuccess) 
            {
               printf("ConnectNamedPipe (%d)\n", GetLastError()); 
               return 0;
            }
         } 
 
         // Allocate storage for this instance. 
 
            lpPipeInst = (LPPIPEINST) GlobalAlloc( 
               GPTR, sizeof(PIPEINST)); 
            if (lpPipeInst == NULL) 
            {
               printf("GlobalAlloc failed (%d)\n", GetLastError()); 
               return 0;
            }
 
            lpPipeInst->hPipeInst = hPipe; 
 
         // Start the read operation for this client. 
         // Note that this same routine is later used as a 
         // completion routine after a write operation. 
 
            lpPipeInst->cbToWrite = 0; 
            CompletedWriteRoutine(0, 0, (LPOVERLAPPED) lpPipeInst); 
 
         // Create new pipe instance for the next client. 
 
            fPendingIO = CreateAndConnectInstance( 
               &oConnect); 
            break; 
 
      // The wait is satisfied by a completed read or write 
      // operation. This allows the system to execute the 
      // completion routine. 
 
         case WAIT_IO_COMPLETION: 
            break; 
 
      // An error occurred in the wait function. 
 
         default: 
         {
            printf("WaitForSingleObjectEx (%d)\n", GetLastError()); 
            return 0;
         }
      } 
   } 
   return 0; 
} 
 
// CompletedWriteRoutine(DWORD, DWORD, LPOVERLAPPED) 
// This routine is called as a completion routine after writing to 
// the pipe, or when a new client has connected to a pipe instance.
// It starts another read operation. 
 
VOID WINAPI CompletedWriteRoutine(DWORD dwErr, DWORD cbWritten, 
   LPOVERLAPPED lpOverLap) 
{ 
   LPPIPEINST lpPipeInst; 
   BOOL fRead = FALSE; 
 
// lpOverlap points to storage for this instance. 
 
   lpPipeInst = (LPPIPEINST) lpOverLap; 
 
// The write operation has finished, so read the next request (if 
// there is no error). 
 
   if ((dwErr == 0) && (cbWritten == lpPipeInst->cbToWrite)) 
      fRead = ReadFileEx( 
         lpPipeInst->hPipeInst, 
         lpPipeInst->chRequest, 
         BUFSIZE*sizeof(TCHAR), 
         (LPOVERLAPPED) lpPipeInst, 
         (LPOVERLAPPED_COMPLETION_ROUTINE) CompletedReadRoutine); 
 
// Disconnect if an error occurred. 
 
   if (! fRead) 
      DisconnectAndClose(lpPipeInst); 
} 
 
// CompletedReadRoutine(DWORD, DWORD, LPOVERLAPPED) 
// This routine is called as an I/O completion routine after reading 
// a request from the client. It gets data and writes it to the pipe. 
 
VOID WINAPI CompletedReadRoutine(DWORD dwErr, DWORD cbBytesRead, 
    LPOVERLAPPED lpOverLap) 
{ 
   LPPIPEINST lpPipeInst; 
   BOOL fWrite = FALSE; 
 
// lpOverlap points to storage for this instance. 
 
   lpPipeInst = (LPPIPEINST) lpOverLap; 
 
// The read operation has finished, so write a response (if no 
// error occurred). 
 
   if ((dwErr == 0) && (cbBytesRead != 0)) 
   { 
      GetAnswerToRequest(lpPipeInst); 
 
      fWrite = WriteFileEx( 
         lpPipeInst->hPipeInst, 
         lpPipeInst->chReply, 
         lpPipeInst->cbToWrite, 
         (LPOVERLAPPED) lpPipeInst, 
         (LPOVERLAPPED_COMPLETION_ROUTINE) CompletedWriteRoutine); 
   } 
 
// Disconnect if an error occurred. 
 
   if (! fWrite) 
      DisconnectAndClose(lpPipeInst); 
} 
 
// DisconnectAndClose(LPPIPEINST) 
// This routine is called when an error occurs or the client closes 
// its handle to the pipe. 
 
VOID DisconnectAndClose(LPPIPEINST lpPipeInst) 
{ 
// Disconnect the pipe instance. 
 
   if (! DisconnectNamedPipe(lpPipeInst->hPipeInst) ) 
   {
      printf("DisconnectNamedPipe failed with %d.\n", GetLastError());
   }
 
// Close the handle to the pipe instance. 
 
   CloseHandle(lpPipeInst->hPipeInst); 
 
// Release the storage for the pipe instance. 
 
   if (lpPipeInst != NULL) 
      GlobalFree(lpPipeInst); 
} 
 
// CreateAndConnectInstance(LPOVERLAPPED) 
// This function creates a pipe instance and connects to the client. 
// It returns TRUE if the connect operation is pending, and FALSE if 
// the connection has been completed. 
 
BOOL CreateAndConnectInstance(LPOVERLAPPED lpoOverlap) 
{ 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 
 
   hPipe = CreateNamedPipe( 
      lpszPipename,             // pipe name 
      PIPE_ACCESS_DUPLEX |      // read/write access 
      FILE_FLAG_OVERLAPPED,     // overlapped mode 
      PIPE_TYPE_MESSAGE |       // message-type pipe 
      PIPE_READMODE_MESSAGE |   // message read mode 
      PIPE_WAIT,                // blocking mode 
      PIPE_UNLIMITED_INSTANCES, // unlimited instances 
      BUFSIZE*sizeof(TCHAR),    // output buffer size 
      BUFSIZE*sizeof(TCHAR),    // input buffer size 
      PIPE_TIMEOUT,             // client time-out 
      NULL);                    // default security attributes
   if (hPipe == INVALID_HANDLE_VALUE) 
   {
      printf("CreateNamedPipe failed with %d.\n", GetLastError()); 
      return 0;
   }
 
// Call a subroutine to connect to the new client. 
 
   return ConnectToNewClient(hPipe, lpoOverlap); 
}

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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Client de canal nommé](named-pipe-client.md)
</dt> </dl>

 

 
