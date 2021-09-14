---
description: Exemple de code qui montre comment utiliser la fonction GetFileAttributesEx pour récupérer des attributs de fichier.
ms.assetid: f6eaea8a-0cc2-4fb6-bec5-7fb12b20c075
title: Récupération et modification des attributs de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c980ddd6390f016b2057392f42f6bf645859307
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009851"
---
# <a name="retrieving-and-changing-file-attributes"></a>Récupération et modification des attributs de fichier

Une application peut récupérer les attributs du fichier à l’aide de la fonction [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) ou [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) . Les fonctions [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) et [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) peuvent définir un grand nombre d’attributs. Toutefois, les applications ne peuvent pas définir tous les attributs.

L’exemple de code de cette rubrique utilise la fonction [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) pour copier tous les fichiers texte (.txt) du répertoire actif dans un nouveau répertoire de fichiers en lecture seule. Le cas échéant, les fichiers du nouveau répertoire sont modifiés en lecture seule.

L’application crée le répertoire spécifié en tant que paramètre à l’aide de la fonction [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) . Le répertoire ne doit pas déjà exister.

L’application recherche tous les fichiers texte dans le répertoire actif à l’aide des fonctions [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) et [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) . Chaque fichier texte est copié dans le \\ répertoire TextRO. Après la copie d’un fichier, la fonction [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) détermine si un fichier est en lecture seule ou non. Si le fichier n’est pas en lecture seule, l’application remplace les répertoires par \\ TextRO et convertit le fichier copié en lecture seule à l’aide de la fonction [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) .

Une fois que tous les fichiers texte du répertoire actif sont copiés, l’application ferme le handle de recherche à l’aide de la fonction [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

void _tmain(int argc, TCHAR* argv[])
{
   WIN32_FIND_DATA FileData;
   HANDLE          hSearch;
   DWORD           dwAttrs;
   TCHAR           szNewPath[MAX_PATH];   
 
   BOOL            fFinished = FALSE; 

   if(argc != 2)
   {
      _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
      return;
   }
 
// Create a new directory. 
 
   if (!CreateDirectory(argv[1], NULL)) 
   { 
      printf("CreateDirectory failed (%d)\n", GetLastError()); 
      return;
   } 
 
// Start searching for text files in the current directory. 
 
   hSearch = FindFirstFile(TEXT("*.txt"), &FileData); 
   if (hSearch == INVALID_HANDLE_VALUE) 
   { 
      printf("No text files found.\n"); 
      return;
   } 
 
// Copy each .TXT file to the new directory 
// and change it to read only, if not already. 
 
   while (!fFinished) 
   { 
      StringCchPrintf(szNewPath, sizeof(szNewPath)/sizeof(szNewPath[0]), TEXT("%s\\%s"), argv[1], FileData.cFileName);

      if (CopyFile(FileData.cFileName, szNewPath, FALSE))
      { 
         dwAttrs = GetFileAttributes(FileData.cFileName); 
         if (dwAttrs==INVALID_FILE_ATTRIBUTES) return; 

         if (!(dwAttrs & FILE_ATTRIBUTE_READONLY)) 
         { 
            SetFileAttributes(szNewPath, 
                dwAttrs | FILE_ATTRIBUTE_READONLY); 
         } 
      } 
      else 
      { 
         printf("Could not copy file.\n"); 
         return;
      } 
 
      if (!FindNextFile(hSearch, &FileData)) 
      {
         if (GetLastError() == ERROR_NO_MORE_FILES) 
         { 
            _tprintf(TEXT("Copied *.txt to %s\n"), argv[1]); 
            fFinished = TRUE; 
         } 
         else 
         { 
            printf("Could not find next file.\n"); 
            return;
         } 
      }
   } 
 
// Close the search handle. 
 
   FindClose(hSearch);
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Constantes d’attribut de fichier**](file-attribute-constants.md)
</dt> <dt>

[Noms de fichiers, chemins d’accès et espaces de noms](naming-a-file.md)
</dt> </dl>

 

 



