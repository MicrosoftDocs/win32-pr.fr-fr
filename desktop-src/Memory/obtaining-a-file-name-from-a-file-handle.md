---
description: GetFinalPathNameByHandle, introduite dans Windows Vista et Windows Server 2008, retourne un chemin d’accès à partir d’un handle.
ms.assetid: 359673bf-cc4c-4881-b946-ecdbef4a7ecb
title: Obtention d’un nom de fichier à partir d’un handle de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7d0c6fd8ea6839fdbfbe887f7a28b38571013b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094077"
---
# <a name="obtaining-a-file-name-from-a-file-handle"></a>Obtention d’un nom de fichier à partir d’un handle de fichier

[**GetFinalPathNameByHandle**](/windows/win32/api/fileapi/nf-fileapi-getfinalpathnamebyhandlea), introduite dans Windows Vista et Windows Server 2008, retourne un chemin d’accès à partir d’un handle. si vous avez besoin d’effectuer cette opération sur les versions antérieures de Windows, l’exemple suivant obtient un nom de fichier à partir d’un handle vers un objet fichier à l’aide d’un objet de mappage de fichier. Elle utilise les fonctions [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) et [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) pour créer le mappage. Ensuite, il utilise la fonction [**GetMappedFileName**](/windows/win32/api/psapi/nf-psapi-getmappedfilenamea) pour obtenir le nom de fichier. Pour les fichiers distants, il imprime le chemin d’accès de l’appareil reçu à partir de cette fonction. Pour les fichiers locaux, il convertit le chemin d’accès pour utiliser une lettre de lecteur et imprime ce chemin d’accès. Pour tester ce code, créez une fonction **principale** qui ouvre un fichier à l’aide de [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) et transmet le handle résultant à `GetFileNameFromHandle` .


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>
#include <string.h>
#include <psapi.h>
#include <strsafe.h>

#define BUFSIZE 512

BOOL GetFileNameFromHandle(HANDLE hFile) 
{
  BOOL bSuccess = FALSE;
  TCHAR pszFilename[MAX_PATH+1];
  HANDLE hFileMap;

  // Get the file size.
  DWORD dwFileSizeHi = 0;
  DWORD dwFileSizeLo = GetFileSize(hFile, &dwFileSizeHi); 

  if( dwFileSizeLo == 0 && dwFileSizeHi == 0 )
  {
     _tprintf(TEXT("Cannot map a file with a length of zero.\n"));
     return FALSE;
  }

  // Create a file mapping object.
  hFileMap = CreateFileMapping(hFile, 
                    NULL, 
                    PAGE_READONLY,
                    0, 
                    1,
                    NULL);

  if (hFileMap) 
  {
    // Create a file mapping to get the file name.
    void* pMem = MapViewOfFile(hFileMap, FILE_MAP_READ, 0, 0, 1);

    if (pMem) 
    {
      if (GetMappedFileName (GetCurrentProcess(), 
                             pMem, 
                             pszFilename,
                             MAX_PATH)) 
      {

        // Translate path with device name to drive letters.
        TCHAR szTemp[BUFSIZE];
        szTemp[0] = '\0';

        if (GetLogicalDriveStrings(BUFSIZE-1, szTemp)) 
        {
          TCHAR szName[MAX_PATH];
          TCHAR szDrive[3] = TEXT(" :");
          BOOL bFound = FALSE;
          TCHAR* p = szTemp;

          do 
          {
            // Copy the drive letter to the template string
            *szDrive = *p;

            // Look up each device name
            if (QueryDosDevice(szDrive, szName, MAX_PATH))
            {
              size_t uNameLen = _tcslen(szName);

              if (uNameLen < MAX_PATH) 
              {
                bFound = _tcsnicmp(pszFilename, szName, uNameLen) == 0
                         && *(pszFilename + uNameLen) == _T('\\');

                if (bFound) 
                {
                  // Reconstruct pszFilename using szTempFile
                  // Replace device path with DOS path
                  TCHAR szTempFile[MAX_PATH];
                  StringCchPrintf(szTempFile,
                            MAX_PATH,
                            TEXT("%s%s"),
                            szDrive,
                            pszFilename+uNameLen);
                  StringCchCopyN(pszFilename, MAX_PATH+1, szTempFile, _tcslen(szTempFile));
                }
              }
            }

            // Go to the next NULL character.
            while (*p++);
          } while (!bFound && *p); // end of string
        }
      }
      bSuccess = TRUE;
      UnmapViewOfFile(pMem);
    } 

    CloseHandle(hFileMap);
  }
  _tprintf(TEXT("File name is %s\n"), pszFilename);
  return(bSuccess);
}

int _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile;

    if( argc != 2 )
    {
        _tprintf(TEXT("This sample takes a file name as a parameter.\n"));
        return 0;
    }
    hFile = CreateFile(argv[1], GENERIC_READ, FILE_SHARE_READ, NULL,
        OPEN_EXISTING, 0, NULL);

    if(hFile == INVALID_HANDLE_VALUE)
    {
        _tprintf(TEXT("CreateFile failed with %d\n"), GetLastError());
        return 0;
    }
    GetFileNameFromHandle( hFile );
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du mappage de fichiers](using-file-mapping.md)
</dt> <dt>

[**GetFinalPathNameByHandle**](/windows/win32/api/fileapi/nf-fileapi-getfinalpathnamebyhandlea)
</dt> </dl>

 

 
