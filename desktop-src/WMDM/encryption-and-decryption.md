---
title: Chiffrement et déchiffrement
description: Chiffrement et déchiffrement
ms.assetid: 6aef4138-0391-4edd-b4fc-d6d0ec3c735b
keywords:
- Gestionnaire de périphériques Windows Media, chiffrement
- Gestionnaire de périphériques, chiffrement
- applications de bureau, chiffrement
- fournisseurs de services, chiffrement
- Guide de programmation, chiffrement
- le chiffrement
- Gestionnaire de périphériques Windows Media, déchiffrement
- Gestionnaire de périphériques, déchiffrement
- applications de bureau, déchiffrement
- fournisseurs de services, déchiffrement
- Guide de programmation, déchiffrement
- déchiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78688c1b4ca9991d8b322c6991de96a51e7e8d22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382660"
---
# <a name="encryption-and-decryption"></a><span data-ttu-id="5eecf-115">Chiffrement et déchiffrement</span><span class="sxs-lookup"><span data-stu-id="5eecf-115">Encryption and Decryption</span></span>

<span data-ttu-id="5eecf-116">Windows Media Gestionnaire de périphériques nécessite le chiffrement des fichiers envoyés entre le fournisseur de services et l’application.</span><span class="sxs-lookup"><span data-stu-id="5eecf-116">Windows Media Device Manager requires encryption of files sent between the service provider and the application.</span></span> <span data-ttu-id="5eecf-117">Cette opération peut être effectuée de deux manières :</span><span class="sxs-lookup"><span data-stu-id="5eecf-117">This can be done in one of two ways:</span></span>

-   <span data-ttu-id="5eecf-118">Si le fournisseur de services prend en charge uniquement [**IMDSPObject :: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) et [**IMDSPObject :: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write), les données doivent être chiffrées et déchiffrées par l’application et le fournisseur de services à l’aide des méthodes [CSecureChannelClient](csecurechannelclient-class.md) et [CSecureChannelServer](csecurechannelserver-class.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="5eecf-118">If the service provider supports only [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) and [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write), the data must be encrypted and decrypted by the application and service provider by using [CSecureChannelClient](csecurechannelclient-class.md) and [CSecureChannelServer](csecurechannelserver-class.md) methods respectively.</span></span>
-   <span data-ttu-id="5eecf-119">Si le fournisseur de services prend en charge [**IMDSPObject2 :: ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) et [**IMDSPObject2 :: WriteOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel), votre application peut éviter l’authentification coûteuse des messages de canal sécurisé.</span><span class="sxs-lookup"><span data-stu-id="5eecf-119">If the service provider supports [**IMDSPObject2::ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) and [**IMDSPObject2::WriteOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel), your application can avoid costly secure channel message authentication.</span></span> <span data-ttu-id="5eecf-120">(Le canal sécurisé est conservé afin que les fournisseurs de services hérités qui n’implémentent pas [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) continuent à fonctionner.)</span><span class="sxs-lookup"><span data-stu-id="5eecf-120">(The secure channel is retained so that legacy service providers that do not implement [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) can still continue to function.)</span></span>

<span data-ttu-id="5eecf-121">L’exigence de chiffrement empêche les applications malveillantes d’obtenir des données transmises entre les composants logiciels et protège également l’intégrité des données envoyées vers ou depuis l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5eecf-121">The encryption requirement prevents malicious applications from obtaining data that is being passed between software components, and also protects the integrity of data being sent to or from the device.</span></span>

<span data-ttu-id="5eecf-122">Les trois méthodes suivantes requièrent le chiffrement ou le déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="5eecf-122">The following three methods require encryption or decryption.</span></span>



| <span data-ttu-id="5eecf-123">Méthode</span><span class="sxs-lookup"><span data-stu-id="5eecf-123">Method</span></span>                                                                          | <span data-ttu-id="5eecf-124">Description</span><span class="sxs-lookup"><span data-stu-id="5eecf-124">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5eecf-125">**IWMDMOperation::TransferObjectData**</span><span class="sxs-lookup"><span data-stu-id="5eecf-125">**IWMDMOperation::TransferObjectData**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) | <span data-ttu-id="5eecf-126">Oeuvre Chiffrement ou déchiffrement, selon que l’application envoie ou reçoit des données.</span><span class="sxs-lookup"><span data-stu-id="5eecf-126">(Application) Encryption or decryption, depending on whether the application is sending or receiving data.</span></span> |
| [<span data-ttu-id="5eecf-127">**IMDSPObject :: lecture**</span><span class="sxs-lookup"><span data-stu-id="5eecf-127">**IMDSPObject::Read**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)                                   | <span data-ttu-id="5eecf-128">(Fournisseur de services) Chiffre.</span><span class="sxs-lookup"><span data-stu-id="5eecf-128">(Service provider) Encryption.</span></span>                                                                             |
| [<span data-ttu-id="5eecf-129">**IMDSPObject :: Write**</span><span class="sxs-lookup"><span data-stu-id="5eecf-129">**IMDSPObject::Write**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)                                 | <span data-ttu-id="5eecf-130">(Fournisseur de services) Déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="5eecf-130">(Service Provider) Decryption.</span></span>                                                                             |



 

<span data-ttu-id="5eecf-131">Le chiffrement et le déchiffrement sont tous deux effectués par des appels de méthode uniques.</span><span class="sxs-lookup"><span data-stu-id="5eecf-131">Encryption and decryption are both done by single method calls.</span></span> <span data-ttu-id="5eecf-132">Le chiffrement est effectué par [**CSecureChannelClient :: EncryptParam**](/previous-versions/bb231587(v=vs.85)) pour les applications ou par [**CSecureChannelServer :: EncryptParam**](/previous-versions/ms868509(v=msdn.10)) pour les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="5eecf-132">Encryption is done by [**CSecureChannelClient::EncryptParam**](/previous-versions/bb231587(v=vs.85)) for applications or by [**CSecureChannelServer::EncryptParam**](/previous-versions/ms868509(v=msdn.10)) for service providers.</span></span> <span data-ttu-id="5eecf-133">Le déchiffrement s’effectue par [**CSecureChannelClient ::D ecryptparam**](/previous-versions/bb231586(v=vs.85)) pour les applications ou [**CSecureChannelServer ::D ecryptparam**](/previous-versions/bb231598(v=vs.85)) pour les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="5eecf-133">Decryption is done by [**CSecureChannelClient::DecryptParam**](/previous-versions/bb231586(v=vs.85)) for applications or [**CSecureChannelServer::DecryptParam**](/previous-versions/bb231598(v=vs.85)) for service providers.</span></span> <span data-ttu-id="5eecf-134">Les paramètres sont identiques entre les méthodes client et serveur.</span><span class="sxs-lookup"><span data-stu-id="5eecf-134">The parameters are identical between the client and server methods.</span></span>

<span data-ttu-id="5eecf-135">Les étapes suivantes montrent comment chiffrer et déchiffrer les données.</span><span class="sxs-lookup"><span data-stu-id="5eecf-135">The following steps show how to encrypt and decrypt data.</span></span> <span data-ttu-id="5eecf-136">(Ces étapes sont importantes uniquement si votre application communique avec un fournisseur de services hérité qui n’implémente pas [IWMDMOperation3 :: TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel).)</span><span class="sxs-lookup"><span data-stu-id="5eecf-136">(These steps are important only if your application communicates with a legacy service provider that does not implement [IWMDMOperation3::TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel).)</span></span>

<span data-ttu-id="5eecf-137">**Chiffrement**</span><span class="sxs-lookup"><span data-stu-id="5eecf-137">**Encryption**</span></span>

1.  <span data-ttu-id="5eecf-138">Créez la clé MAC pour les données chiffrées, comme décrit dans [authentification de message](message-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="5eecf-138">Create the MAC key for the encrypted data, as described in [Message Authentication](message-authentication.md).</span></span>
2.  <span data-ttu-id="5eecf-139">Appelez **EncryptParam** avec les données à chiffrer pour effectuer un chiffrement sur place.</span><span class="sxs-lookup"><span data-stu-id="5eecf-139">Call **EncryptParam** with the data to encrypt, to perform in-place encryption.</span></span>

<span data-ttu-id="5eecf-140">L’exemple de code suivant illustre l’implémentation d’un fournisseur de services de [**IMDSPObject :: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read).</span><span class="sxs-lookup"><span data-stu-id="5eecf-140">The following code example demonstrates a service provider's implementation of [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read).</span></span> <span data-ttu-id="5eecf-141">Cette méthode crée la clé MAC à l’aide des données à chiffrer et de la taille des données, puis les envoie à l’application.</span><span class="sxs-lookup"><span data-stu-id="5eecf-141">This method creates the MAC key using the data to encrypt and the size of the data, and sends them both to the application.</span></span>


```C++
HRESULT CMyStorage::Read(
    BYTE  *pData,
    DWORD *pdwSize,
    BYTE   abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwToRead;         // Bytes to read.
    DWORD    dwRead   = NULL;  // Bytes read.
    BYTE    *pTmpData = NULL;  // Temporary buffer to hold data before 
                               // it is copied to pData.

    // Use a global CSecureChannelServer member to verify that 
    // the client is authenticated.
    if (!(g_pAppSCServer->fIsAuthenticated()))
    {
        return WMDM_E_NOTCERTIFIED;
    }
    

    // Verify that the handle to the file to read is valid.
    if(m_hFile == INVALID_HANDLE_VALUE)
    {
        return E_FAIL;
    }

    // Create a buffer to hold the data read.    
    dwToRead = *pdwSize;
    pTmpData = new BYTE [dwToRead] ;
    if(!pTmpData)
        return E_OUTOFMEMORY;

    // Read data into the temporary buffer.
    if(ReadFile(m_hFile,(LPVOID)pTmpData,dwToRead,&dwRead,NULL)) 
    { 
        *pdwSize = dwRead; 

        if( dwRead )
        {
            // Create a MAC from all the parameters.
            // CORg is a macro that goes to Error label on failure.
            // MAC consists of data and size of data.
            HMAC hMAC;
            
            CORg(g_pAppSCServer->MACInit(&hMAC));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), dwRead));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(DWORD)));
            CORg(g_pAppSCServer->MACFinal(hMAC, abMac));
            
            // Encrypt the data.
            CORg(g_pAppSCServer->EncryptParam(pTmpData, dwRead));
            
            // Copy data from the temporary buffer into the out parameter.
            memcpy(pData, pTmpData, dwRead);
        }
    
        hr = S_OK; 
    }
    else
    { 
        *pdwSize = 0; 

        hr = E_FAIL; 
    }

Error:

    if(pTmpData) 
    {
        delete [] pTmpData;
    }

    return hr;
} 
```



<span data-ttu-id="5eecf-142">**Déchiffrement**</span><span class="sxs-lookup"><span data-stu-id="5eecf-142">**Decryption**</span></span>

1.  <span data-ttu-id="5eecf-143">Appelez **DecryptParam** avec les données à chiffrer pour effectuer un déchiffrement sur place.</span><span class="sxs-lookup"><span data-stu-id="5eecf-143">Call **DecryptParam** with the data to encrypt, to perform in-place decryption.</span></span>
2.  <span data-ttu-id="5eecf-144">Vérifiez la clé MAC pour les données déchiffrées, comme décrit dans [authentification de message](message-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="5eecf-144">Verify the MAC key for the decrypted data, as described in [Message Authentication](message-authentication.md).</span></span>

<span data-ttu-id="5eecf-145">L’exemple de code suivant illustre l’implémentation d’un fournisseur de services de [**IMDSPObject :: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write).</span><span class="sxs-lookup"><span data-stu-id="5eecf-145">The following code example demonstrates a service provider's implementation of [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write).</span></span> <span data-ttu-id="5eecf-146">Cette méthode crée la clé MAC à l’aide des données à chiffrer et de la taille des données, puis les envoie à l’application.</span><span class="sxs-lookup"><span data-stu-id="5eecf-146">This method creates the MAC key using the data to encrypt and the size of the data, and sends them both to the application.</span></span>


```C++
HRESULT CMyStorage::Write(BYTE *pData, DWORD *pdwSize,
                                 BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwWritten = 0;
    BYTE    *pTmpData  = NULL;          // Temporary buffer to hold the 
                                        // data during decryption.
    BYTE     pTempMac[WMDM_MAC_LENGTH]; // Temporary MAC that will be 
                                        // copied into the abMac
                                        // out parameter.

    if( m_hFile == INVALID_HANDLE_VALUE )
    {
        return E_FAIL;
    }

    // Allocate the temporary buffer and copy the encrypted data into it.
    pTmpData = new BYTE [*pdwSize];
    if(!pTmpData)
        return E_OUTOFMEMORY;
    memcpy(pTmpData, pData, *pdwSize);

    // Decrypt the data.
    CHRg(g_pAppSCServer->DecryptParam(pTmpData, *pdwSize));

    // Check the MAC passed to the method. The MAC is built from
    // the data and data size parameters.
    // CORg is a macro that goes to the Error label on failure.
    HMAC hMAC;
    CORg(g_pAppSCServer->MACInit(&hMAC));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), *pdwSize));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(*pdwSize)));
    CORg(g_pAppSCServer->MACFinal(hMAC, pTempMac));

    // If the MAC values don't match, return an error.
    if (memcmp(abMac, pTempMac, WMDM_MAC_LENGTH) != 0)
    {
        hr = WMDM_E_MAC_CHECK_FAILED;
        goto Error;
    }

    // The MAC values matched, so write the decrypted data to a local file.
    if( WriteFile(m_hFile,pTmpData,*pdwSize,&dwWritten,NULL) ) 
    {
        hr = S_OK;
    }
    else 
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    *pdwSize = dwWritten;

Error:

    if( pTmpData )
    {
        delete [] pTmpData;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="5eecf-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5eecf-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eecf-148">**Utilisation de canaux authentifiés sécurisés**</span><span class="sxs-lookup"><span data-stu-id="5eecf-148">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 