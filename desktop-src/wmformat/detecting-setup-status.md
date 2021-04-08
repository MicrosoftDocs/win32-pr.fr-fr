---
title: Détection de l’état de l’installation
description: Détection de l’état de l’installation
ms.assetid: d502a5d6-798b-4269-aef3-1412fc379819
keywords:
- Windows Media Format SDK, redistribution de logiciels
- Format de systèmes avancés (ASF), redistribution de logiciels
- ASF (format des systèmes avancés), redistribution de logiciels
- Windows Media Format SDK, redistribution
- Format de systèmes avancés (ASF), redistribution
- ASF (format des systèmes avancés), redistribution
- redistribution de logiciels, détection de l’état de l’installation
- redistribution, détection de l’état de l’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6add696f2b2989de1e77d48504a1d540634213d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675678"
---
# <a name="detecting-setup-status"></a><span data-ttu-id="6be83-111">Détection de l’état de l’installation</span><span class="sxs-lookup"><span data-stu-id="6be83-111">Detecting Setup Status</span></span>

<span data-ttu-id="6be83-112">Lorsque l’exécutable de redistribution s’exécute sur un ordinateur, il enregistre son état d’installation dans le registre en tant que valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6be83-112">When the redistribution executable runs on a computer, it records its installation status in the registry as an **HRESULT** value.</span></span> <span data-ttu-id="6be83-113">L’état de l’installation est stocké dans l’entrée de Registre **InstallResult** sous la sous-clé suivante :</span><span class="sxs-lookup"><span data-stu-id="6be83-113">The installation status is stored in the **InstallResult** registry entry under the following subkey:</span></span>

<span data-ttu-id="6be83-114">**HKEY \_ \_ logiciel utilisateur actuel- \\ \\ \\ \\ programme d’installation de Microsoft MediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="6be83-114">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Setup**</span></span>

<span data-ttu-id="6be83-115">L’entrée de Registre **InstallResult** se présente sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="6be83-115">The **InstallResult** registry entry has the following form.</span></span>



| <span data-ttu-id="6be83-116">Nom</span><span class="sxs-lookup"><span data-stu-id="6be83-116">Name</span></span>              | <span data-ttu-id="6be83-117">Type</span><span class="sxs-lookup"><span data-stu-id="6be83-117">Type</span></span>           | <span data-ttu-id="6be83-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="6be83-118">Value</span></span>                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6be83-119">**InstallResult**</span><span class="sxs-lookup"><span data-stu-id="6be83-119">**InstallResult**</span></span> | <span data-ttu-id="6be83-120">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="6be83-120">**REG\_DWORD**</span></span> | <span data-ttu-id="6be83-121">**HRESULT** qui indique si l’installation du lecteur Windows Media a réussi et si un redémarrage est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6be83-121">An **HRESULT** that indicates whether Windows Media Player installation was successful and whether a restart is needed.</span></span> |



 

<span data-ttu-id="6be83-122">Le code suivant définit les variables *fSucess* et *fRebootNeeded* sur **true** ou **false**, selon le cas, en fonction de la valeur **HRESULT** écrite par le programme d’installation de Windows Media dans le package de redistribution des composants.</span><span class="sxs-lookup"><span data-stu-id="6be83-122">The following code will set the *fSucess* and *fRebootNeeded* variables to **True** or **False**, as appropriate, based on the **HRESULT** value written by Windows Media setup in the component redistribution package.</span></span>


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

    LONG lResult = RegOpenKeyEx( 
        HKEY_CURRENT_USER, 
        TEXT("Software\\Microsoft\\MediaPlayer\\Setup"), 
        0, 
        KEY_QUERY_VALUE, 
        &hKey 
        );

    if ( lResult == ERROR_SUCCESS )
    {
        DWORD dwRegType = 0;   // Registry value type.
        DWORD dwValue = 0;     // Registry value.
        DWORD cbValue = sizeof( dwValue );  // Size of the value in bytes.

        lResult = RegQueryValueEx( 
            hKey, 
            TEXT("InstallResult"), 
            NULL, 
            &dwRegType, 
            (LPBYTE)&dwValue, 
            &cbValue
            );

        if( lResult == ERROR_SUCCESS )
        {
            if (dwRegType == REG_DWORD)
            {
                fSuccess = SUCCEEDED( dwValue );
                fRebootNeeded = ( NS_S_REBOOT_REQUIRED == dwValue );
            }
        }

        RegCloseKey( hKey );
    }

    if( fSuccess )
    {
        printf( "Setup succeeded." );
    }
    else
    {
        printf( "Setup failed." );
    }

    if( fRebootNeeded )
    {
        printf( "A reboot IS required.\n" );
    }
    else
    {
        printf( "A reboot IS NOT required.\n" );
    }
 
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="6be83-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6be83-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6be83-124">**Redistribution de logiciels**</span><span class="sxs-lookup"><span data-stu-id="6be83-124">**Software Redistribution**</span></span>](software-redistribution.md)
</dt> </dl>

 

 




