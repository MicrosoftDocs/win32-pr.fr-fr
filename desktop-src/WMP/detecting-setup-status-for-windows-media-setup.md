---
title: détection de l’état de l’installation de Windows Media
description: détection de l’état de l’installation de Windows Media
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
ms.openlocfilehash: 797c7cb5fe4d34895109777c4da7e15489a0d32acd9cf42660b3346521f6f059
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340898"
---
# <a name="detecting-setup-status-for-windows-media-setup"></a>détection de l’état de l’installation de Windows Media

le code suivant peut être utilisé avec les packages de redistribution Lecteur Windows Media. L’état de l’installation est stocké dans l’entrée de Registre **InstallResult** sous la sous-clé suivante :

**HKEY \_ \_ logiciel utilisateur actuel- \\ \\ \\ \\ programme d’installation de Microsoft MediaPlayer**

L’entrée de Registre **InstallResult** se présente sous la forme suivante.



| Nom              | Type           | Valeur                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **InstallResult** | **\_valeur DWORD reg** | **HRESULT** qui indique si Lecteur Windows Media installation a réussi et si un redémarrage est nécessaire. |



 

Voici un exemple de code C++ qui peut être incorporé dans une application d’installation appelante. ce code définit les `fSuccess` variables et `fRebootNeeded` sur **true** ou **false**, selon le cas, en fonction de la valeur **HRESULT** écrite par Lecteur Windows Media programme d’installation dans le package de redistribution de composants.


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

[**redistribution du logiciel Lecteur Windows Media**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




