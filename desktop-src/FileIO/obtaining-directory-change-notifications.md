---
description: Une application peut surveiller le contenu d’un répertoire et de ses sous-répertoires à l’aide de notifications de modification.
ms.assetid: ad884b15-e040-478b-aa99-d8622198f62a
title: Obtention de notifications de modification de répertoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44375c334c3630aee09bf4a13fc23f87cc91e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753564"
---
# <a name="obtaining-directory-change-notifications"></a>Obtention de notifications de modification de répertoire

Une application peut surveiller le contenu d’un répertoire et de ses sous-répertoires à l’aide de notifications de modification. L’attente d’une notification de modification est semblable à une opération de lecture en attente sur un répertoire et, si nécessaire, à ses sous-répertoires. En cas de modification d’un répertoire surveillé, l’opération de lecture est terminée. Par exemple, une application peut utiliser ces fonctions pour mettre à jour une liste de répertoires chaque fois qu’un nom de fichier dans le répertoire analysé change.

Une application peut spécifier un ensemble de conditions qui déclenchent une notification de modification à l’aide de la fonction [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) . Les conditions incluent les modifications apportées aux noms de fichiers, aux noms de répertoires, aux attributs, à la taille de fichier, à l’heure de la dernière écriture et à la sécurité. Cette fonction retourne également un handle qui peut être attendu à l’aide des [fonctions Wait](/windows/desktop/Sync/wait-functions). Si la condition d’attente est satisfaite, [**FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification) peut être utilisé pour fournir un handle de notification pour attendre les modifications ultérieures. Toutefois, ces fonctions n’indiquent pas la modification réelle qui a satisfait à la condition d’attente.

Utilisez [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) pour fermer le descripteur de notification.

Pour récupérer des informations sur la modification spécifique dans le cadre de la notification, utilisez la fonction [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) . Cette fonction vous permet également de fournir une routine de saisie semi-automatique.

Pour suivre les modifications apportées à un volume, consultez [modifier les journaux](change-journals.md).

L’exemple suivant analyse l’arborescence de répertoires pour les modifications de nom de répertoire. Il surveille également un répertoire pour les modifications de nom de fichier. L’exemple utilise la fonction [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) pour créer deux descripteurs de notification et la fonction [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) pour attendre les handles. Chaque fois qu’un répertoire est créé ou supprimé dans l’arborescence, l’exemple doit mettre à jour l’ensemble de l’arborescence de répertoires. Chaque fois qu’un fichier est créé ou supprimé dans le répertoire, l’exemple doit actualiser le répertoire.

> [!Note]
>
> Cet exemple simpliste utilise la fonction [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) pour la terminaison et le nettoyage, mais les applications plus complexes doivent toujours utiliser une gestion des ressources appropriée comme [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) , le cas échéant.

 


```C++
#include <windows.h>
#include <stdlib.h>
#include <stdio.h>
#include <tchar.h>

void RefreshDirectory(LPTSTR);
void RefreshTree(LPTSTR);
void WatchDirectory(LPTSTR);

void _tmain(int argc, TCHAR *argv[])
{
    if(argc != 2)
    {
        _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
        return;
    }

    WatchDirectory(argv[1]);
}

void WatchDirectory(LPTSTR lpDir)
{
   DWORD dwWaitStatus; 
   HANDLE dwChangeHandles[2]; 
   TCHAR lpDrive[4];
   TCHAR lpFile[_MAX_FNAME];
   TCHAR lpExt[_MAX_EXT];

   _tsplitpath_s(lpDir, lpDrive, 4, NULL, 0, lpFile, _MAX_FNAME, lpExt, _MAX_EXT);

   lpDrive[2] = (TCHAR)'\\';
   lpDrive[3] = (TCHAR)'\0';
 
// Watch the directory for file creation and deletion. 
 
   dwChangeHandles[0] = FindFirstChangeNotification( 
      lpDir,                         // directory to watch 
      FALSE,                         // do not watch subtree 
      FILE_NOTIFY_CHANGE_FILE_NAME); // watch file name changes 
 
   if (dwChangeHandles[0] == INVALID_HANDLE_VALUE) 
   {
     printf("\n ERROR: FindFirstChangeNotification function failed.\n");
     ExitProcess(GetLastError()); 
   }
 
// Watch the subtree for directory creation and deletion. 
 
   dwChangeHandles[1] = FindFirstChangeNotification( 
      lpDrive,                       // directory to watch 
      TRUE,                          // watch the subtree 
      FILE_NOTIFY_CHANGE_DIR_NAME);  // watch dir name changes 
 
   if (dwChangeHandles[1] == INVALID_HANDLE_VALUE) 
   {
     printf("\n ERROR: FindFirstChangeNotification function failed.\n");
     ExitProcess(GetLastError()); 
   }
 

// Make a final validation check on our handles.

   if ((dwChangeHandles[0] == NULL) || (dwChangeHandles[1] == NULL))
   {
     printf("\n ERROR: Unexpected NULL from FindFirstChangeNotification.\n");
     ExitProcess(GetLastError()); 
   }

// Change notification is set. Now wait on both notification 
// handles and refresh accordingly. 
 
   while (TRUE) 
   { 
   // Wait for notification.
 
      printf("\nWaiting for notification...\n");

      dwWaitStatus = WaitForMultipleObjects(2, dwChangeHandles, 
         FALSE, INFINITE); 
 
      switch (dwWaitStatus) 
      { 
         case WAIT_OBJECT_0: 
 
         // A file was created, renamed, or deleted in the directory.
         // Refresh this directory and restart the notification.
 
             RefreshDirectory(lpDir); 
             if ( FindNextChangeNotification(dwChangeHandles[0]) == FALSE )
             {
               printf("\n ERROR: FindNextChangeNotification function failed.\n");
               ExitProcess(GetLastError()); 
             }
             break; 
 
         case WAIT_OBJECT_0 + 1: 
 
         // A directory was created, renamed, or deleted.
         // Refresh the tree and restart the notification.
 
             RefreshTree(lpDrive); 
             if (FindNextChangeNotification(dwChangeHandles[1]) == FALSE )
             {
               printf("\n ERROR: FindNextChangeNotification function failed.\n");
               ExitProcess(GetLastError()); 
             }
             break; 
 
         case WAIT_TIMEOUT:

         // A timeout occurred, this would happen if some value other 
         // than INFINITE is used in the Wait call and no changes occur.
         // In a single-threaded environment you might not want an
         // INFINITE wait.
 
            printf("\nNo changes in the timeout period.\n");
            break;

         default: 
            printf("\n ERROR: Unhandled dwWaitStatus.\n");
            ExitProcess(GetLastError());
            break;
      }
   }
}

void RefreshDirectory(LPTSTR lpDir)
{
   // This is where you might place code to refresh your
   // directory listing, but not the subtree because it
   // would not be necessary.

   _tprintf(TEXT("Directory (%s) changed.\n"), lpDir);
}

void RefreshTree(LPTSTR lpDrive)
{
   // This is where you might place code to refresh your
   // directory listing, including the subtree.

   _tprintf(TEXT("Directory tree (%s) changed.\n"), lpDrive);
}
```



 

 
