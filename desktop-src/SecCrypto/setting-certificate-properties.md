---
description: 'Utilisez la méthode ICertServerPolicy :: SetCertificateProperty pour définir les propriétés de l’objet d’un certificat.'
ms.assetid: 93e4b05d-0230-4562-8052-4e118fd92057
title: Définition des propriétés d’un certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe131190b10b431427162e628004d8b21053a099015a68184196b7218967222
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117974567"
---
# <a name="setting-certificate-properties"></a>Définition des propriétés d’un certificat

Utilisez la méthode [**ICertServerPolicy :: SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) pour définir les propriétés de l’objet d’un certificat. Les propriétés de l’objet sont des propriétés associées au propriétaire du certificat ou à la personne qui a demandé le certificat. Pour obtenir la liste des propriétés de l’objet, consultez [Propriétés du nom](name-properties.md).

Vous pouvez également utiliser la méthode [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) pour définir les propriétés de certificat NotBefore et notAfter. Pour obtenir une description des propriétés du certificat NotBefore et NotAfter, consultez [Propriétés du certificat](certificate-properties.md).

Utilisez la méthode [**ICertServerPolicy :: SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) pour ajouter un nombre quelconque d’extensions au certificat. Vous pouvez utiliser des extensions pour ajouter des informations supplémentaires sur l’objet ou l’utilisation au certificat. Pour plus d’informations, consultez [gestionnaires d’extensions](extension-handlers.md).

L’exemple suivant définit une propriété et une extension de certificat sur un certificat. Vous appelez les méthodes [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) et [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) dans votre implémentation [**ICertPolicy2 :: VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest) . L’exemple n’est pas une implémentation de **VerifyRequest** complète. l’exemple n’affiche pas la logique de vérification.


```C++
#include <windows.h>
#include <stdio.h>

STDMETHODIMP CCertPolicy::VerifyRequest(
             BSTR const strConfig,
             LONG Context,
             LONG bNewRequest,
             LONG Flags,
             LONG __RPC_FAR *pDisposition)
{
    HRESULT hr = S_OK;
    ICertServerPolicy *pServer = NULL;
    BSTR bstrPropName = NULL;
    VARIANT vPropValue;
    BSTR bstrExtName = NULL;
    VARIANT vExtValue;


    // Retrieve an ICertServerPolicy interface pointer.
    hr = CoCreateInstance( CLSID_CCertServerPolicy,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ICertServerPolicy,
                           (void **) &pServer );
    if (FAILED( hr ))
    {
        printf("Failed CoCreateInstance for ICertServerPolicy "
            "- %x\n", hr );
        return hr;
    }

    // Set the context to which this request refers.
    hr = pServer->SetContext(Context);
    if (FAILED( hr ))
    {
        printf("Failed SetContext(%u) - %x\n", Context, hr );
        pServer->Release();
        return hr;
    }

    // Specify the subject property to set on the certificate.
    bstrPropName = SysAllocString(L"Subject.EMail");
    if ( NULL == bstrPropName )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for bstrPropName "
            "(no memory)\n" );
        pServer->Release();
        return hr;
    }

    VariantInit( &vPropValue );
    vPropValue.VT_BSTR;
    vPropValue.bstrVal = SysAllocString(L"someone@example.com");
    if ( NULL == vPropValue.bstrVal )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for vPropValue "
            "(no memory)\n" );
        SysFreeString(bstrPropName);
        pServer->Release();
        return hr;
    }

    // Set the subject property on the certificate.
    hr = pServer->SetCertificateProperty( bstrPropName,
                                          PROPTYPE_STRING,
                                          &vPropValue );
    SysFreeString(bstrPropName);
    VariantClear(&vPropValue);
    if (FAILED(hr))
    {
        printf("Failed SetCertificateProperty - %x\n", hr);
        pServer->Release();
        return hr;
    }

    // Specify the extension property to set on the certificate.
    bstrExtName = SysAllocString(L"2.29.38.4");
    if ( NULL == bstrExtName )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for bstrExtName "
            "(no memory)\n" );
        pServer->Release();
        return hr;
    }

    VariantInit( &vExtValue );
    vExtValue.VT_BSTR;
    vExtValue.bstrVal = SysAllocString
        (L"https://example.microsoft.com");
    if ( NULL == vExtValue.bstrVal )
    {
        hr = E_OUTOFMEMORY; 
        printf("Failed SysAllocString for vExtValue (no memory)\n" );
        SysFreeString(bstrExtName);
        pServer->Release();
        return hr;
    }

    // Set the extension property on the certificate.
    hr = pServer->SetCertificateExtension( bstrExtName,
                                           PROPTYPE_STRING,
                                           EXTENSION_CRITICAL_FLAG,
                                           &vExtValue );
    SysFreeString(bstrExtName);
    VariantClear(&vExtValue);
    if (FAILED(hr))
    {
        printf("Failed SetCertificateExtension - %x\n", hr);
        pServer->Release();
        return hr;
    }

    pServer->Release();
    return(hr);

}
```



 

 



