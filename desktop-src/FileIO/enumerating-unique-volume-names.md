---
description: Comment obtenir un chemin d’accès du GUID de volume pour chaque volume local associé à une lettre de lecteur en cours d’utilisation sur l’ordinateur.
ms.assetid: f6590a46-2e09-472c-8231-bb24c9b0b5f6
title: Énumération des chemins d’accès des GUID de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e363369d3ea26abb054c8b9321c0147ace7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529264"
---
# <a name="enumerating-volume-guid-paths"></a><span data-ttu-id="428cd-103">Énumération des chemins d’accès des GUID de volume</span><span class="sxs-lookup"><span data-stu-id="428cd-103">Enumerating Volume GUID Paths</span></span>

<span data-ttu-id="428cd-104">L’exemple de code de cette rubrique montre comment obtenir un chemin d’accès de **GUID** de volume pour chaque volume local associé à une lettre de lecteur en cours d’utilisation sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="428cd-104">The code example in this topic shows you how to obtain a volume **GUID** path for each local volume associated with a drive letter that is currently in use on the computer.</span></span>

<span data-ttu-id="428cd-105">L’exemple de code utilise la fonction [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .</span><span class="sxs-lookup"><span data-stu-id="428cd-105">The code example uses the [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) function.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define BUFSIZE MAX_PATH 

void main(void)
 {
  BOOL bFlag;
  TCHAR Buf[BUFSIZE];           // temporary buffer for volume name
  TCHAR Drive[] = TEXT("c:\\"); // template drive specifier
  TCHAR I;                      // generic loop counter

  // Walk through legal drive letters, skipping floppies.
  for (I = TEXT('c'); I < TEXT('z');  I++ ) 
   {
    // Stamp the drive for the appropriate letter.
    Drive[0] = I;

    bFlag = GetVolumeNameForVolumeMountPoint(
                Drive,     // input volume mount point or directory
                Buf,       // output volume name buffer
                BUFSIZE ); // size of volume name buffer

    if (bFlag) 
     {
      _tprintf (TEXT("The ID of drive \"%s\" is \"%s\"\n"), Drive, Buf);
     }
   }
 }
```



<span data-ttu-id="428cd-106">Pour obtenir un exemple qui énumère tous les volumes attachés localement et affiche le chemin d’accès de l’appareil, le chemin d’accès au **GUID** du volume et les chemins d’accès montés (y compris les lettres de lecteur), consultez [affichage des chemins de volume](displaying-volume-paths.md).</span><span class="sxs-lookup"><span data-stu-id="428cd-106">For an example that enumerates all locally attached volumes and displays the device path, volume **GUID** path, and mounted paths (including drive letters), see [Displaying Volume Paths](displaying-volume-paths.md).</span></span>

 

 



