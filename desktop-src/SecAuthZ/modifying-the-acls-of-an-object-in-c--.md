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
# <a name="modifying-the-acls-of-an-object-in-c"></a>Modification des listes de contrôle d’accès d’un objet en C++

L’exemple suivant ajoute une [*entrée de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) à la [*liste de contrôle d’accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) d’un objet.

Le paramètre *AccessMode* détermine le type de nouvelle entrée du contrôle d’accès et la façon dont la nouvelle entrée du contrôle d’accès est combinée avec les entrées de contrôle d’accès existantes pour le tiers de confiance spécifié. Utilisez les indicateurs accorder l’accès \_ , définir \_ l’accès, refuser \_ l’accès ou révoquer l’accès \_ dans le paramètre *AccessMode* . Pour plus d’informations sur ces indicateurs, consultez [**\_ mode d’accès**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

Vous pouvez utiliser du code similaire pour utiliser une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL). Spécifiez \_ les \_ informations de sécurité SACL dans les fonctions [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) et [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) pour obtenir et définir la liste SACL pour l’objet. Utilisez les indicateurs définir le succès de l' \_ audit \_ , définir \_ l’échec de l’audit \_ et révoquer l' \_ accès dans le paramètre *AccessMode* . Pour plus d’informations sur ces indicateurs, consultez [**\_ mode d’accès**](/windows/win32/api/accctrl/ne-accctrl-access_mode).

Utilisez ce code pour ajouter une [entrée](object-specific-aces.md) du contrôle d’accès spécifique à l’objet à la liste DACL d’un objet de service d’annuaire. Pour spécifier les GUID dans une entrée du contrôle d’accès spécifique à un objet, définissez le paramètre *TrusteeForm* sur Trusted \_ is \_ Objects, le \_ \_ nom ou le tiers de confiance \_ is \_ Objects and \_ \_ sid, et définissez le paramètre *pszTrustee* sur un pointeur vers un [**objet \_ , un \_ nom**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) ou un objet et une structure [**\_ \_ sid**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) .

Cet exemple utilise la fonction [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) pour récupérer la liste DACL existante. Elle remplit ensuite une structure [**d' \_ accès explicite**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) avec les informations relatives à une entrée du contrôle d’accès et utilise la fonction [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) pour fusionner la nouvelle entrée du contrôle d’accès avec les entrées de contrôle d’accès existantes dans la liste DACL. Enfin, l’exemple appelle la fonction [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) pour attacher la nouvelle liste DACL au [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) de l’objet.


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



 

 
