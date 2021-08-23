---
description: Exemple de code qui montre comment créer un fichier temporaire à des fins de manipulation de données à l’aide des fonctions GetTempFileName et GetTempPath.
ms.assetid: 6254c67d-5d34-499d-b1a4-8cac526dd294
title: Création et utilisation d’un fichier temporaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f242b9b021744c42e7e1b8745c7eec2b6388249246872192ecfd6308bdab55af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650419"
---
# <a name="creating-and-using-a-temporary-file"></a>Création et utilisation d’un fichier temporaire

Les applications peuvent obtenir des noms de fichier et de chemin d’accès uniques pour les fichiers temporaires à l’aide des fonctions [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) et [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) . La fonction **GetTempFileName** génère un nom de fichier unique et la fonction **GetTempPath** récupère le chemin d’accès à un répertoire dans lequel les fichiers temporaires doivent être créés.

La procédure suivante décrit comment une application crée un fichier temporaire à des fins de manipulation de données.

**Pour créer et utiliser un fichier temporaire**

1.  L’application ouvre le fichier texte source fourni par l’utilisateur à l’aide de [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).
2.  L’application récupère un chemin d’accès de fichier temporaire et un nom de fichier à l’aide des fonctions [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) et [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) , puis utilise [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) pour créer le fichier temporaire.
3.  L’application lit les blocs de données de texte dans une mémoire tampon, convertit le contenu de la mémoire tampon en majuscules à l’aide de la fonction [CharUpperBuffA](/windows/win32/api/winuser/nf-winuser-charupperbuffa) et écrit la mémoire tampon convertie dans le fichier temporaire.
4.  Lorsque tout le fichier source est écrit dans le fichier temporaire, l’application ferme les deux fichiers et renomme le fichier temporaire en « allcaps.txt » à l’aide de la fonction [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) .

La réussite de chacune des étapes précédentes est vérifiée avant de passer à l’étape suivante, et une description de l’échec s’affiche si une erreur se produit. L’application se termine immédiatement après l’affichage du message d’erreur.

Notez que la manipulation de fichiers texte a été choisie pour faciliter la démonstration et peut être remplacée par toute procédure de manipulation de données souhaitée. Le fichier de données peut être de n’importe quel type de données, et non uniquement du texte.

La fonction [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) récupère une chaîne de chemin complète à partir d’une variable d’environnement, mais ne vérifie pas à l’avance l’existence du chemin d’accès ou les droits d’accès appropriés à ce chemin, qui est la responsabilité du développeur de l’application. Pour plus d’informations, consultez [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha). Dans l’exemple suivant, une erreur est considérée comme une condition de terminal et l’application se ferme après l’envoi d’un message descriptif à la sortie standard. Toutefois, il existe de nombreuses autres options, telles que demander à l’utilisateur un répertoire temporaire ou simplement essayer d’utiliser le répertoire actif.

> [!Note]  
> La fonction [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) ne requiert pas l’utilisation de la fonction [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) .

 

L’exemple C++ suivant montre comment créer un fichier temporaire à des fins de manipulation de données.


```C++
//
//  This application opens a file specified by the user and uses
//  a temporary file to convert the file to upper case letters.
//  Note that the given source file is assumed to be an ASCII text file
//  and the new file created is overwritten each time the application is
//  run.
//

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE 1024

void PrintError(LPCTSTR errDesc);

int _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile     = INVALID_HANDLE_VALUE;
    HANDLE hTempFile = INVALID_HANDLE_VALUE; 

    BOOL fSuccess  = FALSE;
    DWORD dwRetVal = 0;
    UINT uRetVal   = 0;

    DWORD dwBytesRead    = 0;
    DWORD dwBytesWritten = 0; 

    TCHAR szTempFileName[MAX_PATH];  
    TCHAR lpTempPathBuffer[MAX_PATH];
    char  chBuffer[BUFSIZE]; 

    LPCTSTR errMsg;

    if(argc != 2)
    {
        _tprintf(TEXT("Usage: %s <file>\n"), argv[0]);
        return -1;
    }

    //  Opens the existing file. 
    hFile = CreateFile(argv[1],               // file name 
                       GENERIC_READ,          // open for reading 
                       0,                     // do not share 
                       NULL,                  // default security 
                       OPEN_EXISTING,         // existing file only 
                       FILE_ATTRIBUTE_NORMAL, // normal file 
                       NULL);                 // no template 
    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        PrintError(TEXT("First CreateFile failed"));
        return (1);
    } 

     //  Gets the temp path env string (no guarantee it's a valid path).
    dwRetVal = GetTempPath(MAX_PATH,          // length of the buffer
                           lpTempPathBuffer); // buffer for path 
    if (dwRetVal > MAX_PATH || (dwRetVal == 0))
    {
        PrintError(TEXT("GetTempPath failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (2);
    }

    //  Generates a temporary file name. 
    uRetVal = GetTempFileName(lpTempPathBuffer, // directory for tmp files
                              TEXT("DEMO"),     // temp file name prefix 
                              0,                // create unique name 
                              szTempFileName);  // buffer for name 
    if (uRetVal == 0)
    {
        PrintError(TEXT("GetTempFileName failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (3);
    }

    //  Creates the new file to write to for the upper-case version.
    hTempFile = CreateFile((LPTSTR) szTempFileName, // file name 
                           GENERIC_WRITE,        // open for write 
                           0,                    // do not share 
                           NULL,                 // default security 
                           CREATE_ALWAYS,        // overwrite existing
                           FILE_ATTRIBUTE_NORMAL,// normal file 
                           NULL);                // no template 
    if (hTempFile == INVALID_HANDLE_VALUE) 
    { 
        PrintError(TEXT("Second CreateFile failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (4);
    } 

    //  Reads BUFSIZE blocks to the buffer and converts all characters in 
    //  the buffer to upper case, then writes the buffer to the temporary 
    //  file. 
    do 
    {
        if (ReadFile(hFile, chBuffer, BUFSIZE, &dwBytesRead, NULL)) 
        {
            //  Replaces lower case letters with upper case
            //  in place (using the same buffer). The return
            //  value is the number of replacements performed,
            //  which we aren't interested in for this demo.
            CharUpperBuffA(chBuffer, dwBytesRead); 

            fSuccess = WriteFile(hTempFile, 
                                 chBuffer, 
                                 dwBytesRead,
                                 &dwBytesWritten, 
                                 NULL); 
            if (!fSuccess) 
            {
                PrintError(TEXT("WriteFile failed"));
                return (5);
            }
        } 
        else
        {
            PrintError(TEXT("ReadFile failed"));
            return (6);
        }
    //  Continues until the whole file is processed.
    } while (dwBytesRead == BUFSIZE); 

    //  The handles to the files are no longer needed, so
    //  they are closed prior to moving the new file.
    if (!CloseHandle(hFile)) 
    {
       PrintError(TEXT("CloseHandle(hFile) failed"));
       return (7);
    }
    
    if (!CloseHandle(hTempFile)) 
    {
       PrintError(TEXT("CloseHandle(hTempFile) failed"));
       return (8);
    }

    //  Moves the temporary file to the new text file, allowing for differnt
    //  drive letters or volume names.
    fSuccess = MoveFileEx(szTempFileName, 
                          TEXT("AllCaps.txt"), 
                          MOVEFILE_REPLACE_EXISTING | MOVEFILE_COPY_ALLOWED);
    if (!fSuccess)
    { 
        PrintError(TEXT("MoveFileEx failed"));
        return (9);
    }
    else 
        _tprintf(TEXT("All-caps version of %s written to AllCaps.txt\n"), argv[1]);
    return (0);
}

//  ErrorMessage support function.
//  Retrieves the system error message for the GetLastError() code.
//  Note: caller must use LocalFree() on the returned LPCTSTR buffer.
LPCTSTR ErrorMessage(DWORD error) 
{ 
    LPVOID lpMsgBuf;

    FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER 
                   | FORMAT_MESSAGE_FROM_SYSTEM 
                   | FORMAT_MESSAGE_IGNORE_INSERTS,
                  NULL,
                  error,
                  MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
                  (LPTSTR) &lpMsgBuf,
                  0,
                  NULL);

    return((LPCTSTR)lpMsgBuf);
}

//  PrintError support function.
//  Simple wrapper function for error output.
void PrintError(LPCTSTR errDesc)
{
        LPCTSTR errMsg = ErrorMessage(GetLastError());
        _tprintf(TEXT("\n** ERROR ** %s: %s\n"), errDesc, errMsg);
        LocalFree((LPVOID)errMsg);
}
```



 

 
