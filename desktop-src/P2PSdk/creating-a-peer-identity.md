---
description: L’API Identity Manager vous permet de créer une identité d’homologue à utiliser dans un réseau pair à pair.
ms.assetid: 44b85bbc-9594-4f68-b930-51a28422b571
title: Création d’une identité d’homologue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab240b9fa1265ba03bfb1ce584dabed92988620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952037"
---
# <a name="creating-a-peer-identity"></a>Création d’une identité d’homologue

L’API Identity Manager vous permet de créer une identité d’homologue à utiliser dans un réseau pair à pair.

Lorsque vous créez une identité d’homologue, vous pouvez fournir les informations facultatives suivantes :

-   [Classifieur](peer-names.md)
-   Nom convivial
-   Fournisseur de services de chiffrement

> [!Note]  
> Dans la mesure du possible, réutilisez une identité d’homologue.

 

## <a name="example-of-creating-and-deleting-a-peer-identity"></a>Exemple de création et de suppression d’une identité d’homologue

L’extrait de code suivant vous montre comment créer et supprimer une identité d’homologue à l’aide d’un classifieur et d’un nom convivial.


```C++
#define UNICODE
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "p2p.lib")

//-----------------------------------------------------------------------------
// Function: CreateIdentity
//
// Purpose:  Creates a new Identity.
//
// Returns:  HRESULT
//
HRESULT CreateIdentity(PWSTR pwzFriendlyName)
{
    HRESULT     hr              = S_OK;   
    PWSTR       pwzClassifier   = L"GroupMember";
    PWSTR       pwzIdentity     = NULL;

    hr = PeerIdentityCreate(pwzClassifier, pwzFriendlyName, 0, &pwzIdentity);
    if (FAILED(hr))
    {            
        printf("Failed to create identity.");
    }
    else
    {
        printf("Identity: %s", pwzFriendlyName);
    }
       
    PeerFreeData(pwzIdentity);    

    return hr;
}


//-----------------------------------------------------------------------------
// Function: DeleteIdentity
//
// Purpose:  Delete the identity created by CreateIdentity
//
// Returns:  HRESULT
//
HRESULT DeleteIdentity()
{
    HRESULT hr = S_OK;

    if (g_pwzIdentity)
    {
        hr = PeerIdentityDelete(g_pwzIdentity);
        g_pwzIdentity = NULL;
    }

    return hr;
}
```



 

 



