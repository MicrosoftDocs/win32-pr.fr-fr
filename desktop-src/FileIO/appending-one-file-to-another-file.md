---
description: Exemple de code qui montre comment une application peut ajouter un fichier à la fin d’un autre fichier, y compris comment ouvrir et fermer des fichiers, lire et écrire dans des fichiers, et verrouiller et déverrouiller des fichiers.
ms.assetid: e4d1f842-16a1-47e4-84b4-9bb44aaa1dc5
title: Ajout d’un fichier à un autre fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 546d24fe88a2bbf22c190a0caca3b3f98e753720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518718"
---
# <a name="appending-one-file-to-another-file"></a><span data-ttu-id="cd9d3-103">Ajout d’un fichier à un autre fichier</span><span class="sxs-lookup"><span data-stu-id="cd9d3-103">Appending One File to Another File</span></span>

<span data-ttu-id="cd9d3-104">L’exemple de code de cette rubrique montre comment ouvrir et fermer des fichiers, lire et écrire dans des fichiers, et verrouiller et déverrouiller des fichiers.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-104">The code example in this topic shows you how to open and close files, read and write to files, and lock and unlock files.</span></span>

<span data-ttu-id="cd9d3-105">Dans l’exemple, l’application ajoute un fichier à la fin d’un autre fichier.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-105">In the example, the application appends one file to the end of another file.</span></span> <span data-ttu-id="cd9d3-106">Tout d’abord, l’application ouvre le fichier ajouté avec les autorisations qui autorisent uniquement l’écriture sur l’application.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-106">First, the application opens the file being appended with permissions that allow only the application to write to it.</span></span> <span data-ttu-id="cd9d3-107">Toutefois, pendant le processus d’ajout, les autres processus peuvent ouvrir le fichier avec l’autorisation de lecture seule, qui fournit une vue d’instantané du fichier qui est ajouté.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-107">However, during the append process other processes can open the file with read-only permission, which provides a snapshot view of the file being appended.</span></span> <span data-ttu-id="cd9d3-108">Ensuite, le fichier est verrouillé pendant le processus d’ajout réel pour garantir l’intégrité des données écrites dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-108">Then, the file is locked during the actual append process to ensure the integrity of the data being written to the file.</span></span>

<span data-ttu-id="cd9d3-109">Cet exemple n’utilise pas de transactions.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-109">This example does not use transactions.</span></span> <span data-ttu-id="cd9d3-110">Si vous utilisiez des opérations traitées, vous ne pouvez avoir qu’un accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-110">If you were using transacted operations, you would only be able have read-only access.</span></span> <span data-ttu-id="cd9d3-111">Dans ce cas, vous ne verrez les données ajoutées qu’une fois l’opération de validation de transaction terminée.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-111">In this case, you would only see the appended data after the transaction commit operation completed.</span></span>

<span data-ttu-id="cd9d3-112">L’exemple montre également que l’application ouvre deux fichiers à l’aide de [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea):</span><span class="sxs-lookup"><span data-stu-id="cd9d3-112">The example also shows that the application opens two files by using [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea):</span></span>

-   <span data-ttu-id="cd9d3-113">One.txt est ouvert pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-113">One.txt is opened for reading.</span></span>
-   <span data-ttu-id="cd9d3-114">Two.txt est ouvert pour l’écriture et la lecture partagée.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-114">Two.txt is opened for writing and shared reading.</span></span>

<span data-ttu-id="cd9d3-115">L’application utilise ensuite [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) et [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) pour ajouter le contenu de One.txt à la fin de Two.txt en lisant et en écrivant les blocs de 4 Ko.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-115">Then the application uses [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) and [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) to append the contents of One.txt to the end of Two.txt by reading and writing the 4 KB blocks.</span></span> <span data-ttu-id="cd9d3-116">Toutefois, avant d’écrire dans le deuxième fichier, l’application utilise [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) pour définir le pointeur du deuxième fichier à la fin de ce fichier et utilise [**lockfile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) pour verrouiller la zone à écrire.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-116">However, before writing to the second file, the application uses [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) to set the pointer of the second file to the end of that file, and uses [**LockFile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) to lock the area to be written.</span></span> <span data-ttu-id="cd9d3-117">Cela empêche un autre thread ou processus avec un handle dupliqué d’accéder à la zone pendant que l’opération d’écriture est en cours.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-117">This prevents another thread or process with a duplicate handle from accessing the area while the write operation is in progress.</span></span> <span data-ttu-id="cd9d3-118">Lorsque chaque opération d’écriture est terminée, [**UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) est utilisé pour déverrouiller la zone verrouillée.</span><span class="sxs-lookup"><span data-stu-id="cd9d3-118">When each write operation is complete, [**UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) is used to unlock the locked area.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

void main()
{
  HANDLE hFile;
  HANDLE hAppend;
  DWORD  dwBytesRead, dwBytesWritten, dwPos;
  BYTE   buff[4096];

  // Open the existing file.

  hFile = CreateFile(TEXT("one.txt"), // open One.txt
            GENERIC_READ,             // open for reading
            0,                        // do not share
            NULL,                     // no security
            OPEN_EXISTING,            // existing file only
            FILE_ATTRIBUTE_NORMAL,    // normal file
            NULL);                    // no attr. template

  if (hFile == INVALID_HANDLE_VALUE)
  {
     printf("Could not open One.txt."); 
     return;
  }

  // Open the existing file, or if the file does not exist,
  // create a new file.

  hAppend = CreateFile(TEXT("two.txt"), // open Two.txt
              FILE_APPEND_DATA,         // open for writing
              FILE_SHARE_READ,          // allow multiple readers
              NULL,                     // no security
              OPEN_ALWAYS,              // open or create
              FILE_ATTRIBUTE_NORMAL,    // normal file
              NULL);                    // no attr. template

  if (hAppend == INVALID_HANDLE_VALUE)
  {
     printf("Could not open Two.txt."); 
     return;
  }

  // Append the first file to the end of the second file.
  // Lock the second file to prevent another process from
  // accessing it while writing to it. Unlock the
  // file when writing is complete.

  while (ReadFile(hFile, buff, sizeof(buff), &dwBytesRead, NULL)
      && dwBytesRead > 0)
    {
    dwPos = SetFilePointer(hAppend, 0, NULL, FILE_END);
    LockFile(hAppend, dwPos, 0, dwBytesRead, 0);
    WriteFile(hAppend, buff, dwBytesRead, &dwBytesWritten, NULL);
    UnlockFile(hAppend, dwPos, 0, dwBytesRead, 0);
    }

  // Close both files.

  CloseHandle(hFile);
  CloseHandle(hAppend);
}
```



 

 



