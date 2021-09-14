---
description: Montre comment demander un certificat d’archivage de clé.
ms.assetid: a09f55c1-fb27-41e7-9a2f-617d2360c02f
title: Demande d’un certificat d’archivage de clé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da1f69338ed4a41986700853ef5d46ee08612e8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416368"
---
# <a name="requesting-a-key-archival-certificate"></a>Demande d’un certificat d’archivage de clé

L’exemple suivant illustre la création et l’envoi d’une [*demande de certificat*](../secgloss/c-gly.md) et la réception du certificat d’archivage de clé résultant. Pour que cet exemple aboutisse, l' [*autorité de certification*](../secgloss/c-gly.md) (ca) qui reçoit la demande de certificat doit être configurée pour l’archivage de clé.

Les étapes suivantes décrivent la création et l’envoi d’une demande de certificat.

**Pour créer et envoyer une demande de certificat**

1.  Récupérez le certificat d’échange de l’autorité de certification à l’aide de la méthode [**ICertRequest2 :: GetCACertificate**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-getcacertificate) .
2.  Spécifiez que le certificat d’échange de l’autorité de certification récupéré est le certificat d’archive de clé à l’aide de la propriété [**ICEnroll4 ::P rivatekeyarchivecertificate**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-get_privatekeyarchivecertificate) .
3.  Créez une demande de certificat CMC à l’aide de la méthode [**ICEnroll4 :: CreateRequest**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-createrequest) .
4.  Envoyez la demande de certificat à une autorité de certification à l’aide de la méthode [**ICertRequest2 :: Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) . L’autorité de certification doit être configurée pour prendre en charge l’archivage de clé.

Les étapes suivantes décrivent comment récupérer le certificat émis à des fins d’archivage de clé.

**Pour récupérer le certificat émis à des fins d’archivage de clé**

1.  Récupérez la réponse complète, y compris le certificat émis, à l’aide de la méthode [**ICertRequest2 :: GetFullResponseProperty**](/windows/desktop/api/Certcli/nf-certcli-icertrequest2-getfullresponseproperty) .
2.  Installez le certificat émis à l’aide de la méthode [**ICEnroll4 :: acceptResponse**](/windows/desktop/api/Xenroll/nf-xenroll-icenroll4-acceptresponse) .

L’exemple suivant illustre la création et l’envoi d’une demande de certificat et la réception du certificat d’archivage de clé résultant.


```C++
// Pointer to interface objects.
ICEnroll4 * pEnroll = NULL;
ICertRequest2 * pRequest = NULL;

// BSTR variables.
BSTR    bstrCACert = NULL;
BSTR    bstrDN = NULL;
BSTR    bstrCertAuth = NULL;
BSTR    bstrReq = NULL;
BSTR    bstrDispMsg = NULL;
BSTR    bstrErrorMsg = NULL;

VARIANT varFullResp;

LONG    lDisp =0;
LONG    lRequestID = 0;
LONG    lStatus = 0;

HRESULT    hr;

// Initialize COM.
hr = CoInitializeEx( NULL, COINIT_APARTMENTTHREADED );
if ( FAILED( hr ) )
{
    printf("Failed CoInitializeEx - [%x]\n", hr);
    goto error;
}

// Create an instance of the Certificate Enrollment object.
hr = CoCreateInstance( CLSID_CEnroll,
                       NULL,
                       CLSCTX_INPROC_SERVER,
                       IID_ICEnroll4,
                       (void **)&pEnroll);
if ( FAILED( hr ) )
{
    printf("Failed CoCreateInstance - pEnroll [%x]\n", hr);
    goto error;
}

// Create an instance of the Certificate Request object.
hr = CoCreateInstance( CLSID_CCertRequest,
                       NULL,
                       CLSCTX_INPROC_SERVER,
                       IID_ICertRequest2,
                       (void **)&pRequest);
if ( FAILED( hr ) )
{
    printf("Failed CoCreateInstance - pRequest [%x]\n", hr);
    goto error;
}

// Allocate the BSTR that represents the certification authority.
// Note the use of '\\' to produce a single '\' in C++.
bstrCertAuth = SysAllocString(L"Server\\CertAuth");
if (NULL == bstrCertAuth)
{
    printf("Failed SysAllocString\n");
    goto error;
}

// Retrieve the CA's exchange certificate.
hr = pRequest->GetCACertificate(TRUE,
                                bstrCertAuth,
                                CR_OUT_BASE64HEADER,
                                &bstrCACert);
if (FAILED(hr))
{
    printf("Failed GetCACertificate [%x]\n", hr);
    goto error;
}

// Specify the retrieved certificate 
// as the key archive certificate.
hr = pEnroll->put_PrivateKeyArchiveCertificate(bstrCACert);
if (FAILED(hr))
{
    printf("put_PrivateKeyArchiveCertificate [%x]\n", hr);
    goto error;
}

// Create the data for the request.
// A user interface or database retrieval could
// be used instead of this example's hard-coded text.
bstrDN = SysAllocString(L"CN=UserName"    // common name
                        L",OU=UserUnit"   // org unit
                        L",O=UserOrg"     // org
                        L",L=UserCity"    // locality
                        L",S=WA"          // state
                        L",C=US");        // country/region
if (NULL == bstrDN)
{
    printf("Failed SysAllocString\n");
    goto error;
}

// Create the certificate request.
hr = pEnroll->createRequest( XECR_CMC,
                             bstrDN, 
                             NULL,
                             &bstrReq );
if ( FAILED( hr ) )
{
    printf("Failed createRequest - [%x]\n", hr);
    goto error;
}

// Submit the certificate request.
hr = pRequest->Submit( CR_IN_CMC,
                       bstrReq,
                       NULL,
                       bstrCertAuth,
                       &lDisp );
if ( FAILED( hr ) )
{
    
    printf("Failed Submit - [%x]\n", hr);  
    goto error;
}

// Evaluate the disposition of the submitted request.
switch (lDisp)
{
    case CR_DISP_ISSUED:
           printf("Certificate was issued.\n");
           break;

    case CR_DISP_ISSUED_OUT_OF_BAND:
    case CR_DISP_INCOMPLETE:
    case CR_DISP_ERROR:
    case CR_DISP_DENIED:
    case CR_DISP_UNDER_SUBMISSION:
    case CR_DISP_REVOKED:
            printf("Certificate was not issued: %d\n", lDisp);
            break;

    default:
            printf("Unexpected disposition: %d\n", lDisp);
            goto error;
}

// Retrieve the request ID.
hr = pRequest->GetRequestId(&lRequestID);
if ( FAILED(hr) )
{
    printf("Failed GetRequestId - [%x]\n", hr);  
    goto error;
}
printf("The request ID is %d\n", lRequestID);

if (CR_DISP_ISSUED != lDisp)
{
    // Provide information about why a certificate 
    // was not issued.
    
    // Retrieve the last status.
    hr = pRequest->GetLastStatus(&lStatus);
    if ( FAILED(hr) )
    {
        printf("Failed GetLastStatus - [%x]\n", hr);  
        goto error;
    }

    // Retrieve the disposition message.
    hr = pRequest->GetDispositionMessage(&bstrDispMsg);
    if ( FAILED(hr) )
    {
        printf("Failed GetDispositionMessage - [%x]\n", hr);  
        goto error;
    }

    // Retrieve the error message.
    hr = pRequest->GetErrorMessageText(lStatus,
                                       CR_GEMT_HRESULT_STRING,
                                       &bstrErrorMsg);
    if ( FAILED(hr) )
    {
        printf("Failed GetErrorMessageText - [%x]\n", hr);  
        goto error;
    }
    
    // Display the information and exit.
    printf("Request ID: %d\nDisposition: %S\nError: %S\n",
           lRequestID,
           bstrDispMsg,
           bstrErrorMsg);
    goto error;
}

// Retrieve the full response.
VariantInit(&varFullResp);
hr = pRequest->GetFullResponseProperty( FR_PROP_FULLRESPONSE,
                                        0,
                                        PROPTYPE_BINARY,
                                        CR_OUT_BASE64,
                                        &varFullResp );
if ( FAILED( hr ) )
{
    printf("Failed GetFullResponseProperty - [%x]\n", hr);
    goto error;
}

// Accept the response.
hr = pEnroll->acceptResponse(varFullResp.bstrVal);
if ( FAILED( hr ) )
{
    printf("Failed AcceptResponse - [%x]\n", hr);
    goto error;
}
else
{
    printf("Successfully completed processing\n");
}

error:

// Done processing.
// Clean up object resources.
if ( NULL != pEnroll )
    pEnroll->Release();
if ( NULL != pRequest )
    pRequest->Release();

// Free BSTR variables.
if ( NULL != bstrCACert )
    SysFreeString ( bstrCACert );
if ( NULL != bstrDN )
    SysFreeString ( bstrDN );
if ( NULL != bstrCertAuth )
    SysFreeString ( bstrCertAuth );
if ( NULL != bstrReq )
    SysFreeString ( bstrReq );
if ( NULL != bstrDispMsg )
    SysFreeString ( bstrDispMsg );
if ( NULL != bstrErrorMsg )
    SysFreeString ( bstrErrorMsg );

// Clear VARIANTS.
VariantClear(&varFullResp);

// Free COM resources.
CoUninitialize();

return hr;
```



 

 
