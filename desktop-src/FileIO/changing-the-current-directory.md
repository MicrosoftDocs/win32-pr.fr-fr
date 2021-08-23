---
description: Une application peut modifier le répertoire actif en appelant la fonction SetCurrentDirectory.
ms.assetid: b08e7739-55d4-4690-9ce5-2a8cb29214e9
title: Modification du répertoire actif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf742c872bab7d37e115afa815fff961d2f975bfbd3db75ff61a5e992d64a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632109"
---
# <a name="changing-the-current-directory"></a>Modification du répertoire actif

Le répertoire à la fin du chemin d’accès actif est appelé le répertoire actif. Il s’agit du répertoire dans lequel l’application active a démarré, sauf si elle a été modifiée explicitement. Une application peut déterminer le répertoire actuel en appelant la fonction [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) . Il est parfois nécessaire d’utiliser la fonction [**GetFullPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) pour vous assurer que la lettre de lecteur est incluse si l’application l’exige.

> [!Note]  
> Bien que chaque processus ne puisse avoir qu’un seul répertoire actif, si l’application change de volume à l’aide de la fonction [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) , le système mémorise le dernier chemin d’accès actuel pour chaque volume (lettre de lecteur). Ce comportement se manifeste uniquement lors de la spécification d’une lettre de lecteur sans chemin d’accès complet lors de la modification du point de répertoire actif de référence à un autre volume. Cela s’applique aux opérations d’extraction ou de définition.

 

Une application peut modifier le répertoire actif en appelant la fonction [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) .

L’exemple suivant illustre l’utilisation de [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) et [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory).


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



 

 



