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
ms.openlocfilehash: 6332dd28e903996e8688d6c6fc672df080822595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517938"
---
# <a name="iadsdeleteops-interface"></a><span data-ttu-id="56720-107">Interface IADsDeleteOps</span><span class="sxs-lookup"><span data-stu-id="56720-107">IADsDeleteOps Interface</span></span>

<span data-ttu-id="56720-108">L’interface [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) est utilisée dans les routines de surveillance et de maintenance pour le magasin d’annuaires sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="56720-108">The [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) interface is used in supervisory and maintenance routines for the underlying directory store.</span></span> <span data-ttu-id="56720-109">Il peut supprimer des objets feuilles et des sous-arborescences entières en une seule opération.</span><span class="sxs-lookup"><span data-stu-id="56720-109">It can delete leaf objects and entire subtrees in a single operation.</span></span>

<span data-ttu-id="56720-110">Si cette interface n’était pas prise en charge, la suppression d’un objet de Active Directory nécessiteraient que chaque objet contenu soit énuméré et supprimé de manière récursive.</span><span class="sxs-lookup"><span data-stu-id="56720-110">If this interface were not supported, deleting an object from Active Directory would require that each contained object be recursively enumerated and deleted.</span></span> <span data-ttu-id="56720-111">Avec cette interface, tout objet conteneur, contenant tous les objets et sous-objets qu’il contient, peut être supprimé à l’aide d’une seule opération.</span><span class="sxs-lookup"><span data-stu-id="56720-111">With this interface, any container object, with all its contained objects and subobjects, can be deleted with a single operation.</span></span>

<span data-ttu-id="56720-112">L’exemple de code suivant supprime le conteneur « ENG » et tous les objets enfants.</span><span class="sxs-lookup"><span data-stu-id="56720-112">The following code example deletes the "Eng" container and all child objects.</span></span>


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



<span data-ttu-id="56720-113">L’exemple de code suivant supprime le conteneur « ENG » et tous les objets enfants.</span><span class="sxs-lookup"><span data-stu-id="56720-113">The following code example deletes the "Eng" container and all child objects.</span></span>


```VB
Dim DeleteOps As IADsDeleteOps

' Bind to the LDAP provider.
Set DeleteOps = GetObject("LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com")

' Delete the container and all child objects.
DeleteOps.DeleteObject (0)
```



 

 




