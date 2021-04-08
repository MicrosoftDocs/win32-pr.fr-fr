---
description: Exemple de code qui montre comment utiliser la fonction CreateFile pour créer un nouveau fichier ou ouvrir un fichier existant.
ms.assetid: 04e089a7-c559-4a35-a38b-e1acdf3438d1
title: Ouverture d’un fichier pour la lecture ou l’écriture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a254684538a64a37cd94841812df84808da8374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752821"
---
# <a name="opening-a-file-for-reading-or-writing"></a>Ouverture d’un fichier pour la lecture ou l’écriture

La fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) peut créer un nouveau fichier ou ouvrir un fichier existant. Vous devez spécifier le nom de fichier, les instructions de création et d’autres attributs. Lorsqu’une application crée un nouveau fichier, le système d’exploitation l’ajoute au répertoire spécifié.

## <a name="example-open-a-file-for-writing"></a>Exemple : ouvrir un fichier en écriture

L’exemple suivant utilise [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) pour créer un nouveau fichier et l’ouvrir pour écrire et [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) pour écrire une chaîne simple de façon synchrone dans le fichier.

Un appel ultérieur à l’ouverture de ce fichier avec [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) échouera jusqu’à la fermeture du descripteur.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

void DisplayError(LPTSTR lpszFunction);

int __cdecl _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile; 
    char DataBuffer[] = "This is some test data to write to the file.";
    DWORD dwBytesToWrite = (DWORD)strlen(DataBuffer);
    DWORD dwBytesWritten = 0;
    BOOL bErrorFlag = FALSE;

    printf("\n");
    if( argc != 2 )
    {
        printf("Usage Error:\tIncorrect number of arguments\n\n");
        _tprintf(TEXT("%s <file_name>\n"), argv[0]);
        return;
    }

    hFile = CreateFile(argv[1],                // name of the write
                       GENERIC_WRITE,          // open for writing
                       0,                      // do not share
                       NULL,                   // default security
                       CREATE_NEW,             // create new file only
                       FILE_ATTRIBUTE_NORMAL,  // normal file
                       NULL);                  // no attr. template

    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        DisplayError(TEXT("CreateFile"));
        _tprintf(TEXT("Terminal failure: Unable to open file \"%s\" for write.\n"), argv[1]);
        return;
    }

    _tprintf(TEXT("Writing %d bytes to %s.\n"), dwBytesToWrite, argv[1]);

    bErrorFlag = WriteFile( 
                    hFile,           // open file handle
                    DataBuffer,      // start of data to write
                    dwBytesToWrite,  // number of bytes to write
                    &dwBytesWritten, // number of bytes that were written
                    NULL);            // no overlapped structure

    if (FALSE == bErrorFlag)
    {
        DisplayError(TEXT("WriteFile"));
        printf("Terminal failure: Unable to write to file.\n");
    }
    else
    {
        if (dwBytesWritten != dwBytesToWrite)
        {
            // This is an error because a synchronous write that results in
            // success (WriteFile returns TRUE) should write all data as
            // requested. This would not necessarily be the case for
            // asynchronous writes.
            printf("Error: dwBytesWritten != dwBytesToWrite\n");
        }
        else
        {
            _tprintf(TEXT("Wrote %d bytes to %s successfully.\n"), dwBytesWritten, argv[1]);
        }
    }

    CloseHandle(hFile);
}

void DisplayError(LPTSTR lpszFunction) 
// Routine Description:
// Retrieve and output the system error message for the last-error code
{ 
    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, 
        NULL );

    lpDisplayBuf = 
        (LPVOID)LocalAlloc( LMEM_ZEROINIT, 
                            ( lstrlen((LPCTSTR)lpMsgBuf)
                              + lstrlen((LPCTSTR)lpszFunction)
                              + 40) // account for format string
                            * sizeof(TCHAR) );
    
    if (FAILED( StringCchPrintf((LPTSTR)lpDisplayBuf, 
                     LocalSize(lpDisplayBuf) / sizeof(TCHAR),
                     TEXT("%s failed with error code %d as follows:\n%s"), 
                     lpszFunction, 
                     dw, 
                     lpMsgBuf)))
    {
        printf("FATAL ERROR: Unable to output error code.\n");
    }
    
    _tprintf(TEXT("ERROR: %s\n"), (LPCTSTR)lpDisplayBuf);

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
```



## <a name="example-open-a-file-for-reading"></a>Exemple : ouvrir un fichier en lecture

L’exemple suivant utilise [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) pour ouvrir un fichier existant afin de lire et [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) pour lire jusqu’à 80 caractères de façon synchrone à partir du fichier.

Dans ce cas, [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ne fonctionne que si le fichier spécifié existe déjà dans le répertoire actif. Un appel ultérieur à l’ouverture de ce fichier avec **CreateFile** échoue si l’appel utilise les mêmes modes d’accès et de partage.

Conseil : vous pouvez utiliser le fichier que vous avez créé avec l’exemple WriteFile précédent pour tester cet exemple.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

#define BUFFERSIZE 5
DWORD g_BytesTransferred = 0;

void DisplayError(LPTSTR lpszFunction);

VOID CALLBACK FileIOCompletionRoutine(
  __in  DWORD dwErrorCode,
  __in  DWORD dwNumberOfBytesTransfered,
  __in  LPOVERLAPPED lpOverlapped
);

VOID CALLBACK FileIOCompletionRoutine(
  __in  DWORD dwErrorCode,
  __in  DWORD dwNumberOfBytesTransfered,
  __in  LPOVERLAPPED lpOverlapped )
 {
  _tprintf(TEXT("Error code:\t%x\n"), dwErrorCode);
  _tprintf(TEXT("Number of bytes:\t%x\n"), dwNumberOfBytesTransfered);
  g_BytesTransferred = dwNumberOfBytesTransfered;
 }

//
// Note: this simplified sample assumes the file to read is an ANSI text file
// only for the purposes of output to the screen. CreateFile and ReadFile
// do not use parameters to differentiate between text and binary file types.
//

int __cdecl _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile; 
    DWORD  dwBytesRead = 0;
    char   ReadBuffer[BUFFERSIZE] = {0};
    OVERLAPPED ol = {0};

    printf("\n");
    if( argc != 2 )
    {
        printf("Usage Error: Incorrect number of arguments\n\n");
        _tprintf(TEXT("Usage:\n\t%s <text_file_name>\n"), argv[0]);
        return;
    }

    hFile = CreateFile(argv[1],               // file to open
                       GENERIC_READ,          // open for reading
                       FILE_SHARE_READ,       // share for reading
                       NULL,                  // default security
                       OPEN_EXISTING,         // existing file only
                       FILE_ATTRIBUTE_NORMAL | FILE_FLAG_OVERLAPPED, // normal file
                       NULL);                 // no attr. template
 
    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        DisplayError(TEXT("CreateFile"));
        _tprintf(TEXT("Terminal failure: unable to open file \"%s\" for read.\n"), argv[1]);
        return; 
    }

    // Read one character less than the buffer size to save room for
    // the terminating NULL character. 

    if( FALSE == ReadFileEx(hFile, ReadBuffer, BUFFERSIZE-1, &ol, FileIOCompletionRoutine) )
    {
        DisplayError(TEXT("ReadFile"));
        printf("Terminal failure: Unable to read from file.\n GetLastError=%08x\n", GetLastError());
        CloseHandle(hFile);
        return;
    }
    SleepEx(5000, TRUE);
    dwBytesRead = g_BytesTransferred;
    // This is the section of code that assumes the file is ANSI text. 
    // Modify this block for other data types if needed.

    if (dwBytesRead > 0 && dwBytesRead <= BUFFERSIZE-1)
    {
        ReadBuffer[dwBytesRead]='\0'; // NULL character

        _tprintf(TEXT("Data read from %s (%d bytes): \n"), argv[1], dwBytesRead);
        printf("%s\n", ReadBuffer);
    }
    else if (dwBytesRead == 0)
    {
        _tprintf(TEXT("No data read from file %s\n"), argv[1]);
    }
    else
    {
        printf("\n ** Unexpected value for dwBytesRead ** \n");
    }

    // It is always good practice to close the open file handles even though
    // the app will exit here and clean up open handles anyway.
    
    CloseHandle(hFile);
}

void DisplayError(LPTSTR lpszFunction) 
// Routine Description:
// Retrieve and output the system error message for the last-error code
{ 
    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, 
        NULL );

    lpDisplayBuf = 
        (LPVOID)LocalAlloc( LMEM_ZEROINIT, 
                            ( lstrlen((LPCTSTR)lpMsgBuf)
                              + lstrlen((LPCTSTR)lpszFunction)
                              + 40) // account for format string
                            * sizeof(TCHAR) );
    
    if (FAILED( StringCchPrintf((LPTSTR)lpDisplayBuf, 
                     LocalSize(lpDisplayBuf) / sizeof(TCHAR),
                     TEXT("%s failed with error code %d as follows:\n%s"), 
                     lpszFunction, 
                     dw, 
                     lpMsgBuf)))
    {
        printf("FATAL ERROR: Unable to output error code.\n");
    }
    
    _tprintf(TEXT("ERROR: %s\n"), (LPCTSTR)lpDisplayBuf);

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création et ouverture de fichiers](creating-and-opening-files.md)
</dt> </dl>

 

 



