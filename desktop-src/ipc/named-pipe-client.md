---
description: L’exemple de code montre un client de canal qui ouvre un canal nommé, définit le descripteur de canal en mode de lecture de message, utilise la fonction WriteFile pour envoyer une demande au serveur et utilise la fonction ReadFile pour lire la réponse des serveurs.
ms.assetid: 0779242c-45f4-4cd9-9c9f-36cff54c8dee
title: Client de canal nommé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6318edd7d5b41c701e3112188a896c0529338805
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122266"
---
# <a name="named-pipe-client"></a>Client de canal nommé

Un client de canal nommé utilise la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir un handle vers un canal nommé. Si le canal existe mais que toutes ses instances sont occupées, **CreateFile** retourne une **\_ \_ valeur de handle non valide** et la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne un canal d’erreur \_ \_ occupé. Dans ce cas, le client de canal nommé utilise la fonction [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) pour attendre qu’une instance du canal nommé devienne disponible.

La fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) échoue si l’accès spécifié est incompatible avec l’accès spécifié (duplex, sortant ou entrant) lorsque le serveur a créé le canal. Pour un canal duplex, le client peut spécifier un accès en lecture, en écriture ou en lecture/écriture ; pour un canal sortant (serveur en écriture seule), le client doit spécifier un accès en lecture seule. et pour un canal entrant (serveur en lecture seule), le client doit spécifier un accès en écriture seule.

Le handle retourné par [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) est défini par défaut sur le mode de lecture en octets, le mode d’attente bloquant, le mode avec chevauchement désactivé et le mode écriture désactivée. Le client de canal peut utiliser **CreateFile** pour activer le mode avec chevauchement en spécifiant l’indicateur de fichier avec \_ \_ chevauchement ou pour activer le mode d’écriture en spécifiant l’option d’écriture de l’indicateur de fichier \_ \_ \_ . Le client peut utiliser la fonction [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) pour activer le mode non bloquant en spécifiant l’utilisation de canal \_ ou pour activer le mode de lecture de message en spécifiant le message de canal \_ READMODE \_ .

L’exemple suivant montre un client de canal qui ouvre un canal nommé, définit le descripteur de canal en mode de lecture de message, utilise la fonction [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) pour envoyer une demande au serveur et utilise la fonction [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) pour lire la réponse du serveur. Ce client de canal peut être utilisé avec l’un des serveurs de type de message figurant au bas de cette rubrique. Avec un serveur de type Byte, toutefois, ce client de canal échoue lorsqu’il appelle [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) pour passer en mode de lecture de message. Étant donné que le client lit à partir du canal en mode de lecture de message, il est possible que l’opération **ReadFile** retourne zéro après avoir lu un message partiel. Cela se produit lorsque le message est plus volumineux que le tampon de lecture. Dans ce cas, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une erreur \_ plus \_ de données et le client peut lire le reste du message à l’aide d’appels supplémentaires à **ReadFile**.

Ce client de canal peut être utilisé avec l’un des serveurs de canaux listés sous Voir aussi.


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   HANDLE hPipe; 
   LPTSTR lpvMessage=TEXT("Default message from client."); 
   TCHAR  chBuf[BUFSIZE]; 
   BOOL   fSuccess = FALSE; 
   DWORD  cbRead, cbToWrite, cbWritten, dwMode; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1 )
      lpvMessage = argv[1];
 
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
         _tprintf( TEXT("Could not open pipe. GLE=%d\n"), GetLastError() ); 
         return -1;
      }
 
      // All pipe instances are busy, so wait for 20 seconds. 
 
      if ( ! WaitNamedPipe(lpszPipename, 20000)) 
      { 
         printf("Could not open pipe: 20 second wait timed out."); 
         return -1;
      } 
   } 
 
// The pipe connected; change to message-read mode. 
 
   dwMode = PIPE_READMODE_MESSAGE; 
   fSuccess = SetNamedPipeHandleState( 
      hPipe,    // pipe handle 
      &dwMode,  // new pipe mode 
      NULL,     // don't set maximum bytes 
      NULL);    // don't set maximum time 
   if ( ! fSuccess) 
   {
      _tprintf( TEXT("SetNamedPipeHandleState failed. GLE=%d\n"), GetLastError() ); 
      return -1;
   }
 
// Send a message to the pipe server. 
 
   cbToWrite = (lstrlen(lpvMessage)+1)*sizeof(TCHAR);
   _tprintf( TEXT("Sending %d byte message: \"%s\"\n"), cbToWrite, lpvMessage); 

   fSuccess = WriteFile( 
      hPipe,                  // pipe handle 
      lpvMessage,             // message 
      cbToWrite,              // message length 
      &cbWritten,             // bytes written 
      NULL);                  // not overlapped 

   if ( ! fSuccess) 
   {
      _tprintf( TEXT("WriteFile to pipe failed. GLE=%d\n"), GetLastError() ); 
      return -1;
   }

   printf("\nMessage sent to server, receiving reply as follows:\n");
 
   do 
   { 
   // Read from the pipe. 
 
      fSuccess = ReadFile( 
         hPipe,    // pipe handle 
         chBuf,    // buffer to receive reply 
         BUFSIZE*sizeof(TCHAR),  // size of buffer 
         &cbRead,  // number of bytes read 
         NULL);    // not overlapped 
 
      if ( ! fSuccess && GetLastError() != ERROR_MORE_DATA )
         break; 
 
      _tprintf( TEXT("\"%s\"\n"), chBuf ); 
   } while ( ! fSuccess);  // repeat loop if ERROR_MORE_DATA 

   if ( ! fSuccess)
   {
      _tprintf( TEXT("ReadFile from pipe failed. GLE=%d\n"), GetLastError() );
      return -1;
   }

   printf("\n<End of message, press ENTER to terminate connection and exit>");
   _getch();
 
   CloseHandle(hPipe); 
 
   return 0; 
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Serveur de canaux multithread](multithreaded-pipe-server.md)
</dt> <dt>

[Serveur de canaux nommés utilisant des e/s avec chevauchement](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[Serveur de canaux nommés utilisant les routines de saisie semi-automatique](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
