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
# <a name="authenticating-the-service-provider"></a>Authentification du fournisseur de services

Pour être accessible à partir de Windows Media Gestionnaire de périphériques, un fournisseur de services doit hériter et implémenter l’interface [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .

Pour s’authentifier, un fournisseur de services effectue les étapes suivantes :

1.  En cas d’instanciation, elle crée un nouvel objet global [CSecureChannelServer](csecurechannelserver-class.md) et définit les valeurs de certificat et de clé à partir de son fichier de clé.
2.  Il implémente les méthodes [**IComponentAuthenticate :: SACAuth**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacauth) et [**IComponentAuthenticate :: SACGetProtocols**](/windows/desktop/api/mswmdm/nf-mswmdm-icomponentauthenticate-sacgetprotocols) en passant simplement les paramètres dans son membre CSecureChannelServer global.
3.  Avant de gérer les méthodes de Gestionnaire de périphériques Windows Media implémentées, le fournisseur de services doit vérifier l’authentification de l’appelant en appelant CSecureChannelServer :: fIsAuthenticated et échouer si l’appelant n’est pas authentifié.

Ces étapes sont présentées dans les exemples C++ suivants.

**Création de l’objet CSecureChannelServer**


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



**Implémentation des méthodes IComponentAuthenticate**


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



**Vérification de l’authentification de l’appelant**

L’exemple de code suivant montre un fournisseur de services vérifiant l’authentification de l’appelant dans le cadre de son implémentation de l’interface **IMDServiceProvider** .


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création d’un fournisseur de services**](creating-a-service-provider.md)
</dt> </dl>

 

 




