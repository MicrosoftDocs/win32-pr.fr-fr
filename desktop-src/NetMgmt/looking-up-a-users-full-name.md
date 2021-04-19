---
title: Recherche du nom complet d’un utilisateur
description: Les ordinateurs peuvent être organisés en un domaine, qui est un ensemble de réseaux d’ordinateurs. L’administrateur de domaine gère les informations de compte d’utilisateur et de groupe centralisées.
ms.assetid: 296ecfd0-1b65-482c-bee1-eff2130cc14e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2daa6bc2bc7d7255e961537c641a999d5a0bb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513467"
---
# <a name="looking-up-a-users-full-name"></a><span data-ttu-id="0e446-104">Recherche du nom complet d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="0e446-104">Looking Up a User's Full Name</span></span>

<span data-ttu-id="0e446-105">Les ordinateurs peuvent être organisés en un *domaine*, qui est un ensemble de réseaux d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="0e446-105">Computers can be organized into a *domain*, which is a collection of computers network.</span></span> <span data-ttu-id="0e446-106">L’administrateur de domaine gère les informations de compte d’utilisateur et de groupe centralisées.</span><span class="sxs-lookup"><span data-stu-id="0e446-106">The domain administrator maintains centralized user and group account information.</span></span>

<span data-ttu-id="0e446-107">Pour rechercher le nom complet d’un utilisateur, en fonction du nom d’utilisateur et du nom de domaine :</span><span class="sxs-lookup"><span data-stu-id="0e446-107">To find the full name of a user, given the user name and domain name:</span></span>

-   <span data-ttu-id="0e446-108">Convertit le nom d’utilisateur et le nom de domaine en Unicode, s’ils ne sont pas déjà des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="0e446-108">Convert the user name and domain name to Unicode, if they are not already Unicode strings.</span></span>
-   <span data-ttu-id="0e446-109">Recherchez le nom d’ordinateur du contrôleur de domaine en appelant [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname).</span><span class="sxs-lookup"><span data-stu-id="0e446-109">Look up the computer name of the domain controller (DC) by calling [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname).</span></span>
-   <span data-ttu-id="0e446-110">Recherchez le nom d’utilisateur sur l’ordinateur DC en appelant [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo).</span><span class="sxs-lookup"><span data-stu-id="0e446-110">Look up the user name on the DC computer by calling [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo).</span></span>
-   <span data-ttu-id="0e446-111">Convertit le nom d’utilisateur complet en ANSI, à moins que le programme ne s’attende à utiliser des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="0e446-111">Convert the full user name to ANSI, unless the program is expecting to work with Unicode strings.</span></span>

<span data-ttu-id="0e446-112">L’exemple de code suivant est une fonction (GetFullName) qui prend un nom d’utilisateur et un nom de domaine dans les deux premiers arguments et retourne le nom complet de l’utilisateur dans le troisième argument.</span><span class="sxs-lookup"><span data-stu-id="0e446-112">The following sample code is a function (GetFullName) that takes a user name and a domain name in the first two arguments and returns the user's full name in the third argument.</span></span>


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



 

 




