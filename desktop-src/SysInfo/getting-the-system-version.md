---
description: L’exemple suivant utilise les fonctions d’assistance de l’API de version pour déterminer la version du système d’exploitation actuel, s’il s’agit d’une version serveur ou client, puis affiche ces informations dans la console.
ms.assetid: ae851aef-27d5-4eb7-aeb2-ccdfbf040e5a
title: Obtention de la version du système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0fa259378b81f9255846694927ee2b68e6f38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869210"
---
# <a name="getting-the-system-version"></a><span data-ttu-id="0e00f-103">Obtention de la version du système</span><span class="sxs-lookup"><span data-stu-id="0e00f-103">Getting the System Version</span></span>

<span data-ttu-id="0e00f-104">L’exemple suivant utilise les [fonctions d’assistance](version-helper-apis.md) de l’API de version pour déterminer la version du système d’exploitation actuel, s’il s’agit d’une version serveur ou client, puis affiche ces informations dans la console.</span><span class="sxs-lookup"><span data-stu-id="0e00f-104">The following example uses the [Version API Helper functions](version-helper-apis.md) to determine the version of the current operating system, if it is a Server or Client release, and then displays this information to the console.</span></span> <span data-ttu-id="0e00f-105">Si le mode de compatibilité est activé, l’exemple affiche le système d’exploitation sélectionné pour la [compatibilité des applications](/previous-versions/bb757005(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="0e00f-105">If compatibility mode is in effect, the example displays the operating system selected for [application compatibility](/previous-versions/bb757005(v=msdn.10)).</span></span>

<span data-ttu-id="0e00f-106">Le fait de compter sur les informations de version n’est pas la meilleure façon de tester une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="0e00f-106">Relying on version information is not the best way to test for a feature.</span></span> <span data-ttu-id="0e00f-107">Au lieu de cela, reportez-vous à la documentation de la fonctionnalité qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="0e00f-107">Instead, refer to the documentation for the feature of interest.</span></span> <span data-ttu-id="0e00f-108">Pour plus d’informations sur les techniques courantes de détection des fonctionnalités, consultez [version du système d’exploitation](operating-system-version.md).</span><span class="sxs-lookup"><span data-stu-id="0e00f-108">For more information on common techniques for feature detection, see [Operating System Version](operating-system-version.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <VersionHelpers.h>

int 
__cdecl
wmain(
    __in int argc, 
    __in_ecount(argc) PCWSTR argv[]
    )
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);

    if (IsWindowsXPOrGreater())
    {
        printf("XPOrGreater\n");
    }

    if (IsWindowsXPSP1OrGreater())
    {
        printf("XPSP1OrGreater\n");
    }

    if (IsWindowsXPSP2OrGreater())
    {
        printf("XPSP2OrGreater\n");
    }

    if (IsWindowsXPSP3OrGreater())
    {
        printf("XPSP3OrGreater\n");
    }

    if (IsWindowsVistaOrGreater())
    {
        printf("VistaOrGreater\n");
    }

    if (IsWindowsVistaSP1OrGreater())
    {
        printf("VistaSP1OrGreater\n");
    }

    if (IsWindowsVistaSP2OrGreater())
    {
        printf("VistaSP2OrGreater\n");
    }

    if (IsWindows7OrGreater())
    {
        printf("Windows7OrGreater\n");
    }

    if (IsWindows7SP1OrGreater())
    {
        printf("Windows7SP1OrGreater\n");
    }

    if (IsWindows8OrGreater())
    {
        printf("Windows8OrGreater\n");
    }

    if (IsWindows8Point1OrGreater())
    {
        printf("Windows8Point1OrGreater\n");
    }

    if (IsWindows10OrGreater())
    {
        printf("Windows10OrGreater\n");
    }

    if (IsWindowsServer())
    {
        printf("Server\n");
    }
    else
    {
        printf("Client\n");
    }
}
```



 

 
