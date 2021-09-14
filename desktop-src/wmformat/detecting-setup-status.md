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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226001"
---
# <a name="detecting-setup-status"></a>Détection de l’état de l’installation

Lorsque l’exécutable de redistribution s’exécute sur un ordinateur, il enregistre son état d’installation dans le registre en tant que valeur **HRESULT** . L’état de l’installation est stocké dans l’entrée de Registre **InstallResult** sous la sous-clé suivante :

**HKEY \_ \_ logiciel utilisateur actuel- \\ \\ \\ \\ programme d’installation de Microsoft MediaPlayer**

L’entrée de Registre **InstallResult** se présente sous la forme suivante.



| Nom              | Type           | Valeur                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **InstallResult** | **\_valeur DWORD reg** | **HRESULT** qui indique si Lecteur Windows Media installation a réussi et si un redémarrage est nécessaire. |



 

le code suivant définit les variables *fSucess* et *fRebootNeeded* sur **True** ou **false**, selon le cas, en fonction de la valeur **HRESULT** écrite par Windows configuration de média dans le package de redistribution de composants.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Redistribution de logiciels**](software-redistribution.md)
</dt> </dl>

 

 




