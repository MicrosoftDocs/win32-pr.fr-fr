---
title: Exemple d’extraction de certificat d’ordinateur
description: Exemple d’extraction de certificat d’ordinateur
ms.assetid: 4112e29e-7c86-4825-9798-dd1a81b82083
keywords:
- Windows Media Format SDK, certificats d’ordinateur
- Windows Media Format SDK, certificats
- Windows Media Format SDK, exemple de code
- Windows Media Format SDK, exemples de code
- gestion des droits numériques (DRM), certificats d’ordinateur
- DRM (gestion des droits numériques), certificats d’ordinateur
- gestion des droits numériques (DRM), certificats
- DRM (gestion des droits numériques), certificats
- gestion des droits numériques (DRM), exemple de code
- DRM (gestion des droits numériques), exemple de code
- gestion des droits numériques (DRM), exemples de code
- DRM (gestion des droits numériques), exemples de code
- API étendues du client DRM, certificats d’ordinateur
- API étendues clientes, certificats d’ordinateur
- API étendues du client DRM, certificats
- API étendues clientes, certificats
- API étendues du client DRM, exemple de code
- API étendues clientes, exemple de code
- API étendues du client DRM, exemples de code
- API étendues clientes, exemples de code
- certificats, exemples de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e68a8ecbaf3e3c0ba8001a7a2094ab2b4a7e09a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380255"
---
# <a name="get-machine-certificate-example"></a><span data-ttu-id="db6e4-124">Exemple d’extraction de certificat d’ordinateur</span><span class="sxs-lookup"><span data-stu-id="db6e4-124">Get Machine Certificate Example</span></span>

<span data-ttu-id="db6e4-125">L’exemple suivant montre comment récupérer la collection de certificats de l’ordinateur :</span><span class="sxs-lookup"><span data-stu-id="db6e4-125">The following example shows how to retrieve the machine certificate collection:</span></span>


```C++
HRESULT GetMachineCert( BYTE **ppbCert, DWORD *pcbCert )
{
    HRESULT hr = S_OK;
    IWMDRMProvider *pProvider = NULL;
    IWMDRMSecurity *pSecurity = NULL;
    BYTE rgbVersion[4];

    // Create a provider object.
    hr = WMDRMCreateProvider( &pProvider );
    if( FAILED( hr ) ) goto EXIT;

    // Create a security object from a provider object.
    hr = pProvider->CreateObject( IID_IWMDRMSecurity, (void**) &pSecurity );
    if( FAILED( hr ) ) goto EXIT;

    // Query the security to get the machine certificate.
    hr = pSecurity->GetMachineCertificate( WMDRM_CERTIFICATE_TYPE_V2,
        rgbVersion, ppbCert, pcbCert );

    if( FAILED( hr ) ) goto EXIT;

EXIT:

    SAFE_RELEASE( pSecurity );
    SAFE_RELEASE( pProvider );

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="db6e4-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db6e4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db6e4-127">**Exemples d’importation DRM**</span><span class="sxs-lookup"><span data-stu-id="db6e4-127">**DRM Import Examples**</span></span>](drm-import-examples.md)
</dt> </dl>

 

 




