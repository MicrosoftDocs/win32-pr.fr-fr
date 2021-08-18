---
description: L’exemple suivant utilise les fonctions OpenProcessToken et GetTokenInformation pour récupérer les appartenances aux groupes dans un jeton d’accès.
ms.assetid: f895dfef-75ad-419c-95d0-6480bdf9c769
title: Recherche d’un SID dans un jeton d’accès en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942b3609064b51a299d4bd679b5cafe0e1f2b592298fe3a83cfb183ede959823
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911919"
---
# <a name="searching-for-a-sid-in-an-access-token-in-c"></a>Recherche d’un SID dans un jeton d’accès en C++

L’exemple suivant utilise les fonctions [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) et [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) pour récupérer les appartenances aux groupes dans un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly). Elle utilise ensuite la fonction [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) pour créer un SID qui identifie le SID connu du groupe administrateur pour l’ordinateur local. Ensuite, elle utilise la fonction [**EqualSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid) pour comparer le SID connu avec les SID de groupe du jeton d’accès. Si le SID est présent dans le jeton, la fonction vérifie les attributs du SID pour déterminer s’il est activé.

La fonction [**CheckTokenMembership**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-checktokenmembership) doit être utilisée pour déterminer si un SID spécifié est présent et activé dans un jeton d’accès. Cette fonction élimine les ininterprétations potentielles de l’appartenance au groupe actif.


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "advapi32.lib")

#define MAX_NAME 256

BOOL SearchTokenGroupsForSID (VOID) 
{
    DWORD i, dwSize = 0, dwResult = 0;
    HANDLE hToken;
    PTOKEN_GROUPS pGroupInfo;
    SID_NAME_USE SidType;
    char lpName[MAX_NAME];
    char lpDomain[MAX_NAME];
    PSID pSID = NULL;
    SID_IDENTIFIER_AUTHORITY SIDAuth = SECURITY_NT_AUTHORITY;
       
    // Open a handle to the access token for the calling process.

    if (!OpenProcessToken( GetCurrentProcess(), TOKEN_QUERY, &hToken )) 
    {
        printf( "OpenProcessToken Error %u\n", GetLastError() );
        return FALSE;
    }

    // Call GetTokenInformation to get the buffer size.

    if(!GetTokenInformation(hToken, TokenGroups, NULL, dwSize, &dwSize)) 
    {
        dwResult = GetLastError();
        if( dwResult != ERROR_INSUFFICIENT_BUFFER ) {
            printf( "GetTokenInformation Error %u\n", dwResult );
            return FALSE;
        }
    }

    // Allocate the buffer.

    pGroupInfo = (PTOKEN_GROUPS) GlobalAlloc( GPTR, dwSize );

    // Call GetTokenInformation again to get the group information.

    if(! GetTokenInformation(hToken, TokenGroups, pGroupInfo, 
                            dwSize, &dwSize ) ) 
    {
        printf( "GetTokenInformation Error %u\n", GetLastError() );
        return FALSE;
    }

    // Create a SID for the BUILTIN\Administrators group.

    if(! AllocateAndInitializeSid( &SIDAuth, 2,
                     SECURITY_BUILTIN_DOMAIN_RID,
                     DOMAIN_ALIAS_RID_ADMINS,
                     0, 0, 0, 0, 0, 0,
                     &pSID) ) 
    {
        printf( "AllocateAndInitializeSid Error %u\n", GetLastError() );
        return FALSE;
    }

    // Loop through the group SIDs looking for the administrator SID.

    for(i=0; i<pGroupInfo->GroupCount; i++) 
    {
        if ( EqualSid(pSID, pGroupInfo->Groups[i].Sid) ) 
        {

            // Lookup the account name and print it.

            dwSize = MAX_NAME;
            if( !LookupAccountSid( NULL, pGroupInfo->Groups[i].Sid,
                                  lpName, &dwSize, lpDomain, 
                                  &dwSize, &SidType ) ) 
            {
                dwResult = GetLastError();
                if( dwResult == ERROR_NONE_MAPPED )
                   strcpy_s (lpName, dwSize, "NONE_MAPPED" );
                else 
                {
                    printf("LookupAccountSid Error %u\n", GetLastError());
                    return FALSE;
                }
            }
            printf( "Current user is a member of the %s\\%s group\n", 
                    lpDomain, lpName );

            // Find out whether the SID is enabled in the token.
            if (pGroupInfo->Groups[i].Attributes & SE_GROUP_ENABLED)
                printf("The group SID is enabled.\n");
            else if (pGroupInfo->Groups[i].Attributes & 
                              SE_GROUP_USE_FOR_DENY_ONLY)
                printf("The group SID is a deny-only SID.\n");
            else 
                printf("The group SID is not enabled.\n");
        }
    }

    if (pSID)
        FreeSid(pSID);
    if ( pGroupInfo )
        GlobalFree( pGroupInfo );
    return TRUE;
}
```



 

 
