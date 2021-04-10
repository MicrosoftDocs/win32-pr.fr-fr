---
description: L’exemple suivant définit l’heure de dernière écriture d’un fichier à l’heure système actuelle à l’aide de la fonction SetFileTime.
ms.assetid: b4a70c01-d5ce-47e8-9918-9c9176894240
title: Modification de l’heure d’un fichier à l’heure actuelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3d4b6189514196c5f8a332c259da9f8f8d7417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953243"
---
# <a name="changing-a-file-time-to-the-current-time"></a>Modification de l’heure d’un fichier à l’heure actuelle

L’exemple suivant définit l’heure de dernière écriture d’un fichier à l’heure système actuelle à l’aide de la fonction [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime) .

Le système de fichiers NTFS stocke les valeurs d’heure au format UTC. elles ne sont donc pas affectées par les modifications apportées au fuseau horaire ou à l’heure d’été. Le système de fichiers FAT stocke les valeurs d’heure en fonction de l’heure locale de l’ordinateur.

Le fichier doit être ouvert avec la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) à l’aide des attributs d’écriture de fichier \_ \_ .


```C++
#include <windows.h>

// SetFileToCurrentTime - sets last write time to current system time
// Return value - TRUE if successful, FALSE otherwise
// hFile  - must be a valid file handle

BOOL SetFileToCurrentTime(HANDLE hFile)
{
    FILETIME ft;
    SYSTEMTIME st;
    BOOL f;

    GetSystemTime(&st);              // Gets the current system time
    SystemTimeToFileTime(&st, &ft);  // Converts the current system time to file time format
    f = SetFileTime(hFile,           // Sets last-write time of the file 
        (LPFILETIME) NULL,           // to the converted current system time 
        (LPFILETIME) NULL, 
        &ft);    

    return f;
}
```



 

 
