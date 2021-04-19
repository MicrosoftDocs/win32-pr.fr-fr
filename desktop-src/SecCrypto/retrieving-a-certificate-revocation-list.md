---
description: Montre comment récupérer une liste de révocation de certificats.
ms.assetid: b8fbffae-d968-453d-81f0-af9d60be5fa9
title: Récupération d’une liste de révocation de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9c7933ac5762c9367d7bdff150da011f789835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537066"
---
# <a name="retrieving-a-certificate-revocation-list"></a>Récupération d’une liste de révocation de certificats

Une [*autorité de certification*](../secgloss/c-gly.md) (ca) est responsable de la publication de sa [*liste de révocation de certificats*](../secgloss/c-gly.md) (CRL). La liste de révocation de certificats actuelle peut être récupérée à l’aide de la méthode [**ICertAdmin2 :: GetCRL**](/windows/desktop/api/Certadm/nf-certadm-icertadmin-getcrl) . Dans les cas où le certificat d’une autorité de certification a été renouvelé, vous devrez peut-être récupérer les listes de révocation de certificats pour les certificats d’autorité de certification précédents. Pour plus d’informations sur le renouvellement de l’autorité de certification, consultez Renouvellement de l' [autorité de certification](certification-authority-renewal.md). En outre, une autorité de certification peut publier des listes de révocation de certificats delta. Pour récupérer les listes de révocation de certificats pour les certificats d’autorité de certification renouvelés ou les listes CRL Delta, utilisez les méthodes [**ICertAdmin2 :: GetCAProperty**](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcaproperty) ou [**ICertRequest2 :: GetCAProperty**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getcaproperty) .

L’exemple suivant montre la récupération de la liste de révocation de certificats actuelle.


```C++
    ICertAdmin2 * pCertAdmin2 = NULL;  // pointer to interface object
    BSTR bstrCA = NULL;  // variable for computer\CAname
    BSTR bstrCRL = NULL;  // variable to contain the retrieved CRL
    HRESULT hr;

    // Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED(hr))
    {
        printf("Failed CoInitializeEx [%x]\n", hr);
        goto error;
    }

    // Create the CertAdmin object,
    // and get a pointer to its ICertAdmin interface.
    hr = CoCreateInstance( CLSID_CCertAdmin,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ICertAdmin2,
                           (void **)&pCertAdmin2;);
    if (FAILED(hr))
    {
        printf("Failed CoCreateInstance pCertAdmin2 [%x]\n", hr);
        goto error;
    }

    // Note the use of two '\' in C++ to produce one '\'.
    bstrCA = SysAllocString(L"<COMPUTERNAMEHERE>\\<CANAMEHERE>");
    if (FAILED(hr))
    {
        printf("Failed to allocate memory for bstrCA\n");
        goto error;
    }

    // Retrieve the CRL.
    hr = pCertAdmin2->GetCRL( bstrCA, CR_OUT_BINARY, &bstrCRL );
    if (FAILED(hr))
    {
        printf("Failed GetCRL [%x]\n", hr);
        goto error;
    }
    else
        printf("CRL retrieved successfully\n");
        // Use the CRL as needed...

    // Processing is finished.

error:

    // Free BSTR values.
    if (NULL != bstrCA)
        SysFreeString(bstrCA);

    if (NULL != bstrCRL)
        SysFreeString(bstrCRL);

    // Clean up object resources.
    if (NULL != pCertAdmin2)
        pCertAdmin2->Release();

    // Free COM resources.
    CoUninitialize();
```



L’exemple suivant montre l’extraction de listes de révocation de certificats de base et Delta, y compris celles des certificats d’autorité de certification qui ont été renouvelés. L’exemple utilise [**ICertAdmin2 :: GetCAProperty**](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcaproperty), bien que [**ICertRequest2 :: GetCAProperty**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getcaproperty) offre des fonctionnalités similaires.


```C++
    LONG nCACertCount, nIndex, nCRLState;
    VARIANT    variant;

    VariantInit(&variant);
    // Determine the number of CA certificates.
    hr = pCertAdmin2->GetCAProperty(bstrCA, 
                                CR_PROP_CASIGCERTCOUNT,
                                0,
                                PROPTYPE_LONG, 
                                CR_OUT_BINARY, 
                                &variant);
    if (FAILED(hr))
    {
        printf("Failed call to GetCAProperty - "
            "CR_PROP_CASIGCERTCOUNT\n");
        goto error;
    }
    nCACertCount = variant.lVal;

    for (nIndex = 0; nIndex < nCACertCount; nIndex++)
    {
           // Determine the CRL state for each certificate index.
           pCertAdmin2->GetCAProperty(bstrCA, 
                               CR_PROP_CRLSTATE, 
                               nIndex, 
                               PROPTYPE_LONG, 
                               CR_OUT_BINARY, 
                               &variant);
        if (FAILED(hr))
        {
            printf("Failed call to GetCAProperty - "
                "CR_PROP_CRLSTATE\n");
            goto error;
        }
        nCRLState = variant.lVal;

        // Process certificate indices only when 
        // the CRL state is valid.
        if (CA_DISP_VALID == nCRLState)
        {
           // Retrieve the base CRL.
           hr = pCertAdmin2->GetCAProperty(bstrCA,
                                   CR_PROP_BASECRL, 
                                   nIndex, 
                                   PROPTYPE_BINARY,
                                   CR_OUT_BINARY, 
                                   &variant);
           if (FAILED(hr))
           {
               printf("Failed call to GetCAProperty - "
                   "CR_PROP_BASECRL\n");
               goto error;
           }

           // Use the base CRL as needed (not shown).
           // ...

           // Retrieve the delta CRL.
           hr = pCertAdmin2->GetCAProperty(bstrCA, 
                                   CR_PROP_DELTACRL, 
                                   nIndex, 
                                   PROPTYPE_BINARY, 
                                   CR_OUT_BINARY, 
                                   &variant);
           if (FAILED(hr))
           {
               printf("Failed call to GetCAProperty - "
                   "CR_PROP_DELTACRL\n");
               goto error;
           }

           // Use the delta CRL as needed (not shown).
           // ...

       }        
    }
    
    // Processing is finished.

error:

    // Clean up object resources.
    if ( NULL != pCertAdmin2 )
        pCertAdmin2->Release();

    // Free BSTR variables.
    if ( NULL != bstrCA )
        SysFreeString ( bstrCA );

    // Clear the variant.
    VariantClear(&variant);
```



 

 
