---
title: Authentification du fournisseur de services
description: Authentification du fournisseur de services
ms.assetid: e48a8a7c-0277-4f0c-bad2-5bc9d0286da8
keywords:
- Gestionnaire de périphériques Windows Media, authentification
- Gestionnaire de périphériques, authentification
- Guide de programmation, authentification
- fournisseurs de services, authentification
- création de fournisseurs de services, authentification
- Authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271bf5594e4adaede01bb8e3795780f8f5c5177a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510623"
---
# <a name="authenticating-the-service-provider"></a><span data-ttu-id="07baf-109">Authentification du fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="07baf-109">Authenticating the Service Provider</span></span>

<span data-ttu-id="07baf-110">Pour être accessible à partir de Windows Media Gestionnaire de périphériques, un fournisseur de services doit hériter et implémenter l’interface [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .</span><span class="sxs-lookup"><span data-stu-id="07baf-110">To be accessible from Windows Media Device Manager, a service provider must inherit and implement the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span>

<span data-ttu-id="07baf-111">Pour s’authentifier, un fournisseur de services effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="07baf-111">To authenticate itself, a service provider performs the following steps:</span></span>

1.  <span data-ttu-id="07baf-112">En cas d’instanciation, elle crée un nouvel objet global [CSecureChannelServer](csecurechannelserver-class.md) et définit les valeurs de certificat et de clé à partir de son fichier de clé.</span><span class="sxs-lookup"><span data-stu-id="07baf-112">On instantiation, it creates a new global [CSecureChannelServer](csecurechannelserver-class.md) object and sets the certificate and key values from its key file.</span></span>
2.  <span data-ttu-id="07baf-113">Il implémente les méthodes [**IComponentAuthenticate :: SACAuth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) et [**IComponentAuthenticate :: SACGetProtocols**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) en passant simplement les paramètres dans son membre CSecureChannelServer global.</span><span class="sxs-lookup"><span data-stu-id="07baf-113">It implements the [**IComponentAuthenticate::SACAuth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) and [**IComponentAuthenticate::SACGetProtocols**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) methods by simply passing the parameters into its global CSecureChannelServer member.</span></span>
3.  <span data-ttu-id="07baf-114">Avant de gérer les méthodes de Gestionnaire de périphériques Windows Media implémentées, le fournisseur de services doit vérifier l’authentification de l’appelant en appelant CSecureChannelServer :: fIsAuthenticated et échouer si l’appelant n’est pas authentifié.</span><span class="sxs-lookup"><span data-stu-id="07baf-114">Before handling any implemented Windows Media Device Manager methods, the service provider must verify the caller's authentication by calling CSecureChannelServer::fIsAuthenticated, and failing if the caller is not authenticated.</span></span>

<span data-ttu-id="07baf-115">Ces étapes sont présentées dans les exemples C++ suivants.</span><span class="sxs-lookup"><span data-stu-id="07baf-115">These steps are shown in the following C++ examples.</span></span>

<span data-ttu-id="07baf-116">**Création de l’objet CSecureChannelServer**</span><span class="sxs-lookup"><span data-stu-id="07baf-116">**Creating the CSecureChannelServer object**</span></span>


```C++
CMyServiceProvider::CMyServiceProvider()
{
    HRESULT hr = S_OK;

    // Create the persistent SAC object.
    g_pSAC = new CSecureChannelServer();

    // Set the SAC certificate.
    if (g_pSAC)
    {
        hr = g_pSAC->SetCertificate(
             SAC_CERT_V1,
            (BYTE*)abCert, sizeof(abCert), // SP's certificate.
            (BYTE*)abPVK, sizeof(abPVK)    // SP's key.
        );
    }   
    if (FAILED(hr)) return hr;

    //... Perform other class initialization here ...

    return hr;
}
```



<span data-ttu-id="07baf-117">**Implémentation des méthodes IComponentAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="07baf-117">**Implementing the IComponentAuthenticate methods**</span></span>


```C++
STDMETHODIMP CMDServiceProvider::SACAuth(
    DWORD   dwProtocolID,
    DWORD   dwPass,
    BYTE   *pbDataIn,
    DWORD   dwDataInLen,
    BYTE  **ppbDataOut,
    DWORD  *pdwDataOutLen)
{
    HRESULT hr = S_OK;

    // Verify that the global CSecureChannelServer member still exists.
    if (!g_pSAC)
        return E_FAIL;

    // Just pass the call to the global SAC member.
    hr = g_pSAC->SACAuth(
        dwProtocolID,
        dwPass,
        pbDataIn, dwDataInLen,
        ppbDataOut, pdwDataOutLen
    );
    return hr;
}

STDMETHODIMP CMDServiceProvider::SACGetProtocols(
    DWORD **ppdwProtocols,
    DWORD  *pdwProtocolCount)
{
    HRESULT hr = E_FAIL;

    if (!g_pSAC)
        return hr;

    hr = g_pSAC->SACGetProtocols(
        ppdwProtocols,
        pdwProtocolCount
    );
    return hr;
}
```



<span data-ttu-id="07baf-118">**Vérification de l’authentification de l’appelant**</span><span class="sxs-lookup"><span data-stu-id="07baf-118">**Verifying the caller's authentication**</span></span>

<span data-ttu-id="07baf-119">L’exemple de code suivant montre un fournisseur de services vérifiant l’authentification de l’appelant dans le cadre de son implémentation de l’interface **IMDServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="07baf-119">The following code example shows a service provider checking the caller's authentication as part of its implementation of the **IMDServiceProvider** interface.</span></span>


```C++
STDMETHODIMP CMyServiceProvider::GetDeviceCount(DWORD * pdwCount)
{
    HRESULT hr = S_OK;
    if (!g_pSAC)
        return E_FAIL;

    if (!(g_pSAC->fIsAuthenticated()))
        return WMDM_E_NOTCERTIFIED;

    *pdwCount = m_DeviceCount;

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="07baf-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="07baf-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07baf-121">**Création d’un fournisseur de services**</span><span class="sxs-lookup"><span data-stu-id="07baf-121">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




