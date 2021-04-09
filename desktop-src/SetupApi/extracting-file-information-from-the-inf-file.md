---
description: Une fois le fichier INF ouvert, vous pouvez recueillir des informations à partir de celui-ci pour créer l’interface utilisateur ou pour diriger le processus d’installation. Les fonctions d’installation offrent plusieurs niveaux de fonctionnalités pour collecter des informations à partir d’un fichier INF.
ms.assetid: 3ef2768b-8c73-4258-937c-77a40963ffe4
title: Extraction d’informations de fichier à partir du fichier INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b404f44ca7d1d92fe0ce8eab08b73012ff144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862998"
---
# <a name="extracting-file-information-from-the-inf-file"></a>Extraction d’informations de fichier à partir du fichier INF

Une fois le fichier INF ouvert, vous pouvez recueillir des informations à partir de celui-ci pour créer l’interface utilisateur ou pour diriger le processus d’installation. Les fonctions d’installation offrent plusieurs niveaux de fonctionnalités pour collecter des informations à partir d’un fichier INF.



| Pour collecter des informations...                | Utilisez ces fonctions...                                                        |
|---------------------------------------|-----------------------------------------------------------------------------|
| À propos du fichier INF                    | [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                    |
|                                       | [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)        |
|                                       | [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa). |
| À propos des fichiers source et cible         | [**SetupGetSourceFileLocation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)            |
|                                       | [**SetupGetSourceFileSize**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                    |
|                                       | [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                            |
|                                       | [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                            |
| À partir d’une ligne d’un fichier INF            | [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                |
|                                       | [**SetupFindNextLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                              |
|                                       | [**SetupFindNextMatchLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                    |
|                                       | [**SetupGetLineByIndex**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                          |
|                                       | [**SetupFindFirstLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                            |
| À partir d’un champ d’une ligne dans un fichier INF | [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                          |
|                                       | [**SetupGetIntField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                |
|                                       | [**SetupGetBinaryField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                          |
|                                       | [**SetupGetMultiSzField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                        |



 

L’exemple suivant utilise la fonction [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) pour récupérer la description explicite d’un média source à partir d’un fichier INF.


```C++
#include <windows.h>
#include <setupapi.h>

BOOL test;  
HINF MyInf;
UINT SourceId;
PTSTR Buffer;
DWORD MaxBufSize;
DWORD BufSize;

int main()  
{ 

test = SetupGetSourceInfo (
     MyInf,   //Handle to the INF file to access                
     SourceId, //Id of the source media                 
     SRCINFO_DESCRIPTION, //which information to retrieve     
     Buffer, //a pointer to the buffer to receive the information                     
     MaxBufSize,  //the size allocated for the buffer 
     &BufSize    //buffer size actually needed
);
  
return 0;
}
```



Dans l’exemple, MyInf est le descripteur du fichier INF ouvert. SourceId est l’identificateur d’un média source spécifique. La valeur SRCINFO \_ Description spécifie que la fonction [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) doit récupérer la description du média source. La mémoire tampon pointe vers une chaîne qui reçoit la description, MaxBufSize indique les ressources allouées à la mémoire tampon, et BufSize indique les ressources nécessaires pour stocker la mémoire tampon.

Si BufSize est supérieur à MaxBufSize, la fonction retourne **false** et un appel suivant à [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur \_ mémoire tampon insuffisante \_ .

 

 
