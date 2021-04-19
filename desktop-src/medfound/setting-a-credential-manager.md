---
description: Définition d’un gestionnaire d’informations d’identification
ms.assetid: a20c2e6c-e9d9-438f-a57a-e3080587c11c
title: Définition d’un gestionnaire d’informations d’identification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c98d9d9572438a63f93f916a0084f8a33a7bca5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530843"
---
# <a name="setting-a-credential-manager"></a>Définition d’un gestionnaire d’informations d’identification

Une application qui fournit des informations d’identification à la source réseau doit effectuer les opérations suivantes :

1.  Implémentez un objet gestionnaire d’informations d’identification qui expose l’interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .
2.  Avant de créer la source réseau, créez une nouvelle banque de propriétés.
3.  Définissez la [**propriété \_ \_ Gestionnaire d’informations d’identification MFNETSOURCE**](mfnetsource-credential-manager-property.md) dans la Banque de propriétés. La valeur de la propriété est un pointeur vers l’interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .
4.  Transmettez un pointeur vers la Banque de propriétés vers le programme de résolution de source, comme décrit dans [configuration d’une source de média](configuring-a-media-source.md).

Les sources réseau utilisent le gestionnaire d’informations d’identification pour récupérer les informations d’identification de l’utilisateur. Si la source réseau nécessite des informations d’identification pour accéder à une ressource réseau, elle appelle la méthode [**IMFNetCredentialManager :: BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) de l’application. Cet appel démarre une demande asynchrone pour obtenir les informations d’identification de l’utilisateur. La méthode **BeginGetCredentials** peut récupérer les informations d’identification à partir du cache des informations d’identification ou de l’utilisateur. Les informations d’identification sont stockées dans un *objet d’informations d’identification*. Lorsque l’opération est terminée, l’application appelle l’interface de rappel pour notifier la source réseau. La source réseau appelle [**IMFNetCredentialManager :: EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) pour terminer l’opération asynchrone.

Étant donné qu’il s’agit d’une opération asynchrone, l’application doit distribuer le rappel à la fin de l’opération. Pour obtenir des instructions pas à pas sur l’écriture d’une méthode asynchrone, consultez [écriture d’une méthode asynchrone](writing-an-asynchronous-method.md).

L’exemple suivant montre comment définir la propriété [**du \_ \_ Gestionnaire d’informations d’identification MFNETSOURCE**](mfnetsource-credential-manager-property.md) sur la source réseau.


```C++
// Creates a media source from a URL.
//
// Demonstrates how to set a credential manager on the network source.

HRESULT CreateMediaSourceWithCredentialManager(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CCredentialManager *pCredentials = new (std::nothrow) CCredentialManager();

    if (pCredentials == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_CREDENTIAL_MANAGER;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pCredentials->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(key, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pCredentials);

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Authentification de la source réseau](network-source-authentication.md)
</dt> </dl>

 

 



