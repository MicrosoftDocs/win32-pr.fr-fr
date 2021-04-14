---
title: Détection de l’état de l’installation du programme d’installation de Windows Media
description: Détection de l’état de l’installation du programme d’installation de Windows Media
ms.assetid: c3acc268-934b-4a10-aab5-4b1764cb4c87
keywords:
- Lecteur Windows Media, détection de l’état de l’installation
- Lecteur Windows Media, état de l’installation
- Lecteur Windows Media, redistribution de logiciels
- Lecteur Windows Media, redistribution de logiciels
- détection de l’état de l’installation
- État de l’installation
- redistribution de logiciels
- redistribution de logiciels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28a4df9b842a1b6491a0ec98ca0a3182630c389
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380310"
---
# <a name="detecting-setup-status-for-windows-media-setup"></a><span data-ttu-id="72d36-111">Détection de l’état de l’installation du programme d’installation de Windows Media</span><span class="sxs-lookup"><span data-stu-id="72d36-111">Detecting Setup Status for Windows Media Setup</span></span>

<span data-ttu-id="72d36-112">Le code suivant peut être utilisé avec les packages de redistribution du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="72d36-112">The following code can be used with the Windows Media Player redistribution packages.</span></span> <span data-ttu-id="72d36-113">L’état de l’installation est stocké dans l’entrée de Registre **InstallResult** sous la sous-clé suivante :</span><span class="sxs-lookup"><span data-stu-id="72d36-113">The installation status is stored in the **InstallResult** registry entry under the following subkey:</span></span>

<span data-ttu-id="72d36-114">**HKEY \_ \_ logiciel utilisateur actuel- \\ \\ \\ \\ programme d’installation de Microsoft MediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="72d36-114">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Setup**</span></span>

<span data-ttu-id="72d36-115">L’entrée de Registre **InstallResult** se présente sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="72d36-115">The **InstallResult** registry entry has the following form.</span></span>



| <span data-ttu-id="72d36-116">Nom</span><span class="sxs-lookup"><span data-stu-id="72d36-116">Name</span></span>              | <span data-ttu-id="72d36-117">Type</span><span class="sxs-lookup"><span data-stu-id="72d36-117">Type</span></span>           | <span data-ttu-id="72d36-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="72d36-118">Value</span></span>                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72d36-119">**InstallResult**</span><span class="sxs-lookup"><span data-stu-id="72d36-119">**InstallResult**</span></span> | <span data-ttu-id="72d36-120">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="72d36-120">**REG\_DWORD**</span></span> | <span data-ttu-id="72d36-121">**HRESULT** qui indique si l’installation du lecteur Windows Media a réussi et si un redémarrage est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="72d36-121">An **HRESULT** that indicates whether Windows Media Player installation was successful and whether a restart is needed.</span></span> |



 

<span data-ttu-id="72d36-122">Voici un exemple de code C++ qui peut être incorporé dans une application d’installation appelante.</span><span class="sxs-lookup"><span data-stu-id="72d36-122">Here is example C++ code that could be incorporated into a calling setup application.</span></span> <span data-ttu-id="72d36-123">Ce code permet de définir `fSuccess` les `fRebootNeeded` variables et sur **true** ou **false**, selon le cas, en fonction de la valeur **HRESULT** écrite par le programme d’installation du lecteur Windows Media dans le package de redistribution des composants.</span><span class="sxs-lookup"><span data-stu-id="72d36-123">This code will set the `fSuccess` and `fRebootNeeded` variables to **true** or **false**, as appropriate, based on the **HRESULT** value written by Windows Media Player Setup in the component redistribution package.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
 
// If NS_S_REBOOT_REQUIRED is undefined, use 0xD2AF9.
#ifndef NS_S_REBOOT_REQUIRED
#define NS_S_REBOOT_REQUIRED       0xd2af9
#endif
 
int main( void )
{
    HKEY hKey = NULL;
    BOOL fSuccess = FALSE;
    BOOL fRebootNeeded = FALSE;
 
if( ERROR_SUCCESS == RegOpenKeyExA( 
                         HKEY_CURRENT_USER, 
                         "Software\\Microsoft\\MediaPlayer\\Setup", 
                         0, KEY_QUERY_VALUE, &hKey ))
    {
        char szResult[64];
        DWORD dwResult = sizeof( szResult );
 
if( ERROR_SUCCESS == RegQueryValueExA( 
                         hKey, "InstallResult", NULL, NULL, 
                         (LPBYTE)szResult, &dwResult ) )
        {
            sscanf_s( szResult, "%x", &dwResult );
            fSuccess = SUCCEEDED( dwResult );
            fRebootNeeded = ( NS_S_REBOOT_REQUIRED == dwResult );
        }
 
        RegCloseKey( hKey );
    }
 
    if( fSuccess )
    {
        printf( "Setup Succeeded..." );
        if( fRebootNeeded )
            printf( "A restart IS required...\n" );
        else
            printf( "A restart IS NOT required...\n" );
    }
    else
    {
        printf( "Setup Failed..." );
        if( fRebootNeeded )
            printf( "A restart IS required...\n" );
        else
            printf( "A restart IS NOT required...\n" );
    }
 
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="72d36-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="72d36-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72d36-125">**Redistribution du logiciel Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="72d36-125">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




