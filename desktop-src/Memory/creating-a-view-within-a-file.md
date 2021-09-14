---
description: Si vous souhaitez afficher une partie du fichier qui ne commence pas au début du fichier, vous devez créer un objet de mappage de fichier.
ms.assetid: e47a0e79-3000-479b-afba-dcd36210ea3d
title: Création d’une vue dans un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9425a1c491a5c7d8ae7861d53418ee0f349bf212
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094189"
---
# <a name="creating-a-view-within-a-file"></a>Création d’une vue dans un fichier

Si vous souhaitez afficher une partie du fichier qui ne commence pas au début du fichier, vous devez créer un objet de mappage de fichier. Cet objet représente la taille de la partie du fichier que vous souhaitez afficher, ainsi que le décalage dans le fichier. Par exemple, si vous souhaitez afficher 1 kilo-octet (1K) qui commence 131 072 octets (128 Ko) dans le fichier, vous devez créer un objet de mappage de fichier d’au moins 132 096 octets (129K) en taille. La vue démarre 131 072 octets (128 Ko) dans le fichier et s’étend sur au moins 1 024 octets. Cet exemple suppose une granularité d’allocation de fichier de 64 Ko.

La granularité d’allocation de fichiers affecte l’endroit où une vue cartographique peut démarrer. Une vue cartographique doit commencer à un offset dans le fichier qui est un multiple de la granularité d’allocation de fichier. Par conséquent, les données que vous souhaitez afficher peuvent être le décalage de fichier modulo la granularité d’allocation dans la vue. La taille de la vue correspond au décalage du modulo des données par rapport à la granularité d’allocation, plus la taille des données que vous souhaitez examiner.

Supposons, par exemple, que la fonction [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) indique une granularité d’allocation de 64 Ko. Pour examiner 1 Ko de données de 138 240 octets (135K) dans le fichier, procédez comme suit :

1.  Créez un objet de mappage de fichier d’au moins 139 264 octets (136K) en taille.
2.  Créez une vue de fichier qui commence à un offset de fichier qui est le plus grand multiple de granularité d’allocation de fichier inférieur à l’offset dont vous avez besoin. Dans ce cas, l’affichage des fichiers commence à l’offset 131 072 (128K) dans le fichier. La taille de la vue est 139264 octets (136K) moins 131 072 octets (128 Ko) ou 8 192 octets (8 Ko).
3.  Créez un décalage de pointeur 7K dans la vue pour accéder à la valeur de 1 Ko qui vous intéresse.

Si les données que vous souhaitez chevauchent une limite de granularité d’allocation de fichiers, vous pouvez rendre la vue plus grande que la granularité d’allocation de fichier. Cela évite de scinder les données en parties.

Le programme suivant illustre le deuxième exemple ci-dessus.


```C++
/*
   This program demonstrates file mapping, especially how to align a
   view with the system file allocation granularity.
*/

#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define BUFFSIZE 1024 // size of the memory to examine at any one time

#define FILE_MAP_START 138240 // starting point within the file of
                              // the data to examine (135K)

/* The test file. The code below creates the file and populates it,
   so there is no need to supply it in advance. */

TCHAR * lpcTheFile = TEXT("fmtest.txt"); // the file to be manipulated

int main(void)
{
  HANDLE hMapFile;      // handle for the file's memory-mapped region
  HANDLE hFile;         // the file handle
  BOOL bFlag;           // a result holder
  DWORD dBytesWritten;  // number of bytes written
  DWORD dwFileSize;     // temporary storage for file sizes
  DWORD dwFileMapSize;  // size of the file mapping
  DWORD dwMapViewSize;  // the size of the view
  DWORD dwFileMapStart; // where to start the file map view
  DWORD dwSysGran;      // system allocation granularity
  SYSTEM_INFO SysInfo;  // system information; used to get granularity
  LPVOID lpMapAddress;  // pointer to the base address of the
                        // memory-mapped region
  char * pData;         // pointer to the data
  int i;                // loop counter
  int iData;            // on success contains the first int of data
  int iViewDelta;       // the offset into the view where the data
                        //shows up

  // Create the test file. Open it "Create Always" to overwrite any
  // existing file. The data is re-created below
  hFile = CreateFile(lpcTheFile,
                     GENERIC_READ | GENERIC_WRITE,
                     0,
                     NULL,
                     CREATE_ALWAYS,
                     FILE_ATTRIBUTE_NORMAL,
                     NULL);

  if (hFile == INVALID_HANDLE_VALUE)
  {
    _tprintf(TEXT("hFile is NULL\n"));
    _tprintf(TEXT("Target file is %s\n"),
             lpcTheFile);
    return 4;
  }

  // Get the system allocation granularity.
  GetSystemInfo(&SysInfo);
  dwSysGran = SysInfo.dwAllocationGranularity;

  // Now calculate a few variables. Calculate the file offsets as
  // 64-bit values, and then get the low-order 32 bits for the
  // function calls.

  // To calculate where to start the file mapping, round down the
  // offset of the data into the file to the nearest multiple of the
  // system allocation granularity.
  dwFileMapStart = (FILE_MAP_START / dwSysGran) * dwSysGran;
  _tprintf (TEXT("The file map view starts at %ld bytes into the file.\n"),
          dwFileMapStart);

  // Calculate the size of the file mapping view.
  dwMapViewSize = (FILE_MAP_START % dwSysGran) + BUFFSIZE;
  _tprintf (TEXT("The file map view is %ld bytes large.\n"),
            dwMapViewSize);

  // How large will the file mapping object be?
  dwFileMapSize = FILE_MAP_START + BUFFSIZE;
  _tprintf (TEXT("The file mapping object is %ld bytes large.\n"),
          dwFileMapSize);

  // The data of interest isn't at the beginning of the
  // view, so determine how far into the view to set the pointer.
  iViewDelta = FILE_MAP_START - dwFileMapStart;
  _tprintf (TEXT("The data is %d bytes into the view.\n"),
            iViewDelta);

  // Now write a file with data suitable for experimentation. This
  // provides unique int (4-byte) offsets in the file for easy visual
  // inspection. Note that this code does not check for storage
  // medium overflow or other errors, which production code should
  // do. Because an int is 4 bytes, the value at the pointer to the
  // data should be one quarter of the desired offset into the file

  for (i=0; i<(int)dwSysGran; i++)
  {
    WriteFile (hFile, &i, sizeof (i), &dBytesWritten, NULL);
  }

  // Verify that the correct file size was written.
  dwFileSize = GetFileSize(hFile,  NULL);
  _tprintf(TEXT("hFile size: %10d\n"), dwFileSize);

  // Create a file mapping object for the file
  // Note that it is a good idea to ensure the file size is not zero
  hMapFile = CreateFileMapping( hFile,          // current file handle
                NULL,           // default security
                PAGE_READWRITE, // read/write permission
                0,              // size of mapping object, high
                dwFileMapSize,  // size of mapping object, low
                NULL);          // name of mapping object

  if (hMapFile == NULL)
  {
    _tprintf(TEXT("hMapFile is NULL: last error: %d\n"), GetLastError() );
    return (2);
  }

  // Map the view and test the results.

  lpMapAddress = MapViewOfFile(hMapFile,            // handle to
                                                    // mapping object
                               FILE_MAP_ALL_ACCESS, // read/write
                               0,                   // high-order 32
                                                    // bits of file
                                                    // offset
                               dwFileMapStart,      // low-order 32
                                                    // bits of file
                                                    // offset
                               dwMapViewSize);      // number of bytes
                                                    // to map
  if (lpMapAddress == NULL)
  {
    _tprintf(TEXT("lpMapAddress is NULL: last error: %d\n"), GetLastError());
    return 3;
  }

  // Calculate the pointer to the data.
  pData = (char *) lpMapAddress + iViewDelta;

  // Extract the data, an int. Cast the pointer pData from a "pointer
  // to char" to a "pointer to int" to get the whole thing
  iData = *(int *)pData;

  _tprintf (TEXT("The value at the pointer is %d,\nwhich %s one quarter of the desired file offset.\n"),
            iData,
            iData*4 == FILE_MAP_START ? TEXT("is") : TEXT("is not"));

  // Close the file mapping object and the open file

  bFlag = UnmapViewOfFile(lpMapAddress);
  bFlag = CloseHandle(hMapFile); // close the file mapping object

  if(!bFlag)
  {
    _tprintf(TEXT("\nError %ld occurred closing the mapping object!"),
             GetLastError());
  }

  bFlag = CloseHandle(hFile);   // close the file itself

  if(!bFlag)
  {
    _tprintf(TEXT("\nError %ld occurred closing the file!"),
           GetLastError());
  }

  return 0;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’un affichage des fichiers](creating-a-file-view.md)
</dt> </dl>

 

 
