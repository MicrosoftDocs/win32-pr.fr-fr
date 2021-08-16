---
title: Interface IADsDeleteOps
description: L’interface IADsDeleteOps est utilisée dans les routines de surveillance et de maintenance pour le magasin d’annuaires sous-jacent. Il peut supprimer des objets feuilles et des sous-arborescences entières en une seule opération.
ms.assetid: 821b71c2-e9f5-4ca8-9366-e8a3f1907670
ms.tgt_platform: multiple
keywords:
- Interface ADSI de l’interface IADsDeleteOps
- IADsDeleteOps ADSI, utilisation
- ADSI ADSI, exemple de code C/C++, utilisant IADsDeleteOps pour supprimer des groupes entiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192411e53f54de2a5f73cc043f35cea6787f4b879972b6a69ada4760c175292a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839942"
---
# <a name="iadsdeleteops-interface"></a>Interface IADsDeleteOps

L’interface [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) est utilisée dans les routines de surveillance et de maintenance pour le magasin d’annuaires sous-jacent. Il peut supprimer des objets feuilles et des sous-arborescences entières en une seule opération.

Si cette interface n’était pas prise en charge, la suppression d’un objet de Active Directory nécessiteraient que chaque objet contenu soit énuméré et supprimé de manière récursive. Avec cette interface, tout objet conteneur, contenant tous les objets et sous-objets qu’il contient, peut être supprimé à l’aide d’une seule opération.

L’exemple de code suivant supprime le conteneur « ENG » et tous les objets enfants.


```C++
HRESULT hr;
IADsDeleteOps *pDeleteOps;
LPWSTR pwszUsername = NULL;
LPWSTR pwszPassword = NULL;

// Insert code to securely retrieve the pwszUsername and pwszPassword
// or leave as NULL to use the default security context of the 
// calling application.
 
// Bind to the LDAP provider.
hr = ADsOpenObject(L"LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com", 
    pwszUsername,
    pwszPassword,
    0,
    ADS_SECURE_AUTHENTICATION,
    IID_IADsDeleteOps, 
    (void**)&pDeleteOps);
if(S_OK == hr)
{
    // Delete the container and all child objects.
    pDeleteOps->DeleteObject(0);

    // Release the interface.
    pDeleteOps->Release();
}

if(pwszUsername)
{
    SecureZeroMemory(pwszUsername, lstrlen(pwszUsername) * sizeof(TCHAR));
}
if(pwszPassword)
{
    SecureZeroMemory(pwszPassword, lstrlen(pwszPassword) * sizeof(TCHAR));
}
```



L’exemple de code suivant supprime le conteneur « ENG » et tous les objets enfants.


```VB
Dim DeleteOps As IADsDeleteOps

' Bind to the LDAP provider.
Set DeleteOps = GetObject("LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com")

' Delete the container and all child objects.
DeleteOps.DeleteObject (0)
```



 

 




