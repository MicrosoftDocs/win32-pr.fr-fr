---
description: Exemple de code qui montre comment utiliser la fonction GetFileAttributesEx pour récupérer des attributs de fichier.
ms.assetid: f6eaea8a-0cc2-4fb6-bec5-7fb12b20c075
title: Récupération et modification des attributs de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c980ddd6390f016b2057392f42f6bf645859307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530168"
---
# <a name="retrieving-and-changing-file-attributes"></a><span data-ttu-id="251dc-103">Récupération et modification des attributs de fichier</span><span class="sxs-lookup"><span data-stu-id="251dc-103">Retrieving and Changing File Attributes</span></span>

<span data-ttu-id="251dc-104">Une application peut récupérer les attributs du fichier à l’aide de la fonction [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) ou [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) .</span><span class="sxs-lookup"><span data-stu-id="251dc-104">An application can retrieve the file attributes by using the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) or [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) function.</span></span> <span data-ttu-id="251dc-105">Les fonctions [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) et [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) peuvent définir un grand nombre d’attributs.</span><span class="sxs-lookup"><span data-stu-id="251dc-105">The [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) functions can set many of the attributes.</span></span> <span data-ttu-id="251dc-106">Toutefois, les applications ne peuvent pas définir tous les attributs.</span><span class="sxs-lookup"><span data-stu-id="251dc-106">However, applications cannot set all attributes.</span></span>

<span data-ttu-id="251dc-107">L’exemple de code de cette rubrique utilise la fonction [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) pour copier tous les fichiers texte (. txt) du répertoire actif dans un nouveau répertoire de fichiers en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="251dc-107">The code example in this topic uses the [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) function to copy all text files (.txt) in the current directory to a new directory of read-only files.</span></span> <span data-ttu-id="251dc-108">Le cas échéant, les fichiers du nouveau répertoire sont modifiés en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="251dc-108">Files in the new directory are changed to read only, if necessary.</span></span>

<span data-ttu-id="251dc-109">L’application crée le répertoire spécifié en tant que paramètre à l’aide de la fonction [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="251dc-109">The application creates the directory specified as a parameter by using the [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) function.</span></span> <span data-ttu-id="251dc-110">Le répertoire ne doit pas déjà exister.</span><span class="sxs-lookup"><span data-stu-id="251dc-110">The directory must not exist already.</span></span>

<span data-ttu-id="251dc-111">L’application recherche tous les fichiers texte dans le répertoire actif à l’aide des fonctions [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) et [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) .</span><span class="sxs-lookup"><span data-stu-id="251dc-111">The application searches the current directory for all text files by using the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) functions.</span></span> <span data-ttu-id="251dc-112">Chaque fichier texte est copié dans le \\ répertoire TextRO.</span><span class="sxs-lookup"><span data-stu-id="251dc-112">Each text file is copied to the \\TextRO directory.</span></span> <span data-ttu-id="251dc-113">Après la copie d’un fichier, la fonction [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) détermine si un fichier est en lecture seule ou non.</span><span class="sxs-lookup"><span data-stu-id="251dc-113">After a file is copied, the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function determines whether or not a file is read only.</span></span> <span data-ttu-id="251dc-114">Si le fichier n’est pas en lecture seule, l’application remplace les répertoires par \\ TextRO et convertit le fichier copié en lecture seule à l’aide de la fonction [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) .</span><span class="sxs-lookup"><span data-stu-id="251dc-114">If the file is not read only, the application changes directories to \\TextRO and converts the copied file to read only by using the [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) function.</span></span>

<span data-ttu-id="251dc-115">Une fois que tous les fichiers texte du répertoire actif sont copiés, l’application ferme le handle de recherche à l’aide de la fonction [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .</span><span class="sxs-lookup"><span data-stu-id="251dc-115">After all text files in the current directory are copied, the application closes the search handle by using the [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) function.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="251dc-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="251dc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="251dc-117">**Constantes d’attribut de fichier**</span><span class="sxs-lookup"><span data-stu-id="251dc-117">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> <dt>

[<span data-ttu-id="251dc-118">Noms de fichiers, chemins d’accès et espaces de noms</span><span class="sxs-lookup"><span data-stu-id="251dc-118">File Names, Paths, and Namespaces</span></span>](naming-a-file.md)
</dt> </dl>

 

 



