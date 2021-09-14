---
title: Forcer un utilisateur à modifier le mot de passe d’ouverture de session
description: Cet exemple de code montre comment forcer un utilisateur à modifier le mot de passe d’ouverture de session lors de la prochaine ouverture de session à l’aide des fonctions NetUserGetInfo et NetUserSetInfo et de la \_ structure User info \_ 3.
ms.assetid: 828f5d72-3e19-4b65-a1db-ac702fd4cfde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f3d0910f77c2553a55a53f1393aae5c9535982
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009413"
---
# <a name="forcing-a-user-to-change-the-logon-password"></a>Forcer un utilisateur à modifier le mot de passe d’ouverture de session

Cet exemple de code montre comment forcer un utilisateur à modifier le mot de passe d’ouverture de session lors de la prochaine ouverture de session à l’aide des fonctions [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) et [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) et de la structure [**User \_ info \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3) . notez qu’à partir de Windows XP, il est recommandé d’utiliser à la place la structure [**USER \_ INFO \_ 4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4) .

Affectez une valeur différente de zéro au membre **\_ \_ expiration du mot de passe usri3** de la structure **User \_ info \_ 3** à l’aide du fragment de code suivant :


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#define INCL_NET
#include <stdio.h>
#include <lm.h>

#pragma comment(lib, "netapi32.lib")

#define USERNAME L"your_user_name"
#define SERVER L"\\\\server"

void main( void )
{
    PUSER_INFO_3 pUsr = NULL;
    NET_API_STATUS netRet = 0;
    DWORD dwParmError = 0;
 //
 // First, retrieve the user information at level 3. This is 
 // necessary to prevent resetting other user information when 
 // the NetUserSetInfo call is made.
 //
   netRet = NetUserGetInfo( SERVER, USERNAME, 3, (LPBYTE *)&pUsr);

   if( netRet == NERR_Success )
   {
     //
     // The function was successful; set the usri3_password_expired value to 
     // a nonzero value. Call the NetUserSetInfo function.
     //
        pUsr->usri3_password_expired = TRUE;
        netRet = NetUserSetInfo( SERVER, USERNAME, 3, (LPBYTE)pUsr, &dwParmError);
    //
    // A zero return indicates success. 
    // If the return value is ERROR_INVALID_PARAMETER, 
    //  the dwParmError parameter will contain a value indicating the 
    //  invalid parameter within the user_info_3 structure. These values 
    //  are defined in the lmaccess.h file.
    //
        if( netRet == NERR_Success )
            printf("User %S will need to change password at next logon", USERNAME);
        else printf("Error %d occurred. Parm Error %d returned.\n", netRet, dwParmError);
    //
    // Must free the buffer returned by NetUserGetInfo.
    //
        NetApiBufferFree( pUsr);
    }
    else printf("NetUserGetInfo failed: %d\n", netRet);
}
```



 

 




