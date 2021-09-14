---
description: Les fonctions d’heure incluses dans le runtime C utilisent le \_ type de temps t pour représenter le nombre de secondes écoulées depuis le 1er janvier 1970 à minuit. L’exemple suivant convertit une \_ valeur t Time t en une heure de fichier, à l’aide de la fonction Int32x32To64.
ms.assetid: f626c0b2-a5a1-475d-9a24-64e7b0407278
title: Conversion d’une valeur time_t en heure de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee866efaed716fb12d2501337236afdb7cf641b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008896"
---
# <a name="converting-a-time_t-value-to-a-file-time"></a>Conversion d’une \_ valeur de temps t en heure de fichier

Les fonctions d’heure incluses dans le runtime C utilisent le \_ type de temps t pour représenter le nombre de secondes écoulées depuis le 1er janvier 1970 à minuit. L’exemple suivant convertit une \_ valeur t Time t en une heure de fichier, à l’aide de la fonction [**Int32x32To64**](/windows/desktop/api/winnt/nf-winnt-int32x32to64) .


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



Une fois que vous avez obtenu une heure de fichier, vous pouvez convertir cette valeur en heure système à l’aide de la fonction [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) .

 

 
