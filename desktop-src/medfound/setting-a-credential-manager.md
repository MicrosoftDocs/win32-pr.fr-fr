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
# <a name="setting-a-credential-manager"></a><span data-ttu-id="0cbbf-103">Définition d’un gestionnaire d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="0cbbf-103">Setting a Credential Manager</span></span>

<span data-ttu-id="0cbbf-104">Une application qui fournit des informations d’identification à la source réseau doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0cbbf-104">An application that provides credentials to the network source must do the following:</span></span>

1.  <span data-ttu-id="0cbbf-105">Implémentez un objet gestionnaire d’informations d’identification qui expose l’interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="0cbbf-105">Implement a credential manager object that exposes the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span>
2.  <span data-ttu-id="0cbbf-106">Avant de créer la source réseau, créez une nouvelle banque de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0cbbf-106">Before you create the network source, create a new property store.</span></span>
3.  <span data-ttu-id="0cbbf-107">Définissez la [**propriété \_ \_ Gestionnaire d’informations d’identification MFNETSOURCE**](mfnetsource-credential-manager-property.md) dans la Banque de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0cbbf-107">Set the [**MFNETSOURCE\_CREDENTIAL\_MANAGER**](mfnetsource-credential-manager-property.md) property on the property store.</span></span> <span data-ttu-id="0cbbf-108">La valeur de la propriété est un pointeur vers l’interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="0cbbf-108">The value of the property is a pointer to the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span>
4.  <span data-ttu-id="0cbbf-109">Transmettez un pointeur vers la Banque de propriétés vers le programme de résolution de source, comme décrit dans [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="0cbbf-109">Pass a pointer to the property store to the source resolver, as described in [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="0cbbf-110">Les sources réseau utilisent le gestionnaire d’informations d’identification pour récupérer les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0cbbf-110">The network sources uses the credential manager to get user credentials.</span></span> <span data-ttu-id="0cbbf-111">Si la source réseau nécessite des informations d’identification pour accéder à une ressource réseau, elle appelle la méthode [**IMFNetCredentialManager :: BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) de l’application.</span><span class="sxs-lookup"><span data-stu-id="0cbbf-111">If the network source requires credentials to access a network resource, it calls the application's [**IMFNetCredentialManager::BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method.</span></span> <span data-ttu-id="0cbbf-112">Cet appel démarre une demande asynchrone pour obtenir les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0cbbf-112">This call starts an asynchronous request to gets the user's credentials.</span></span> <span data-ttu-id="0cbbf-113">La méthode **BeginGetCredentials** peut récupérer les informations d’identification à partir du cache des informations d’identification ou de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0cbbf-113">The **BeginGetCredentials** method can get the credentials either from the credential cache or from the user.</span></span> <span data-ttu-id="0cbbf-114">Les informations d’identification sont stockées dans un *objet d’informations d’identification*.</span><span class="sxs-lookup"><span data-stu-id="0cbbf-114">Credentials are stored in a *credential object*.</span></span> <span data-ttu-id="0cbbf-115">Lorsque l’opération est terminée, l’application appelle l’interface de rappel pour notifier la source réseau.</span><span class="sxs-lookup"><span data-stu-id="0cbbf-115">When the operation is complete, the application invokes the callback interface to notify the network source.</span></span> <span data-ttu-id="0cbbf-116">La source réseau appelle [**IMFNetCredentialManager :: EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) pour terminer l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="0cbbf-116">The network source calls [**IMFNetCredentialManager::EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) to complete the asynchronous operation.</span></span>

<span data-ttu-id="0cbbf-117">Étant donné qu’il s’agit d’une opération asynchrone, l’application doit distribuer le rappel à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0cbbf-117">Because this is an asynchronous operation, the application must dispatch the callback at the end of the operation.</span></span> <span data-ttu-id="0cbbf-118">Pour obtenir des instructions pas à pas sur l’écriture d’une méthode asynchrone, consultez [écriture d’une méthode asynchrone](writing-an-asynchronous-method.md).</span><span class="sxs-lookup"><span data-stu-id="0cbbf-118">For step-by-step instructions about writing an asynchronous method, see [Writing an Asynchronous Method](writing-an-asynchronous-method.md).</span></span>

<span data-ttu-id="0cbbf-119">L’exemple suivant montre comment définir la propriété [**du \_ \_ Gestionnaire d’informations d’identification MFNETSOURCE**](mfnetsource-credential-manager-property.md) sur la source réseau.</span><span class="sxs-lookup"><span data-stu-id="0cbbf-119">The following example shows how to set the [**MFNETSOURCE\_CREDENTIAL\_MANAGER**](mfnetsource-credential-manager-property.md) property on the network source.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0cbbf-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0cbbf-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cbbf-121">Authentification de la source réseau</span><span class="sxs-lookup"><span data-stu-id="0cbbf-121">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



