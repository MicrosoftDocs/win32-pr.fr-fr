---
title: Recherche du nom complet d’un utilisateur
description: Les ordinateurs peuvent être organisés en un domaine, qui est un ensemble de réseaux d’ordinateurs. L’administrateur de domaine gère les informations de compte d’utilisateur et de groupe centralisées.
ms.assetid: 296ecfd0-1b65-482c-bee1-eff2130cc14e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdff00483b38ef12355af4dcda4a48d60bf849a8fd5d6829640ae8907e426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012517"
---
# <a name="looking-up-a-users-full-name"></a>Recherche du nom complet d’un utilisateur

Les ordinateurs peuvent être organisés en un *domaine*, qui est un ensemble de réseaux d’ordinateurs. L’administrateur de domaine gère les informations de compte d’utilisateur et de groupe centralisées.

Pour rechercher le nom complet d’un utilisateur, en fonction du nom d’utilisateur et du nom de domaine :

-   Convertit le nom d’utilisateur et le nom de domaine en Unicode, s’ils ne sont pas déjà des chaînes Unicode.
-   Recherchez le nom d’ordinateur du contrôleur de domaine en appelant [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname).
-   Recherchez le nom d’utilisateur sur l’ordinateur DC en appelant [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo).
-   Convertit le nom d’utilisateur complet en ANSI, à moins que le programme ne s’attende à utiliser des chaînes Unicode.

L’exemple de code suivant est une fonction (GetFullName) qui prend un nom d’utilisateur et un nom de domaine dans les deux premiers arguments et retourne le nom complet de l’utilisateur dans le troisième argument.


```C++
#include <windows.h>
#include <lm.h>
#include <stdio.h>

#pragma comment(lib, "netapi32.lib")

BOOL GetFullName( char *UserName, char *Domain, char *dest )
{
    WCHAR wszUserName[UNLEN+1];          // Unicode user name
    WCHAR wszDomain[256]; 
    LPBYTE ComputerName;
    
//    struct _SERVER_INFO_100 *si100;  // Server structure
    struct _USER_INFO_2 *ui;         // User structure

// Convert ANSI user name and domain to Unicode

    MultiByteToWideChar( CP_ACP, 0, UserName,
        (int) strlen(UserName)+1, wszUserName, 
        sizeof(wszUserName)/sizeof(WCHAR) );

    MultiByteToWideChar( CP_ACP, 0, Domain,
        (int) strlen(Domain)+1, wszDomain, 
        sizeof(wszDomain)/sizeof(WCHAR) );

// Get the computer name of a DC for the domain.

    NetGetDCName( NULL, wszDomain, &ComputerName );

// Look up the user on the DC.

    if( NetUserGetInfo( (LPWSTR) ComputerName,
        (LPWSTR) &wszUserName, 2, (LPBYTE *) &ui ) )
    {
        wprintf( L"Error getting user information.\n" );
        return( FALSE );
    }

// Convert the Unicode full name to ANSI.

    WideCharToMultiByte( CP_ACP, 0, ui->usri2_full_name, -1,
        dest, 256, NULL, NULL );

    return (TRUE);
}
```



 

 




