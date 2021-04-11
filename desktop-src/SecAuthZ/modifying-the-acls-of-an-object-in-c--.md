---
description: L’exemple suivant ajoute une entrée de contrôle d’accès (ACE) à la liste de contrôle d’accès discrétionnaire (DACL) d’un objet.
ms.assetid: 0c168bb7-996f-42a8-96cd-2ba7870a3333
title: Modification des listes de contrôle d’accès d’un objet en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21195b1164ce949d1305f0c1748d24b0dbb7525b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952784"
---
# <a name="modifying-the-acls-of-an-object-in-c"></a><span data-ttu-id="2999b-103">Modification des listes de contrôle d’accès d’un objet en C++</span><span class="sxs-lookup"><span data-stu-id="2999b-103">Modifying the ACLs of an Object in C++</span></span>

<span data-ttu-id="2999b-104">L’exemple suivant ajoute une [*entrée de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) à la [*liste de contrôle d’accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) d’un objet.</span><span class="sxs-lookup"><span data-stu-id="2999b-104">The following example adds an [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) to the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of an object.</span></span>

<span data-ttu-id="2999b-105">Le paramètre *AccessMode* détermine le type de nouvelle entrée du contrôle d’accès et la façon dont la nouvelle entrée du contrôle d’accès est combinée avec les entrées de contrôle d’accès existantes pour le tiers de confiance spécifié.</span><span class="sxs-lookup"><span data-stu-id="2999b-105">The *AccessMode* parameter determines the type of new ACE and how the new ACE is combined with any existing ACEs for the specified trustee.</span></span> <span data-ttu-id="2999b-106">Utilisez les indicateurs accorder l’accès \_ , définir \_ l’accès, refuser \_ l’accès ou révoquer l’accès \_ dans le paramètre *AccessMode* .</span><span class="sxs-lookup"><span data-stu-id="2999b-106">Use the GRANT\_ACCESS, SET\_ACCESS, DENY\_ACCESS, or REVOKE\_ACCESS flags in the *AccessMode* parameter.</span></span> <span data-ttu-id="2999b-107">Pour plus d’informations sur ces indicateurs, consultez [**\_ mode d’accès**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span><span class="sxs-lookup"><span data-stu-id="2999b-107">For information about these flags, see [**ACCESS\_MODE**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span></span>

<span data-ttu-id="2999b-108">Vous pouvez utiliser du code similaire pour utiliser une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="2999b-108">Similar code can be used to work with a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="2999b-109">Spécifiez \_ les \_ informations de sécurité SACL dans les fonctions [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) et [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) pour obtenir et définir la liste SACL pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="2999b-109">Specify SACL\_SECURITY\_INFORMATION in the [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) and [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) functions to get and set the SACL for the object.</span></span> <span data-ttu-id="2999b-110">Utilisez les indicateurs définir le succès de l' \_ audit \_ , définir \_ l’échec de l’audit \_ et révoquer l' \_ accès dans le paramètre *AccessMode* .</span><span class="sxs-lookup"><span data-stu-id="2999b-110">Use the SET\_AUDIT\_SUCCESS, SET\_AUDIT\_FAILURE, and REVOKE\_ACCESS flags in the *AccessMode* parameter.</span></span> <span data-ttu-id="2999b-111">Pour plus d’informations sur ces indicateurs, consultez [**\_ mode d’accès**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span><span class="sxs-lookup"><span data-stu-id="2999b-111">For information about these flags, see [**ACCESS\_MODE**](/windows/win32/api/accctrl/ne-accctrl-access_mode).</span></span>

<span data-ttu-id="2999b-112">Utilisez ce code pour ajouter une [entrée](object-specific-aces.md) du contrôle d’accès spécifique à l’objet à la liste DACL d’un objet de service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="2999b-112">Use this code to add an [object-specific ACE](object-specific-aces.md) to the DACL of a directory service object.</span></span> <span data-ttu-id="2999b-113">Pour spécifier les GUID dans une entrée du contrôle d’accès spécifique à un objet, définissez le paramètre *TrusteeForm* sur Trusted \_ is \_ Objects, le \_ \_ nom ou le tiers de confiance \_ is \_ Objects and \_ \_ sid, et définissez le paramètre *pszTrustee* sur un pointeur vers un [**objet \_ , un \_ nom**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) ou un objet et une structure [**\_ \_ sid**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) .</span><span class="sxs-lookup"><span data-stu-id="2999b-113">To specify the GUIDs in an object-specific ACE, set the *TrusteeForm* parameter to TRUSTEE\_IS\_OBJECTS\_AND\_NAME or TRUSTEE\_IS\_OBJECTS\_AND\_SID and set the *pszTrustee* parameter to be a pointer to an [**OBJECTS\_AND\_NAME**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) or [**OBJECTS\_AND\_SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) structure.</span></span>

<span data-ttu-id="2999b-114">Cet exemple utilise la fonction [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) pour récupérer la liste DACL existante.</span><span class="sxs-lookup"><span data-stu-id="2999b-114">This example uses the [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) function to get the existing DACL.</span></span> <span data-ttu-id="2999b-115">Elle remplit ensuite une structure [**d' \_ accès explicite**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) avec les informations relatives à une entrée du contrôle d’accès et utilise la fonction [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) pour fusionner la nouvelle entrée du contrôle d’accès avec les entrées de contrôle d’accès existantes dans la liste DACL.</span><span class="sxs-lookup"><span data-stu-id="2999b-115">Then it fills an [**EXPLICIT\_ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) structure with information about an ACE and uses the [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) function to merge the new ACE with any existing ACEs in the DACL.</span></span> <span data-ttu-id="2999b-116">Enfin, l’exemple appelle la fonction [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) pour attacher la nouvelle liste DACL au [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2999b-116">Finally, the example calls the [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) function to attach the new DACL to the [*security descriptor*](/windows/desktop/SecGloss/s-gly) of the object.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

DWORD AddAceToObjectsSecurityDescriptor (
    LPTSTR pszObjName,          // name of object
    SE_OBJECT_TYPE ObjectType,  // type of object
    LPTSTR pszTrustee,          // trustee for new ACE
    TRUSTEE_FORM TrusteeForm,   // format of trustee structure
    DWORD dwAccessRights,       // access mask for new ACE
    ACCESS_MODE AccessMode,     // type of ACE
    DWORD dwInheritance         // inheritance flags for new ACE
) 
{
    DWORD dwRes = 0;
    PACL pOldDACL = NULL, pNewDACL = NULL;
    PSECURITY_DESCRIPTOR pSD = NULL;
    EXPLICIT_ACCESS ea;

    if (NULL == pszObjName) 
        return ERROR_INVALID_PARAMETER;

    // Get a pointer to the existing DACL.

    dwRes = GetNamedSecurityInfo(pszObjName, ObjectType, 
          DACL_SECURITY_INFORMATION,
          NULL, NULL, &pOldDACL, NULL, &pSD);
    if (ERROR_SUCCESS != dwRes) {
        printf( "GetNamedSecurityInfo Error %u\n", dwRes );
        goto Cleanup; 
    }  

    // Initialize an EXPLICIT_ACCESS structure for the new ACE. 

    ZeroMemory(&ea, sizeof(EXPLICIT_ACCESS));
    ea.grfAccessPermissions = dwAccessRights;
    ea.grfAccessMode = AccessMode;
    ea.grfInheritance= dwInheritance;
    ea.Trustee.TrusteeForm = TrusteeForm;
    ea.Trustee.ptstrName = pszTrustee;

    // Create a new ACL that merges the new ACE
    // into the existing DACL.

    dwRes = SetEntriesInAcl(1, &ea, pOldDACL, &pNewDACL);
    if (ERROR_SUCCESS != dwRes)  {
        printf( "SetEntriesInAcl Error %u\n", dwRes );
        goto Cleanup; 
    }  

    // Attach the new ACL as the object's DACL.

    dwRes = SetNamedSecurityInfo(pszObjName, ObjectType, 
          DACL_SECURITY_INFORMATION,
          NULL, NULL, pNewDACL, NULL);
    if (ERROR_SUCCESS != dwRes)  {
        printf( "SetNamedSecurityInfo Error %u\n", dwRes );
        goto Cleanup; 
    }  

    Cleanup:

        if(pSD != NULL) 
            LocalFree((HLOCAL) pSD); 
        if(pNewDACL != NULL) 
            LocalFree((HLOCAL) pNewDACL); 

        return dwRes;
}

```



 

 
