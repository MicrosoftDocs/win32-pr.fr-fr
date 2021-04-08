---
description: Vérifiez les droits d’accès qu’un descripteur de sécurité autorise pour un client.
ms.assetid: de21968e-4590-4798-9152-43204d55521f
title: Vérification de l’accès client avec les ACL en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda629338d731d6e93f316fc15a6338c99bc1609
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866257"
---
# <a name="verifying-client-access-with-acls-in-c"></a><span data-ttu-id="bc469-103">Vérification de l’accès client avec les ACL en C++</span><span class="sxs-lookup"><span data-stu-id="bc469-103">Verifying Client Access with ACLs in C++</span></span>

<span data-ttu-id="bc469-104">L’exemple suivant montre comment un serveur peut vérifier les droits d’accès qu’un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) autorise pour un client.</span><span class="sxs-lookup"><span data-stu-id="bc469-104">The following example shows how a server could check the access rights that a [*security descriptor*](/windows/desktop/SecGloss/s-gly) allows for a client.</span></span> <span data-ttu-id="bc469-105">L’exemple utilise la fonction [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) ; Toutefois, elle fonctionnerait de la même façon en utilisant l’une des autres fonctions d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="bc469-105">The example uses the [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) function; however, it would work the same using any of the other impersonation functions.</span></span> <span data-ttu-id="bc469-106">Après avoir emprunté le client, l’exemple appelle la fonction [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) pour récupérer le [*jeton d’emprunt d’identité*](/windows/desktop/SecGloss/i-gly).</span><span class="sxs-lookup"><span data-stu-id="bc469-106">After impersonating the client, the example calls the [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) function to get the [*impersonation token*](/windows/desktop/SecGloss/i-gly).</span></span> <span data-ttu-id="bc469-107">Ensuite, il appelle la fonction [**MapGenericMask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) pour convertir tous les droits d’accès génériques en autorisations standard et spécifiques correspondantes selon le mappage spécifié dans la structure de [**\_ mappage générique**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) .</span><span class="sxs-lookup"><span data-stu-id="bc469-107">Then, it calls the [**MapGenericMask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) function to convert any generic access rights to the corresponding specific and standard rights according to the mapping specified in the [**GENERIC\_MAPPING**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) structure.</span></span>

<span data-ttu-id="bc469-108">La fonction [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) vérifie les droits d’accès demandés par rapport aux droits accordés au client dans la liste DACL du descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="bc469-108">The [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) function checks the requested access rights against the rights allowed for the client in the DACL of the security descriptor.</span></span> <span data-ttu-id="bc469-109">Pour vérifier l’accès et générer une entrée dans le journal des événements de sécurité, utilisez la fonction [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) .</span><span class="sxs-lookup"><span data-stu-id="bc469-109">To check access and generate an entry in the security event log, use the [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) function.</span></span>


```C++
#include <windows.h>
#pragma comment(lib, "advapi32.lib")

BOOL ImpersonateAndCheckAccess(
  HANDLE hNamedPipe,               // handle of pipe to impersonate
  PSECURITY_DESCRIPTOR pSD,        // security descriptor to check
  DWORD dwAccessDesired,           // access rights to check
  PGENERIC_MAPPING pGeneric,       // generic mapping for object
  PDWORD pdwAccessAllowed          // returns allowed access rights
) 
{
   HANDLE hToken;
   PRIVILEGE_SET PrivilegeSet;
   DWORD dwPrivSetSize = sizeof( PRIVILEGE_SET );
   BOOL fAccessGranted=FALSE;

// Impersonate the client.

   if (! ImpersonateNamedPipeClient(hNamedPipe) ) 
      return FALSE;

// Get an impersonation token with the client's security context.

   if (! OpenThreadToken( GetCurrentThread(), TOKEN_ALL_ACCESS,
         TRUE, &hToken ))
   {
      goto Cleanup;
   }

// Use the GENERIC_MAPPING structure to convert any 
// generic access rights to object-specific access rights.

   MapGenericMask( &dwAccessDesired, pGeneric );

// Check the client's access rights.

   if( !AccessCheck( 
      pSD,                 // security descriptor to check
      hToken,              // impersonation token
      dwAccessDesired,     // requested access rights
      pGeneric,            // pointer to GENERIC_MAPPING
      &PrivilegeSet,       // receives privileges used in check
      &dwPrivSetSize,      // size of PrivilegeSet buffer
      pdwAccessAllowed,    // receives mask of allowed access rights
      &fAccessGranted ))   // receives results of access check
   {
      goto Cleanup;
   }

Cleanup:

   RevertToSelf();

   if (hToken != INVALID_HANDLE_VALUE)
      CloseHandle(hToken);  

   return fAccessGranted;
}
```



 

 
