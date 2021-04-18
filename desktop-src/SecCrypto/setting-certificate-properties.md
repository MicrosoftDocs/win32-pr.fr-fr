---
description: 'Utilisez la méthode ICertServerPolicy :: SetCertificateProperty pour définir les propriétés de l’objet d’un certificat.'
ms.assetid: 93e4b05d-0230-4562-8052-4e118fd92057
title: Définition des propriétés d’un certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33534792e65c95e24125968a61cf6ac1ad27039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516201"
---
# <a name="setting-certificate-properties"></a><span data-ttu-id="95723-103">Définition des propriétés d’un certificat</span><span class="sxs-lookup"><span data-stu-id="95723-103">Setting Certificate Properties</span></span>

<span data-ttu-id="95723-104">Utilisez la méthode [**ICertServerPolicy :: SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) pour définir les propriétés de l’objet d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="95723-104">Use the [**ICertServerPolicy::SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) method to set the subject properties of a certificate.</span></span> <span data-ttu-id="95723-105">Les propriétés de l’objet sont des propriétés associées au propriétaire du certificat ou à la personne qui a demandé le certificat.</span><span class="sxs-lookup"><span data-stu-id="95723-105">Subject properties are properties related to the owner of the certificate or the individual who requested the certificate.</span></span> <span data-ttu-id="95723-106">Pour obtenir la liste des propriétés de l’objet, consultez [Propriétés du nom](name-properties.md).</span><span class="sxs-lookup"><span data-stu-id="95723-106">For a list of subject properties, see [Name Properties](name-properties.md).</span></span>

<span data-ttu-id="95723-107">Vous pouvez également utiliser la méthode [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) pour définir les propriétés de certificat NotBefore et notAfter.</span><span class="sxs-lookup"><span data-stu-id="95723-107">You can also use the [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) method to set the NotBefore and NotAfter certificate properties.</span></span> <span data-ttu-id="95723-108">Pour obtenir une description des propriétés du certificat NotBefore et NotAfter, consultez [Propriétés du certificat](certificate-properties.md).</span><span class="sxs-lookup"><span data-stu-id="95723-108">For a description of the NotBefore and NotAfter certificate properties, see [Certificate Properties](certificate-properties.md).</span></span>

<span data-ttu-id="95723-109">Utilisez la méthode [**ICertServerPolicy :: SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) pour ajouter un nombre quelconque d’extensions au certificat.</span><span class="sxs-lookup"><span data-stu-id="95723-109">Use the [**ICertServerPolicy::SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) method to add any number of extensions to the certificate.</span></span> <span data-ttu-id="95723-110">Vous pouvez utiliser des extensions pour ajouter des informations supplémentaires sur l’objet ou l’utilisation au certificat.</span><span class="sxs-lookup"><span data-stu-id="95723-110">You can use extensions to add supplemental subject or usage information to the certificate.</span></span> <span data-ttu-id="95723-111">Pour plus d’informations, consultez [gestionnaires d’extensions](extension-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="95723-111">For more information, see [Extension Handlers](extension-handlers.md).</span></span>

<span data-ttu-id="95723-112">L’exemple suivant définit une propriété et une extension de certificat sur un certificat.</span><span class="sxs-lookup"><span data-stu-id="95723-112">The following example sets a certificate property and extension on a certificate.</span></span> <span data-ttu-id="95723-113">Vous appelez les méthodes [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) et [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) dans votre implémentation [**ICertPolicy2 :: VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest) .</span><span class="sxs-lookup"><span data-stu-id="95723-113">You call the [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) and [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) methods in your [**ICertPolicy2::VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest) implementation.</span></span> <span data-ttu-id="95723-114">L’exemple n’est pas une implémentation de **VerifyRequest** complète. l’exemple n’affiche pas la logique de vérification.</span><span class="sxs-lookup"><span data-stu-id="95723-114">The example is not a complete **VerifyRequest** implementation; the example does not show verification logic.</span></span>


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



 

 



