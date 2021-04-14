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
# <a name="detecting-setup-status-for-windows-media-setup"></a>Détection de l’état de l’installation du programme d’installation de Windows Media

Le code suivant peut être utilisé avec les packages de redistribution du lecteur Windows Media. L’état de l’installation est stocké dans l’entrée de Registre **InstallResult** sous la sous-clé suivante :

**HKEY \_ \_ logiciel utilisateur actuel- \\ \\ \\ \\ programme d’installation de Microsoft MediaPlayer**

L’entrée de Registre **InstallResult** se présente sous la forme suivante.



| Nom              | Type           | Valeur                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **InstallResult** | **\_valeur DWORD reg** | **HRESULT** qui indique si l’installation du lecteur Windows Media a réussi et si un redémarrage est nécessaire. |



 

Voici un exemple de code C++ qui peut être incorporé dans une application d’installation appelante. Ce code permet de définir `fSuccess` les `fRebootNeeded` variables et sur **true** ou **false**, selon le cas, en fonction de la valeur **HRESULT** écrite par le programme d’installation du lecteur Windows Media dans le package de redistribution des composants.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Redistribution du logiciel Windows Media Player**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




