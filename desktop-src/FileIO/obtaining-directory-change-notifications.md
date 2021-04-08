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
# <a name="obtaining-directory-change-notifications"></a><span data-ttu-id="c67b2-103">Obtention de notifications de modification de répertoire</span><span class="sxs-lookup"><span data-stu-id="c67b2-103">Obtaining Directory Change Notifications</span></span>

<span data-ttu-id="c67b2-104">Une application peut surveiller le contenu d’un répertoire et de ses sous-répertoires à l’aide de notifications de modification.</span><span class="sxs-lookup"><span data-stu-id="c67b2-104">An application can monitor the contents of a directory and its subdirectories by using change notifications.</span></span> <span data-ttu-id="c67b2-105">L’attente d’une notification de modification est semblable à une opération de lecture en attente sur un répertoire et, si nécessaire, à ses sous-répertoires.</span><span class="sxs-lookup"><span data-stu-id="c67b2-105">Waiting for a change notification is similar to having a read operation pending against a directory and, if necessary, its subdirectories.</span></span> <span data-ttu-id="c67b2-106">En cas de modification d’un répertoire surveillé, l’opération de lecture est terminée.</span><span class="sxs-lookup"><span data-stu-id="c67b2-106">When something changes within the directory being watched, the read operation is completed.</span></span> <span data-ttu-id="c67b2-107">Par exemple, une application peut utiliser ces fonctions pour mettre à jour une liste de répertoires chaque fois qu’un nom de fichier dans le répertoire analysé change.</span><span class="sxs-lookup"><span data-stu-id="c67b2-107">For example, an application can use these functions to update a directory listing whenever a file name within the monitored directory changes.</span></span>

<span data-ttu-id="c67b2-108">Une application peut spécifier un ensemble de conditions qui déclenchent une notification de modification à l’aide de la fonction [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) .</span><span class="sxs-lookup"><span data-stu-id="c67b2-108">An application can specify a set of conditions that trigger a change notification by using the [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) function.</span></span> <span data-ttu-id="c67b2-109">Les conditions incluent les modifications apportées aux noms de fichiers, aux noms de répertoires, aux attributs, à la taille de fichier, à l’heure de la dernière écriture et à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="c67b2-109">The conditions include changes to file names, directory names, attributes, file size, time of last write, and security.</span></span> <span data-ttu-id="c67b2-110">Cette fonction retourne également un handle qui peut être attendu à l’aide des [fonctions Wait](/windows/desktop/Sync/wait-functions).</span><span class="sxs-lookup"><span data-stu-id="c67b2-110">This function also returns a handle that can be waited on by using the [wait functions](/windows/desktop/Sync/wait-functions).</span></span> <span data-ttu-id="c67b2-111">Si la condition d’attente est satisfaite, [**FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification) peut être utilisé pour fournir un handle de notification pour attendre les modifications ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c67b2-111">If the wait condition is satisfied, [**FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification) can be used to provide a notification handle to wait on subsequent changes.</span></span> <span data-ttu-id="c67b2-112">Toutefois, ces fonctions n’indiquent pas la modification réelle qui a satisfait à la condition d’attente.</span><span class="sxs-lookup"><span data-stu-id="c67b2-112">However, these functions do not indicate the actual change that satisfied the wait condition.</span></span>

<span data-ttu-id="c67b2-113">Utilisez [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) pour fermer le descripteur de notification.</span><span class="sxs-lookup"><span data-stu-id="c67b2-113">Use [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) to close the notification handle.</span></span>

<span data-ttu-id="c67b2-114">Pour récupérer des informations sur la modification spécifique dans le cadre de la notification, utilisez la fonction [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) .</span><span class="sxs-lookup"><span data-stu-id="c67b2-114">To retrieve information about the specific change as part of the notification, use the [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) function.</span></span> <span data-ttu-id="c67b2-115">Cette fonction vous permet également de fournir une routine de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="c67b2-115">This function also enables you to provide a completion routine.</span></span>

<span data-ttu-id="c67b2-116">Pour suivre les modifications apportées à un volume, consultez [modifier les journaux](change-journals.md).</span><span class="sxs-lookup"><span data-stu-id="c67b2-116">To track changes on a volume, see [change journals](change-journals.md).</span></span>

<span data-ttu-id="c67b2-117">L’exemple suivant analyse l’arborescence de répertoires pour les modifications de nom de répertoire.</span><span class="sxs-lookup"><span data-stu-id="c67b2-117">The following example monitors the directory tree for directory name changes.</span></span> <span data-ttu-id="c67b2-118">Il surveille également un répertoire pour les modifications de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="c67b2-118">It also monitors a directory for file name changes.</span></span> <span data-ttu-id="c67b2-119">L’exemple utilise la fonction [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) pour créer deux descripteurs de notification et la fonction [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) pour attendre les handles.</span><span class="sxs-lookup"><span data-stu-id="c67b2-119">The example uses the [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) function to create two notification handles and the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function to wait on the handles.</span></span> <span data-ttu-id="c67b2-120">Chaque fois qu’un répertoire est créé ou supprimé dans l’arborescence, l’exemple doit mettre à jour l’ensemble de l’arborescence de répertoires.</span><span class="sxs-lookup"><span data-stu-id="c67b2-120">Whenever a directory is created or deleted in the tree, the example should update the entire directory tree.</span></span> <span data-ttu-id="c67b2-121">Chaque fois qu’un fichier est créé ou supprimé dans le répertoire, l’exemple doit actualiser le répertoire.</span><span class="sxs-lookup"><span data-stu-id="c67b2-121">Whenever a file is created or deleted in the directory, the example should refresh the directory.</span></span>

> [!Note]
>
> <span data-ttu-id="c67b2-122">Cet exemple simpliste utilise la fonction [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) pour la terminaison et le nettoyage, mais les applications plus complexes doivent toujours utiliser une gestion des ressources appropriée comme [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="c67b2-122">This simplistic example uses the [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) function for termination and cleanup, but more complex applications should always use proper resource management such as [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) where appropriate.</span></span>

 


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



 

 
