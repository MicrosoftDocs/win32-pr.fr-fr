---
description: Une application peut modifier le répertoire actif en appelant la fonction SetCurrentDirectory.
ms.assetid: b08e7739-55d4-4690-9ce5-2a8cb29214e9
title: Modification du répertoire actif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e507d206bcd988a7c00f557bde2b8a0ad39c79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522235"
---
# <a name="changing-the-current-directory"></a><span data-ttu-id="a682c-103">Modification du répertoire actif</span><span class="sxs-lookup"><span data-stu-id="a682c-103">Changing the Current Directory</span></span>

<span data-ttu-id="a682c-104">Le répertoire à la fin du chemin d’accès actif est appelé le répertoire actif. Il s’agit du répertoire dans lequel l’application active a démarré, sauf si elle a été modifiée explicitement.</span><span class="sxs-lookup"><span data-stu-id="a682c-104">The directory at the end of the active path is called the current directory; it is the directory in which the active application started, unless it has been explicitly changed.</span></span> <span data-ttu-id="a682c-105">Une application peut déterminer le répertoire actuel en appelant la fonction [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) .</span><span class="sxs-lookup"><span data-stu-id="a682c-105">An application can determine which directory is current by calling the [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) function.</span></span> <span data-ttu-id="a682c-106">Il est parfois nécessaire d’utiliser la fonction [**GetFullPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) pour vous assurer que la lettre de lecteur est incluse si l’application l’exige.</span><span class="sxs-lookup"><span data-stu-id="a682c-106">It is sometimes necessary to use the [**GetFullPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) function to ensure the drive letter is included if the application requires it.</span></span>

> [!Note]  
> <span data-ttu-id="a682c-107">Bien que chaque processus ne puisse avoir qu’un seul répertoire actif, si l’application change de volume à l’aide de la fonction [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) , le système mémorise le dernier chemin d’accès actuel pour chaque volume (lettre de lecteur).</span><span class="sxs-lookup"><span data-stu-id="a682c-107">Although each process can have only one current directory, if the application switches volumes by using the [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) function, the system remembers the last current path for each volume (drive letter).</span></span> <span data-ttu-id="a682c-108">Ce comportement se manifeste uniquement lors de la spécification d’une lettre de lecteur sans chemin d’accès complet lors de la modification du point de répertoire actif de référence à un autre volume.</span><span class="sxs-lookup"><span data-stu-id="a682c-108">This behavior will manifest itself only when specifying a drive letter without a fully qualified path when changing the current directory point of reference to a different volume.</span></span> <span data-ttu-id="a682c-109">Cela s’applique aux opérations d’extraction ou de définition.</span><span class="sxs-lookup"><span data-stu-id="a682c-109">This applies to either Get or Set operations.</span></span>

 

<span data-ttu-id="a682c-110">Une application peut modifier le répertoire actif en appelant la fonction [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) .</span><span class="sxs-lookup"><span data-stu-id="a682c-110">An application can change the current directory by calling the [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) function.</span></span>

<span data-ttu-id="a682c-111">L’exemple suivant illustre l’utilisation de [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) et [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory).</span><span class="sxs-lookup"><span data-stu-id="a682c-111">The following example demonstrates the use of [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) and [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory).</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <tchar.h>

#define BUFSIZE MAX_PATH
 
void _tmain(int argc, TCHAR **argv) 
{ 
   TCHAR Buffer[BUFSIZE];
   DWORD dwRet;

   if(argc != 2)
   {
      _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
      return;
   }

   dwRet = GetCurrentDirectory(BUFSIZE, Buffer);

   if( dwRet == 0 )
   {
      printf("GetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   if(dwRet > BUFSIZE)
   {
      printf("Buffer too small; need %d characters\n", dwRet);
      return;
   }

   if( !SetCurrentDirectory(argv[1]))
   {
      printf("SetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   _tprintf(TEXT("Set current directory to %s\n"), argv[1]);

   if( !SetCurrentDirectory(Buffer) )
   {
      printf("SetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   _tprintf(TEXT("Restored previous directory (%s)\n"), Buffer);
}
```



 

 



