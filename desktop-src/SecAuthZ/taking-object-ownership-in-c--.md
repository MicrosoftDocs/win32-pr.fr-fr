---
description: L’exemple suivant tente de modifier la liste DACL d’un objet fichier en prenant possession de cet objet.
ms.assetid: 0b309ac9-177d-425f-8b78-71fe73e41979
title: Appropriation d’objets en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae43c28cb55193d43a15ed08f5905defded3dc2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516294"
---
# <a name="taking-object-ownership-in-c"></a><span data-ttu-id="388ad-103">Appropriation d’objets en C++</span><span class="sxs-lookup"><span data-stu-id="388ad-103">Taking Object Ownership in C++</span></span>

<span data-ttu-id="388ad-104">L’exemple suivant tente de modifier la liste DACL d’un objet fichier en prenant possession de cet objet.</span><span class="sxs-lookup"><span data-stu-id="388ad-104">The following example tries to change the DACL of a file object by taking ownership of that object.</span></span> <span data-ttu-id="388ad-105">Cela ne fonctionnera que si l’appelant dispose d’un \_ accès en écriture à l’objet DAC ou est le propriétaire de l’objet.</span><span class="sxs-lookup"><span data-stu-id="388ad-105">This will succeed only if the caller has WRITE\_DAC access to the object or is the owner of the object.</span></span> <span data-ttu-id="388ad-106">Si la tentative initiale de modification de la liste DACL échoue, un administrateur peut prendre possession de l’objet.</span><span class="sxs-lookup"><span data-stu-id="388ad-106">If the initial attempt to change the DACL fails, an administrator can take ownership of the object.</span></span> <span data-ttu-id="388ad-107">Pour accorder à l’administrateur la propriété, l’exemple active \_ le \_ privilège se prendre possession du \_ nom dans le [*jeton d’accès*](/windows/desktop/SecGloss/a-gly)de l’appelant, et fait du groupe administrateurs du système local le propriétaire de l’objet.</span><span class="sxs-lookup"><span data-stu-id="388ad-107">To give the administrator ownership, the example enables the SE\_TAKE\_OWNERSHIP\_NAME privilege in the caller's [*access token*](/windows/desktop/SecGloss/a-gly), and makes the local system's Administrators group the owner of the object.</span></span> <span data-ttu-id="388ad-108">Si l’appelant est membre du groupe administrateurs, le code sera en mesure de modifier la liste DACL de l’objet.</span><span class="sxs-lookup"><span data-stu-id="388ad-108">If the caller is a member of the Administrators group, the code will then be able to change the object's DACL.</span></span>

<span data-ttu-id="388ad-109">Pour activer et désactiver des privilèges, cet exemple utilise l’exemple de fonction SetPrivilege décrit dans [activation et désactivation des privilèges en C++](enabling-and-disabling-privileges-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="388ad-109">To enable and disable privileges, this example uses the SetPrivilege sample function described in [Enabling and Disabling Privileges in C++](enabling-and-disabling-privileges-in-c--.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <accctrl.h>
#include <aclapi.h>

//Forward declaration of SetPrivilege
BOOL SetPrivilege(
    HANDLE hToken,          // access token handle
    LPCTSTR lpszPrivilege,  // name of privilege to enable/disable
    BOOL bEnablePrivilege   // to enable or disable privilege
    ) ;


BOOL TakeOwnership(LPTSTR lpszOwnFile) 
{

    BOOL bRetval = FALSE;

    HANDLE hToken = NULL; 
    PSID pSIDAdmin = NULL;
    PSID pSIDEveryone = NULL;
    PACL pACL = NULL;
    SID_IDENTIFIER_AUTHORITY SIDAuthWorld =
            SECURITY_WORLD_SID_AUTHORITY;
    SID_IDENTIFIER_AUTHORITY SIDAuthNT = SECURITY_NT_AUTHORITY;
    const int NUM_ACES  = 2;
    EXPLICIT_ACCESS ea[NUM_ACES];
    DWORD dwRes;

    // Specify the DACL to use.
    // Create a SID for the Everyone group.
    if (!AllocateAndInitializeSid(&SIDAuthWorld, 1,
                     SECURITY_WORLD_RID,
                     0,
                     0, 0, 0, 0, 0, 0,
                     &pSIDEveryone)) 
    {
        printf("AllocateAndInitializeSid (Everyone) error %u\n",
                GetLastError());
        goto Cleanup;
    }

    // Create a SID for the BUILTIN\Administrators group.
    if (!AllocateAndInitializeSid(&SIDAuthNT, 2,
                     SECURITY_BUILTIN_DOMAIN_RID,
                     DOMAIN_ALIAS_RID_ADMINS,
                     0, 0, 0, 0, 0, 0,
                     &pSIDAdmin)) 
    {
        printf("AllocateAndInitializeSid (Admin) error %u\n",
                GetLastError());
        goto Cleanup;
    }

    ZeroMemory(&ea, NUM_ACES * sizeof(EXPLICIT_ACCESS));

    // Set read access for Everyone.
    ea[0].grfAccessPermissions = GENERIC_READ;
    ea[0].grfAccessMode = SET_ACCESS;
    ea[0].grfInheritance = NO_INHERITANCE;
    ea[0].Trustee.TrusteeForm = TRUSTEE_IS_SID;
    ea[0].Trustee.TrusteeType = TRUSTEE_IS_WELL_KNOWN_GROUP;
    ea[0].Trustee.ptstrName = (LPTSTR) pSIDEveryone;

    // Set full control for Administrators.
    ea[1].grfAccessPermissions = GENERIC_ALL;
    ea[1].grfAccessMode = SET_ACCESS;
    ea[1].grfInheritance = NO_INHERITANCE;
    ea[1].Trustee.TrusteeForm = TRUSTEE_IS_SID;
    ea[1].Trustee.TrusteeType = TRUSTEE_IS_GROUP;
    ea[1].Trustee.ptstrName = (LPTSTR) pSIDAdmin;

    if (ERROR_SUCCESS != SetEntriesInAcl(NUM_ACES,
                                         ea,
                                         NULL,
                                         &pACL))
    {
        printf("Failed SetEntriesInAcl\n");
        goto Cleanup;
    }

    // Try to modify the object's DACL.
    dwRes = SetNamedSecurityInfo(
        lpszOwnFile,                 // name of the object
        SE_FILE_OBJECT,              // type of object
        DACL_SECURITY_INFORMATION,   // change only the object's DACL
        NULL, NULL,                  // do not change owner or group
        pACL,                        // DACL specified
        NULL);                       // do not change SACL

    if (ERROR_SUCCESS == dwRes) 
    {
        printf("Successfully changed DACL\n");
        bRetval = TRUE;
        // No more processing needed.
        goto Cleanup;
    }
    if (dwRes != ERROR_ACCESS_DENIED)
    {
        printf("First SetNamedSecurityInfo call failed: %u\n",
                dwRes); 
        goto Cleanup;
    }

    // If the preceding call failed because access was denied, 
    // enable the SE_TAKE_OWNERSHIP_NAME privilege, create a SID for 
    // the Administrators group, take ownership of the object, and 
    // disable the privilege. Then try again to set the object's DACL.

    // Open a handle to the access token for the calling process.
    if (!OpenProcessToken(GetCurrentProcess(), 
                          TOKEN_ADJUST_PRIVILEGES, 
                          &hToken)) 
       {
          printf("OpenProcessToken failed: %u\n", GetLastError()); 
          goto Cleanup; 
       } 

    // Enable the SE_TAKE_OWNERSHIP_NAME privilege.
    if (!SetPrivilege(hToken, SE_TAKE_OWNERSHIP_NAME, TRUE)) 
    {
        printf("You must be logged on as Administrator.\n");
        goto Cleanup; 
    }

    // Set the owner in the object's security descriptor.
    dwRes = SetNamedSecurityInfo(
        lpszOwnFile,                 // name of the object
        SE_FILE_OBJECT,              // type of object
        OWNER_SECURITY_INFORMATION,  // change only the object's owner
        pSIDAdmin,                   // SID of Administrator group
        NULL,
        NULL,
        NULL); 

    if (dwRes != ERROR_SUCCESS) 
    {
        printf("Could not set owner. Error: %u\n", dwRes); 
        goto Cleanup;
    }
        
    // Disable the SE_TAKE_OWNERSHIP_NAME privilege.
    if (!SetPrivilege(hToken, SE_TAKE_OWNERSHIP_NAME, FALSE)) 
    {
        printf("Failed SetPrivilege call unexpectedly.\n");
        goto Cleanup;
    }

    // Try again to modify the object's DACL,
    // now that we are the owner.
    dwRes = SetNamedSecurityInfo(
        lpszOwnFile,                 // name of the object
        SE_FILE_OBJECT,              // type of object
        DACL_SECURITY_INFORMATION,   // change only the object's DACL
        NULL, NULL,                  // do not change owner or group
        pACL,                        // DACL specified
        NULL);                       // do not change SACL

    if (dwRes == ERROR_SUCCESS)
    {
        printf("Successfully changed DACL\n");
        bRetval = TRUE; 
    }
    else
    {
        printf("Second SetNamedSecurityInfo call failed: %u\n",
                dwRes); 
    }

Cleanup:

    if (pSIDAdmin)
        FreeSid(pSIDAdmin); 

    if (pSIDEveryone)
        FreeSid(pSIDEveryone); 

    if (pACL)
       LocalFree(pACL);

    if (hToken)
       CloseHandle(hToken);

    return bRetval;

}
```



 

 
