---
description: Les fonctions d’heure incluses dans le runtime C utilisent le \_ type de temps t pour représenter le nombre de secondes écoulées depuis le 1er janvier 1970 à minuit. L’exemple suivant convertit une \_ valeur t Time t en une heure de fichier, à l’aide de la fonction Int32x32To64.
ms.assetid: f626c0b2-a5a1-475d-9a24-64e7b0407278
title: Conversion d’une valeur time_t en heure de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee866efaed716fb12d2501337236afdb7cf641b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532330"
---
# <a name="converting-a-time_t-value-to-a-file-time"></a><span data-ttu-id="4e942-104">Conversion d’une \_ valeur de temps t en heure de fichier</span><span class="sxs-lookup"><span data-stu-id="4e942-104">Converting a time\_t Value to a File Time</span></span>

<span data-ttu-id="4e942-105">Les fonctions d’heure incluses dans le runtime C utilisent le \_ type de temps t pour représenter le nombre de secondes écoulées depuis le 1er janvier 1970 à minuit.</span><span class="sxs-lookup"><span data-stu-id="4e942-105">The time functions included in the C run-time use the time\_t type to represent the number of seconds elapsed since midnight, January 1, 1970.</span></span> <span data-ttu-id="4e942-106">L’exemple suivant convertit une \_ valeur t Time t en une heure de fichier, à l’aide de la fonction [**Int32x32To64**](/windows/desktop/api/winnt/nf-winnt-int32x32to64) .</span><span class="sxs-lookup"><span data-stu-id="4e942-106">The following example converts a time\_t value to a file time, using the [**Int32x32To64**](/windows/desktop/api/winnt/nf-winnt-int32x32to64) function.</span></span>


```C++
#include <windows.h>
#include <time.h>

void TimetToFileTime( time_t t, LPFILETIME pft )
{
    LONGLONG ll = Int32x32To64(t, 10000000) + 116444736000000000;
    pft->dwLowDateTime = (DWORD) ll;
    pft->dwHighDateTime = ll >>32;
}
```



<span data-ttu-id="4e942-107">Une fois que vous avez obtenu une heure de fichier, vous pouvez convertir cette valeur en heure système à l’aide de la fonction [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) .</span><span class="sxs-lookup"><span data-stu-id="4e942-107">After you have obtained a file time, you can convert this value to system time using the [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) function.</span></span>

 

 
