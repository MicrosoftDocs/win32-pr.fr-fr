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
# <a name="creating-named-shared-memory"></a>Création d’une mémoire partagée nommée

Pour partager des données, plusieurs processus peuvent utiliser des fichiers mappés en mémoire que le fichier d’échange du système stocke.

## <a name="first-process"></a>Premier processus

Le premier processus crée l’objet de mappage de fichier en appelant la fonction [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) avec une **\_ \_ valeur de handle non valide** et un nom pour l’objet. À l’aide de l’indicateur de **page \_ ReadWrite** , le processus dispose d’une autorisation de lecture/écriture sur la mémoire via n’importe quelle vue de fichier qui est créée.

Le processus utilise ensuite le descripteur d’objet de mappage de fichiers que [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) renvoie dans un appel à [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) pour créer une vue du fichier dans l’espace d’adressage du processus. La fonction **MapViewOfFile** retourne un pointeur vers l’affichage des fichiers, `pBuf` . Le processus utilise ensuite la fonction [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) pour écrire une chaîne dans la vue qui est accessible par d’autres processus.

Le fait de préfixer les noms des objets de mappage de fichiers avec « global \\ » permet aux processus de communiquer entre eux, même s’ils se trouvent dans des sessions Terminal Server différentes. Cela nécessite que le premier processus ait le privilège [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) .

Lorsque le processus n’a plus besoin d’accéder à l’objet de mappage de fichier, il doit appeler la fonction [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) . Lorsque tous les descripteurs sont fermés, le système peut libérer la section du fichier d’échange utilisé par l’objet.


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



## <a name="second-process"></a>Deuxième processus

Un deuxième processus peut accéder à la chaîne écrite dans la mémoire partagée par le premier processus en appelant la fonction [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) en spécifiant le même nom pour l’objet de mappage que le premier processus. Elle peut ensuite utiliser la fonction [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) pour obtenir un pointeur vers l’affichage des fichiers, `pBuf` . Le processus peut afficher cette chaîne comme n’importe quelle autre chaîne. Dans cet exemple, la boîte de message affichée contient le message « message du premier processus » qui a été écrit par le premier processus.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Partage de fichiers et de mémoire](sharing-files-and-memory.md)
</dt> </dl>

 

 
