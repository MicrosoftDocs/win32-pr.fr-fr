---
title: Utilisation des modules de gestion des couleurs (CMM)
description: Les modules de gestion des couleurs (CMMs) sont des modules de code WCS qui utilisent les informations des profils d’appareil pour effectuer la conversion des couleurs et le mappage des couleurs.
ms.assetid: df119e1a-b6f5-40a3-8852-8a57b21483d0
keywords:
- Windows Système de couleurs (WCS), module de gestion des couleurs (CMM)
- WCS (Windows color System), Module de gestion des couleurs (CMM)
- gestion des couleurs des images, module de gestion des couleurs (CMM)
- gestion des couleurs, module de gestion des couleurs (CMM)
- couleurs, module de gestion des couleurs (CMM)
- Module de gestion des couleurs (CMM)
- CMM (module de gestion des couleurs)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 147c13a688942d46e400c2158c340fcea58d86616de042e9a44511861b67b802
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442349"
---
# <a name="using-color-management-modules-cmm"></a>Utilisation des modules de gestion des couleurs (CMM)

Les modules de gestion des couleurs (CMMs) sont des modules de code WCS qui utilisent les informations des profils d’appareil pour effectuer la conversion des couleurs et le mappage des couleurs. Les développeurs d’applications ne doivent pas avoir à implémenter CMMs. Microsoft fournit le CMM par défaut. Toutefois, si vous écrivez un logiciel qui requiert l’utilisation de la conversion de couleurs spécialisée et des algorithmes de mappage des couleurs, vous pouvez en créer un.

> [!Note]  
> Les points d’entrée CMM ne sont *pas* des fonctions API et ne doivent pas être appelés par les applications.

 

lors de l’installation de CMMs, le programme d’installation les inscrit dans le registre Windows. Les applications peuvent énumérer le CMMs inscrit et en sélectionner un à l’aide de la fonction [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) . L’exemple d’application suivant montre comment énumérer tous les CMMs inscrits.


```C++
#include <stdio.h>
#include <stdlib.h>
#include <stddef.h>
#include <string.h>
#include <mbstring.h>
#include <windows.h>
#include <icm.h>

#ifdef WINDOWS_98
TCHAR  gszICMatcher[] = __TEXT(
  "SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\ICM\\ICMatchers");
#else
TCHAR  gszICMatcher[] = __TEXT(
  "SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ICMatchers");
#endif

_CRTAPI1 main (int argc, char *argv[])
{
    DWORD dwNumCMM = 0;

    HANDLE hkCMM;
    DWORD dwErr = RegCreateKey(HKEY_LOCAL_MACHINE,
                 gszICMatcher, &hkCMM);
    DWORD dwMaxName, dwMaxValue;
    DWORD dwInfoErr = RegQueryInfoKey(&hkCMM, NULL, NULL,
                                NULL, NULL, NULL, NULL, NULL,
                                &dwMaxName, &dwMaxValue,
                                NULL, NULL);
    TCHAR chCMM[dwMaxName];
    ULONG cjCMM = sizeof(chCMM)/sizeof(chCMM[0]);
    DWORD dwType;
    TCHAR chCMMFile[dwMaxValue];
    ULONG cjCMMFile = sizeof(chCMMFile)/sizeof(chCMMFile[0]);

    if (dwErr != ERROR_SUCCESS)
    {
        printf("Could not open ICMatcher registry key: %d\n", dwErr);
    }

    if (dwErr == ERROR_SUCCESS)
    {
        while (RegEnumValue(
                   hkCMM,dwNumCMM,chCMM,
                   &cjCMM,NULL,&dwType,
                   chCMMFile,&cjCMMFile) == ERROR_SUCCESS)
        {
            if (dwType == REG_SZ)
            {
                printf("%d: %-80s - %-80s\n",dwNumCMM,chCMM,chCMMFile);
            }
            else
            {
                printf("%d: error\n");
            }

            dwNumCMM++;
            cjCMM = sizeof(chCMM);
            cjCMMFile = sizeof(chCMMFile);
        }
    }

    RegCloseKey(hkCMM);
}
```



 

 




