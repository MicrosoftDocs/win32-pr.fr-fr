---
description: Pour partager des données, plusieurs processus peuvent utiliser des fichiers mappés en mémoire que le fichier d’échange du système stocke.
ms.assetid: 17458be2-3ef7-42f2-a717-abf73ac4846f
title: Création d’une mémoire partagée nommée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ac708497ceb12ed099c7a9c0b3788d7a05a925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517479"
---
# <a name="creating-named-shared-memory"></a><span data-ttu-id="ae6e0-103">Création d’une mémoire partagée nommée</span><span class="sxs-lookup"><span data-stu-id="ae6e0-103">Creating Named Shared Memory</span></span>

<span data-ttu-id="ae6e0-104">Pour partager des données, plusieurs processus peuvent utiliser des fichiers mappés en mémoire que le fichier d’échange du système stocke.</span><span class="sxs-lookup"><span data-stu-id="ae6e0-104">To share data, multiple processes can use memory-mapped files that the system paging file stores.</span></span>

## <a name="first-process"></a><span data-ttu-id="ae6e0-105">Premier processus</span><span class="sxs-lookup"><span data-stu-id="ae6e0-105">First Process</span></span>

<span data-ttu-id="ae6e0-106">Le premier processus crée l’objet de mappage de fichier en appelant la fonction [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) avec une **\_ \_ valeur de handle non valide** et un nom pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="ae6e0-106">The first process creates the file mapping object by calling the [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) function with **INVALID\_HANDLE\_VALUE** and a name for the object.</span></span> <span data-ttu-id="ae6e0-107">À l’aide de l’indicateur de **page \_ ReadWrite** , le processus dispose d’une autorisation de lecture/écriture sur la mémoire via n’importe quelle vue de fichier qui est créée.</span><span class="sxs-lookup"><span data-stu-id="ae6e0-107">By using the **PAGE\_READWRITE** flag, the process has read/write permission to the memory through any file views that are created.</span></span>

<span data-ttu-id="ae6e0-108">Le processus utilise ensuite le descripteur d’objet de mappage de fichiers que [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) renvoie dans un appel à [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) pour créer une vue du fichier dans l’espace d’adressage du processus.</span><span class="sxs-lookup"><span data-stu-id="ae6e0-108">Then the process uses the file mapping object handle that [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) returns in a call to [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) to create a view of the file in the process address space.</span></span> <span data-ttu-id="ae6e0-109">La fonction **MapViewOfFile** retourne un pointeur vers l’affichage des fichiers, `pBuf` .</span><span class="sxs-lookup"><span data-stu-id="ae6e0-109">The **MapViewOfFile** function returns a pointer to the file view, `pBuf`.</span></span> <span data-ttu-id="ae6e0-110">Le processus utilise ensuite la fonction [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) pour écrire une chaîne dans la vue qui est accessible par d’autres processus.</span><span class="sxs-lookup"><span data-stu-id="ae6e0-110">The process then uses the [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) function to write a string to the view that can be accessed by other processes.</span></span>

<span data-ttu-id="ae6e0-111">Le fait de préfixer les noms des objets de mappage de fichiers avec « global \\ » permet aux processus de communiquer entre eux, même s’ils se trouvent dans des sessions Terminal Server différentes.</span><span class="sxs-lookup"><span data-stu-id="ae6e0-111">Prefixing the file mapping object names with "Global\\" allows processes to communicate with each other even if they are in different terminal server sessions.</span></span> <span data-ttu-id="ae6e0-112">Cela nécessite que le premier processus ait le privilège [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="ae6e0-112">This requires that the first process must have the [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) privilege.</span></span>

<span data-ttu-id="ae6e0-113">Lorsque le processus n’a plus besoin d’accéder à l’objet de mappage de fichier, il doit appeler la fonction [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="ae6e0-113">When the process no longer needs access to the file mapping object, it should call the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="ae6e0-114">Lorsque tous les descripteurs sont fermés, le système peut libérer la section du fichier d’échange utilisé par l’objet.</span><span class="sxs-lookup"><span data-stu-id="ae6e0-114">When all handles are closed, the system can free the section of the paging file that the object uses.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUF_SIZE 256
TCHAR szName[]=TEXT("Global\\MyFileMappingObject");
TCHAR szMsg[]=TEXT("Message from first process.");

int _tmain()
{
   HANDLE hMapFile;
   LPCTSTR pBuf;

   hMapFile = CreateFileMapping(
                 INVALID_HANDLE_VALUE,    // use paging file
                 NULL,                    // default security
                 PAGE_READWRITE,          // read/write access
                 0,                       // maximum object size (high-order DWORD)
                 BUF_SIZE,                // maximum object size (low-order DWORD)
                 szName);                 // name of mapping object

   if (hMapFile == NULL)
   {
      _tprintf(TEXT("Could not create file mapping object (%d).\n"),
             GetLastError());
      return 1;
   }
   pBuf = (LPTSTR) MapViewOfFile(hMapFile,   // handle to map object
                        FILE_MAP_ALL_ACCESS, // read/write permission
                        0,
                        0,
                        BUF_SIZE);

   if (pBuf == NULL)
   {
      _tprintf(TEXT("Could not map view of file (%d).\n"),
             GetLastError());

       CloseHandle(hMapFile);

      return 1;
   }


   CopyMemory((PVOID)pBuf, szMsg, (_tcslen(szMsg) * sizeof(TCHAR)));
    _getch();

   UnmapViewOfFile(pBuf);

   CloseHandle(hMapFile);

   return 0;
}
```



## <a name="second-process"></a><span data-ttu-id="ae6e0-115">Deuxième processus</span><span class="sxs-lookup"><span data-stu-id="ae6e0-115">Second Process</span></span>

<span data-ttu-id="ae6e0-116">Un deuxième processus peut accéder à la chaîne écrite dans la mémoire partagée par le premier processus en appelant la fonction [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) en spécifiant le même nom pour l’objet de mappage que le premier processus.</span><span class="sxs-lookup"><span data-stu-id="ae6e0-116">A second process can access the string written to the shared memory by the first process by calling the [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) function specifying the same name for the mapping object as the first process.</span></span> <span data-ttu-id="ae6e0-117">Elle peut ensuite utiliser la fonction [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) pour obtenir un pointeur vers l’affichage des fichiers, `pBuf` .</span><span class="sxs-lookup"><span data-stu-id="ae6e0-117">Then it can use the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function to obtain a pointer to the file view, `pBuf`.</span></span> <span data-ttu-id="ae6e0-118">Le processus peut afficher cette chaîne comme n’importe quelle autre chaîne.</span><span class="sxs-lookup"><span data-stu-id="ae6e0-118">The process can display this string as it would any other string.</span></span> <span data-ttu-id="ae6e0-119">Dans cet exemple, la boîte de message affichée contient le message « message du premier processus » qui a été écrit par le premier processus.</span><span class="sxs-lookup"><span data-stu-id="ae6e0-119">In this example, the message box displayed contains the message "Message from first process" that was written by the first process.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <tchar.h>
#pragma comment(lib, "user32.lib")

#define BUF_SIZE 256
TCHAR szName[]=TEXT("Global\\MyFileMappingObject");

int _tmain()
{
   HANDLE hMapFile;
   LPCTSTR pBuf;

   hMapFile = OpenFileMapping(
                   FILE_MAP_ALL_ACCESS,   // read/write access
                   FALSE,                 // do not inherit the name
                   szName);               // name of mapping object

   if (hMapFile == NULL)
   {
      _tprintf(TEXT("Could not open file mapping object (%d).\n"),
             GetLastError());
      return 1;
   }

   pBuf = (LPTSTR) MapViewOfFile(hMapFile, // handle to map object
               FILE_MAP_ALL_ACCESS,  // read/write permission
               0,
               0,
               BUF_SIZE);

   if (pBuf == NULL)
   {
      _tprintf(TEXT("Could not map view of file (%d).\n"),
             GetLastError());

      CloseHandle(hMapFile);

      return 1;
   }

   MessageBox(NULL, pBuf, TEXT("Process2"), MB_OK);

   UnmapViewOfFile(pBuf);

   CloseHandle(hMapFile);

   return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="ae6e0-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ae6e0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae6e0-121">Partage de fichiers et de mémoire</span><span class="sxs-lookup"><span data-stu-id="ae6e0-121">Sharing Files and Memory</span></span>](sharing-files-and-memory.md)
</dt> </dl>

 

 
