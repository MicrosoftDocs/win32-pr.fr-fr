---
title: Utilisation des modules de gestion des couleurs (CMM)
description: Les modules de gestion des couleurs (CMMs) sont des modules de code WCS qui utilisent les informations des profils d’appareil pour effectuer la conversion des couleurs et le mappage des couleurs.
ms.assetid: df119e1a-b6f5-40a3-8852-8a57b21483d0
keywords:
- Système de couleurs Windows (WCS), module de gestion des couleurs (CMM)
- WCS (système de couleurs Windows), module de gestion des couleurs (CMM)
- gestion des couleurs des images, module de gestion des couleurs (CMM)
- gestion des couleurs, module de gestion des couleurs (CMM)
- couleurs, module de gestion des couleurs (CMM)
- Module de gestion des couleurs (CMM)
- CMM (module de gestion des couleurs)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b12a087bfc972ffcbd7f9fb083a9d73d669f134
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386898"
---
# <a name="using-color-management-modules-cmm"></a><span data-ttu-id="da1b2-110">Utilisation des modules de gestion des couleurs (CMM)</span><span class="sxs-lookup"><span data-stu-id="da1b2-110">Using Color Management Modules (CMM)</span></span>

<span data-ttu-id="da1b2-111">Les modules de gestion des couleurs (CMMs) sont des modules de code WCS qui utilisent les informations des profils d’appareil pour effectuer la conversion des couleurs et le mappage des couleurs.</span><span class="sxs-lookup"><span data-stu-id="da1b2-111">Color Management Modules (CMMs) are modules of WCS code that use the information in device profiles to perform color conversion and color mapping.</span></span> <span data-ttu-id="da1b2-112">Les développeurs d’applications ne doivent pas avoir à implémenter CMMs.</span><span class="sxs-lookup"><span data-stu-id="da1b2-112">Application developers should not have to implement CMMs.</span></span> <span data-ttu-id="da1b2-113">Microsoft fournit le CMM par défaut.</span><span class="sxs-lookup"><span data-stu-id="da1b2-113">Microsoft provides the default CMM.</span></span> <span data-ttu-id="da1b2-114">Toutefois, si vous écrivez un logiciel qui requiert l’utilisation de la conversion de couleurs spécialisée et des algorithmes de mappage des couleurs, vous pouvez en créer un.</span><span class="sxs-lookup"><span data-stu-id="da1b2-114">However, if you do write software that requires the use of specialized color conversion and color mapping algorithms, you may create one.</span></span>

> [!Note]  
> <span data-ttu-id="da1b2-115">Les points d’entrée CMM ne sont *pas* des fonctions API et ne doivent pas être appelés par les applications.</span><span class="sxs-lookup"><span data-stu-id="da1b2-115">CMM entry points are *not* API functions and should not be called by applications.</span></span>

 

<span data-ttu-id="da1b2-116">Lors de l’installation de CMMs, le programme d’installation les inscrit dans le Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="da1b2-116">When CMMs are installed, the installation program registers them in the Windows registry.</span></span> <span data-ttu-id="da1b2-117">Les applications peuvent énumérer le CMMs inscrit et en sélectionner un à l’aide de la fonction [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) .</span><span class="sxs-lookup"><span data-stu-id="da1b2-117">Applications can enumerate the registered CMMs and select one using the [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) function.</span></span> <span data-ttu-id="da1b2-118">L’exemple d’application suivant montre comment énumérer tous les CMMs inscrits.</span><span class="sxs-lookup"><span data-stu-id="da1b2-118">The following sample application demonstrates how to enumerate all registered CMMs.</span></span>


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



 

 




