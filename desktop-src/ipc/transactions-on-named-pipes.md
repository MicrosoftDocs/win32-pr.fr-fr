---
description: Une transaction de canal nommé est une communication client/serveur qui associe une opération d’écriture et une opération de lecture dans une opération de réseau unique. Les transactions améliorent les performances des communications réseau entre un client et un serveur distant.
ms.assetid: aedce207-7dea-4670-b6dd-0c61b3f6f690
title: Transactions sur les canaux nommés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 489039b92b65f57cefc71c5d78a01b1824b1418a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530111"
---
# <a name="transactions-on-named-pipes"></a><span data-ttu-id="53feb-104">Transactions sur les canaux nommés</span><span class="sxs-lookup"><span data-stu-id="53feb-104">Transactions on Named Pipes</span></span>

<span data-ttu-id="53feb-105">Une transaction de canal nommé est une communication client/serveur qui associe une opération d’écriture et une opération de lecture dans une opération de réseau unique.</span><span class="sxs-lookup"><span data-stu-id="53feb-105">A named pipe transaction is a client/server communication that combines a write operation and a read operation into a single network operation.</span></span> <span data-ttu-id="53feb-106">Une transaction ne peut être utilisée que sur un canal de type de message duplex.</span><span class="sxs-lookup"><span data-stu-id="53feb-106">A transaction can be used only on a duplex, message-type pipe.</span></span> <span data-ttu-id="53feb-107">Les transactions améliorent les performances des communications réseau entre un client et un serveur distant.</span><span class="sxs-lookup"><span data-stu-id="53feb-107">Transactions improve the performance of network communications between a client and a remote server.</span></span> <span data-ttu-id="53feb-108">Les processus peuvent utiliser les fonctions [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) et [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) pour effectuer des transactions de canal nommé.</span><span class="sxs-lookup"><span data-stu-id="53feb-108">Processes can use the [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) and [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) functions to perform named pipe transactions.</span></span>

<span data-ttu-id="53feb-109">La fonction [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) est généralement utilisée par un client de canal pour écrire un message de demande au serveur de canaux nommés et lire le message de réponse du serveur.</span><span class="sxs-lookup"><span data-stu-id="53feb-109">The [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) function is most commonly used by a pipe client to write a request message to the named pipe server and read the server's response message.</span></span> <span data-ttu-id="53feb-110">Le client de canal doit spécifier \_ \| \_ un accès en écriture générique de lecture générique lorsqu’il ouvre son handle de canal en appelant la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="53feb-110">The pipe client must specify GENERIC\_READ \| GENERIC\_WRITE access when it opens its pipe handle by calling the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="53feb-111">Ensuite, le client de canal définit le descripteur de canal en mode de lecture de message en appelant la fonction [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) .</span><span class="sxs-lookup"><span data-stu-id="53feb-111">Then, the pipe client sets the pipe handle to message-read mode by calling the [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) function.</span></span> <span data-ttu-id="53feb-112">Si la mémoire tampon de lecture spécifiée dans l’appel à **TransactNamedPipe** n’est pas assez grande pour contenir le message entier écrit par le serveur, la fonction retourne zéro et [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur \_ plus de \_ données.</span><span class="sxs-lookup"><span data-stu-id="53feb-112">If the read buffer specified in the call to **TransactNamedPipe** is not large enough to hold the entire message written by the server, the function returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_MORE\_DATA.</span></span> <span data-ttu-id="53feb-113">Le client peut lire le reste du message en appelant la fonction [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)ou [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe) .</span><span class="sxs-lookup"><span data-stu-id="53feb-113">The client can read the remainder of the message by calling either the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex), or [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe) function.</span></span>

<span data-ttu-id="53feb-114">[**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) est généralement appelé par les clients de canal, mais peut également être utilisé par un serveur de canaux.</span><span class="sxs-lookup"><span data-stu-id="53feb-114">[**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) is typically called by pipe clients, but can also be used by a pipe server.</span></span>

<span data-ttu-id="53feb-115">L’exemple suivant montre un client de canal à l’aide de [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe).</span><span class="sxs-lookup"><span data-stu-id="53feb-115">The following example shows a pipe client using [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe).</span></span> <span data-ttu-id="53feb-116">Ce client de canal peut être utilisé avec l’un des serveurs de canaux listés sous Voir aussi.</span><span class="sxs-lookup"><span data-stu-id="53feb-116">This pipe client can be used with any of the pipe servers listed under See Also.</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   HANDLE hPipe; 
   LPTSTR lpszWrite = TEXT("Default message from client"); 
   TCHAR chReadBuf[BUFSIZE]; 
   BOOL fSuccess; 
   DWORD cbRead, dwMode; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1)
   {
      lpszWrite = argv[1]; 
   }
 
   // Try to open a named pipe; wait for it, if necessary. 
    while (1) 
   { 
      hPipe = CreateFile( 
         lpszPipename,   // pipe name 
         GENERIC_READ |  // read and write access 
         GENERIC_WRITE, 
         0,              // no sharing 
         NULL,           // default security attributes
         OPEN_EXISTING,  // opens existing pipe 
         0,              // default attributes 
         NULL);          // no template file 
 
      // Break if the pipe handle is valid. 
      if (hPipe != INVALID_HANDLE_VALUE) 
         break; 
 
      // Exit if an error other than ERROR_PIPE_BUSY occurs. 
      if (GetLastError() != ERROR_PIPE_BUSY) 
      {
         printf("Could not open pipe\n"); 
         return 0;
      }
 
      // All pipe instances are busy, so wait for 20 seconds. 
      if (! WaitNamedPipe(lpszPipename, 20000) ) 
      {
         printf("Could not open pipe\n"); 
         return 0;
      }
  } 
 
   // The pipe connected; change to message-read mode. 
   dwMode = PIPE_READMODE_MESSAGE; 
   fSuccess = SetNamedPipeHandleState( 
      hPipe,    // pipe handle 
      &dwMode,  // new pipe mode 
      NULL,     // don't set maximum bytes 
      NULL);    // don't set maximum time 
   if (!fSuccess) 
   {
      printf("SetNamedPipeHandleState failed.\n"); 
      return 0;
   }
 
   // Send a message to the pipe server and read the response. 
   fSuccess = TransactNamedPipe( 
      hPipe,                  // pipe handle 
      lpszWrite,              // message to server
      (lstrlen(lpszWrite)+1)*sizeof(TCHAR), // message length 
      chReadBuf,              // buffer to receive reply
      BUFSIZE*sizeof(TCHAR),  // size of read buffer
      &cbRead,                // bytes read
      NULL);                  // not overlapped 

   if (!fSuccess && (GetLastError() != ERROR_MORE_DATA)) 
   {
      printf("TransactNamedPipe failed.\n"); 
      return 0;
   }
 
   while(1)
   { 
      _tprintf(TEXT("%s\n"), chReadBuf);

      // Break if TransactNamedPipe or ReadFile is successful
      if(fSuccess)
         break;

      // Read from the pipe if there is more data in the message.
      fSuccess = ReadFile( 
         hPipe,      // pipe handle 
         chReadBuf,  // buffer to receive reply 
         BUFSIZE*sizeof(TCHAR),  // size of buffer 
         &cbRead,  // number of bytes read 
         NULL);    // not overlapped 

      // Exit if an error other than ERROR_MORE_DATA occurs.
      if( !fSuccess && (GetLastError() != ERROR_MORE_DATA)) 
         break;
      else _tprintf( TEXT("%s\n"), chReadBuf); 
   }

   _getch(); 

   CloseHandle(hPipe); 
 
   return 0; 
}
```



<span data-ttu-id="53feb-117">Un client de canal utilise [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) pour combiner les appels de fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) (si nécessaire), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)et [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) dans un appel unique.</span><span class="sxs-lookup"><span data-stu-id="53feb-117">A pipe client uses [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) to combine the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) (if necessary), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe), and [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function calls into a single call.</span></span> <span data-ttu-id="53feb-118">Étant donné que le descripteur de canal est fermé avant le retour de la fonction, tout octet supplémentaire dans le message est perdu si le message est plus grand que la taille spécifiée de la mémoire tampon de lecture.</span><span class="sxs-lookup"><span data-stu-id="53feb-118">Because the pipe handle is closed before the function returns, any additional bytes in the message are lost if the message is larger than the specified size of the read buffer.</span></span> <span data-ttu-id="53feb-119">L’exemple suivant est l’exemple précédent réécrit pour utiliser **CallNamedPipe**.</span><span class="sxs-lookup"><span data-stu-id="53feb-119">The following example is the previous example rewritten to use **CallNamedPipe**.</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   LPTSTR lpszWrite = TEXT("Default message from client"); 
   TCHAR chReadBuf[BUFSIZE]; 
   BOOL fSuccess; 
   DWORD cbRead; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1)
   {
      lpszWrite = argv[1]; 
   }
 
   fSuccess = CallNamedPipe( 
      lpszPipename,        // pipe name 
      lpszWrite,           // message to server 
      (lstrlen(lpszWrite)+1)*sizeof(TCHAR), // message length 
      chReadBuf,              // buffer to receive reply 
      BUFSIZE*sizeof(TCHAR),  // size of read buffer 
      &cbRead,                // number of bytes read 
      20000);                 // waits for 20 seconds 
 
   if (fSuccess || GetLastError() == ERROR_MORE_DATA) 
   { 
      _tprintf( TEXT("%s\n"), chReadBuf ); 
    
      // The pipe is closed; no more data can be read. 
 
      if (! fSuccess) 
      {
         printf("\nExtra data in message was lost\n"); 
      }
   }
 
   _getch(); 

   return 0; 
}
```



## <a name="related-topics"></a><span data-ttu-id="53feb-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="53feb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53feb-121">Serveur de canaux multithread</span><span class="sxs-lookup"><span data-stu-id="53feb-121">Multithreaded pipe server</span></span>](multithreaded-pipe-server.md)
</dt> <dt>

[<span data-ttu-id="53feb-122">Serveur de canaux nommés utilisant des e/s avec chevauchement</span><span class="sxs-lookup"><span data-stu-id="53feb-122">Named pipe server using overlapped I/O</span></span>](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[<span data-ttu-id="53feb-123">Serveur de canaux nommés utilisant les routines de saisie semi-automatique</span><span class="sxs-lookup"><span data-stu-id="53feb-123">Named pipe server using completion routines</span></span>](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
