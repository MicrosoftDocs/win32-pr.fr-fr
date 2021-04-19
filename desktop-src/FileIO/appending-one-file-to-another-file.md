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
# <a name="appending-one-file-to-another-file"></a>Ajout d’un fichier à un autre fichier

L’exemple de code de cette rubrique montre comment ouvrir et fermer des fichiers, lire et écrire dans des fichiers, et verrouiller et déverrouiller des fichiers.

Dans l’exemple, l’application ajoute un fichier à la fin d’un autre fichier. Tout d’abord, l’application ouvre le fichier ajouté avec les autorisations qui autorisent uniquement l’écriture sur l’application. Toutefois, pendant le processus d’ajout, les autres processus peuvent ouvrir le fichier avec l’autorisation de lecture seule, qui fournit une vue d’instantané du fichier qui est ajouté. Ensuite, le fichier est verrouillé pendant le processus d’ajout réel pour garantir l’intégrité des données écrites dans le fichier.

Cet exemple n’utilise pas de transactions. Si vous utilisiez des opérations traitées, vous ne pouvez avoir qu’un accès en lecture seule. Dans ce cas, vous ne verrez les données ajoutées qu’une fois l’opération de validation de transaction terminée.

L’exemple montre également que l’application ouvre deux fichiers à l’aide de [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea):

-   One.txt est ouvert pour la lecture.
-   Two.txt est ouvert pour l’écriture et la lecture partagée.

L’application utilise ensuite [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) et [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) pour ajouter le contenu de One.txt à la fin de Two.txt en lisant et en écrivant les blocs de 4 Ko. Toutefois, avant d’écrire dans le deuxième fichier, l’application utilise [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) pour définir le pointeur du deuxième fichier à la fin de ce fichier et utilise [**lockfile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) pour verrouiller la zone à écrire. Cela empêche un autre thread ou processus avec un handle dupliqué d’accéder à la zone pendant que l’opération d’écriture est en cours. Lorsque chaque opération d’écriture est terminée, [**UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) est utilisé pour déverrouiller la zone verrouillée.


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



 

 



