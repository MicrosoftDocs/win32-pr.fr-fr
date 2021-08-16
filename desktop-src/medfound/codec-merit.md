---
description: Mérite du codec
ms.assetid: 4ed594a0-2cc2-40d2-9b5c-dee59916fa1b
title: Mérite du codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56112942aa8378b2016616d0e090e17eb7225ca27b363c96e37eb7cccb6286e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065121"
---
# <a name="codec-merit"></a>Mérite du codec

à partir de Windows 7, un codec Media Foundation peut se voir attribuer une valeur *mérite* . Lorsque les codecs sont énumérés, les codecs avec des mérites plus élevés sont préférés par rapport aux codecs avec une valeur plus faible. Les codecs ayant n’importe quelle valeur mérite sont préférés sur les codecs sans mérite affecté. Pour plus d’informations sur l’énumération des codecs, consultez [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).

Les valeurs mérite sont attribuées par Microsoft. Actuellement, seuls les codecs matériels peuvent recevoir une valeur mérite. Le fournisseur du codec reçoit également un certificat numérique, qui est utilisé pour vérifier la valeur mérite du codec. Pour obtenir un certificat, envoyez une demande par courrier électronique à wmla@microsoft.com . Le processus d’obtention d’un certificat consiste à signer une licence et à fournir un ensemble de fichiers d’informations à Microsoft.

La mérite du codec fonctionne comme suit :

1.  Le fournisseur du codec implémente l’un des éléments suivants :
    -   Un mini-pilote AVStream. Media Foundation fournit une table MFT de proxy standard pour les pilotes AVStream. C'est l'option recommandée.
    -   Une Media Foundation transformation (MFT) qui agit comme un proxy pour le matériel. Pour plus d’informations, consultez [Hardware MFTS](hardware-mfts.md).
2.  La valeur mérite du codec est stockée dans le registre pour une recherche rapide.
3.  La fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) trie les codecs dans l’ordre de leur mérite. Les codecs dont les valeurs méritent s’affichent dans la liste derrière les codecs inscrits localement (voir [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), mais avant les autres codecs.
4.  Lorsque la table MFT est créée, le mérite du codec est vérifié à l’aide de l’API de [sortie Protection Manager](output-protection-manager.md) (OPM).
5.  Pour une table MFT de proxy, le codec implémente l’interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) . Pour un pilote AVStream, le codec implémente le \_ jeu de propriétés KSPROPSETID OPMVideoOutput.

Le diagramme suivant montre comment la mérite est vérifiée dans les deux cas :

![Diagramme montrant deux processus : l’un domine par le biais du pilote MFT et du pilote AVStream de Media Foundation proxy, l’autre via une table MFT de proxy personnalisée](images/codecmerit.png)

## <a name="custom-proxy-mft"></a>MFT du proxy personnalisé

Si vous fournissez une table MFT du proxy pour le codec matériel, mettez en œuvre la valeur du codec comme suit :

1.  Implémentez l’interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) dans la table MFT. L’exemple de code est présenté dans la section suivante de cette rubrique.
2.  Ajoutez l' [attribut \_ \_ \_ attribut de mérite du codec MFT](mft-codec-merit-attribute.md) au registre comme suit :

    1.  Appelez [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un nouveau magasin d’attributs.
    2.  Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) pour définir l’attribut de [ \_ \_ mérite \_ du codec MFT](mft-codec-merit-attribute.md) . La valeur de l’attribut est le mérite affecté au codec.
    3.  Appelez [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) pour inscrire la table MFT. Transmettez le magasin d’attributs dans le paramètre *pAttributes* .

3.  L’application appelle [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). Cette fonction retourne un tableau de pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , un pour chaque codec qui correspond aux critères d’énumération.
4.  L’application appelle [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) pour créer la table MFT.
5.  La méthode [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) appelle la fonction [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) pour vérifier le certificat et la valeur mérite.
6.  La fonction [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) appelle [**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) et envoie une demande d’état d’informations d' [**\_ extraction de \_ codec \_ OPM**](opm-get-codec-info.md) . Cette demande d’État retourne la valeur mérite attribuée au codec. Si cette valeur ne correspond pas à la valeur de Registre, [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) peut échouer.

Le code suivant montre comment ajouter la valeur mérite au registre lorsque vous inscrivez la table MFT :


```C++
// Shows how to register an MFT with a merit value.

HRESULT RegisterMFTWithMerit()
{
    // The following media types would apply to an H.264 decoder, 
    // and are used here as an example.

    MFT_REGISTER_TYPE_INFO aDecoderInputTypes[] = 
    {
        { MFMediaType_Video, MFVideoFormat_H264 },
    };

    MFT_REGISTER_TYPE_INFO aDecoderOutputTypes[] = 
    {
        { MFMediaType_Video, MFVideoFormat_RGB32 }
    };
    
    // Create an attribute store to hold the merit attribute.
    HRESULT hr = S_OK;
    IMFAttributes *pAttributes = NULL;

    hr = MFCreateAttributes(&pAttributes, 1);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MFT_CODEC_MERIT_Attribute, 
            DECODER_MERIT   // Use the codec's assigned merit value.
            );
    }

    // Register the decoder for MFTEnum(Ex).
    if (SUCCEEDED(hr))
    {
        hr = MFTRegister(
            CLSID_MPEG1SampleDecoder,                   // CLSID
            MFT_CATEGORY_VIDEO_DECODER,                 // Category
            const_cast<LPWSTR>(SZ_DECODER_NAME),        // Friendly name
            0,                                          // Flags
            ARRAYSIZE(aDecoderInputTypes),              // Number of input types
            aDecoderInputTypes,                         // Input types
            ARRAYSIZE(aDecoderOutputTypes),             // Number of output types
            aDecoderOutputTypes,                        // Output types
            pAttributes                                 // Attributes 
            );
    }

    SafeRelease(&pAttributes);
    return hr;
}
```



### <a name="implementing-iopmvideooutput-for-codec-merit"></a>Implémentation de IOPMVideoOutput pour la mérite du codec

Le code suivant montre comment implémenter [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pour la mérite du codec. Pour une description plus générale de l’API OPM, consultez [sortie Protection Manager](output-protection-manager.md).

> [!Note]  
> Le code présenté ici n’a pas d’obscurcissement ou d’autres mécanismes de sécurité. Il est destiné à illustrer l’implémentation de base de la demande d’État et de la négociation OPM.

 

Cet exemple suppose que *g \_ TestCert* est un tableau d’octets qui contient la chaîne de certificats du codec et que *g \_ PrivateKey* est un tableau d’octets qui contient la clé privée du certificat :


```C++
// Byte array that contains the codec's certificate.

const BYTE g_TestCert[] =
{
    // ... (certificate not shown)
```




```C++
// Byte array that contains the private key from the certificate.

const BYTE g_PrivateKey[] = 
{
    // .... (key not shown)
```



Dans la méthode [**IOPMVideoOutput :: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) , générez un nombre aléatoire pour le protocole de transfert. Retournez ce numéro et le certificat à l’appelant :


```C++
STDMETHODIMP CodecMerit::StartInitialization(
    OPM_RANDOM_NUMBER *prnRandomNumber,
    BYTE **ppbCertificate,
    ULONG *pulCertificateLength
    )
{
    HRESULT hr = S_OK;

    DWORD cbCertificate = sizeof(g_TestCert);
    const BYTE *pCertificate = g_TestCert;

    // Generate the random number for the OPM handshake.
    hr = BCryptGenRandom(
        NULL,  
        (PUCHAR)&m_RandomNumber, 
        sizeof(m_RandomNumber),
        BCRYPT_USE_SYSTEM_PREFERRED_RNG
        );

    // Allocate the buffer to copy the certificate.
    if (SUCCEEDED(hr))
    {
        *ppbCertificate = (PBYTE)CoTaskMemAlloc(cbCertificate);

        if (*ppbCertificate == NULL) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Copy the certificate and the random number.
    if (SUCCEEDED(hr))
    {
        *pulCertificateLength = cbCertificate;
        CopyMemory(*ppbCertificate, pCertificate, cbCertificate);
        *prnRandomNumber = m_RandomNumber;
    }
    return hr;
}
```



La méthode [**IOPMVideoOutput :: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) termine le protocole de transfert OPM :


```C++
STDMETHODIMP CodecMerit::FinishInitialization(
    const OPM_ENCRYPTED_INITIALIZATION_PARAMETERS *pParameters
    )
{
    HRESULT hr = S_OK;
    BCRYPT_ALG_HANDLE hAlg = NULL;
    BCRYPT_KEY_HANDLE hKey = NULL;
    BCRYPT_OAEP_PADDING_INFO paddingInfo = {0};
    DWORD DecryptedLength = 0;
    PBYTE pbDecryptedParams = NULL;

    // The caller should pass the following structure in
    // pParameters:

    typedef struct {
        GUID  guidCOPPRandom;   // Our random number.
        GUID  guidKDI;          // AES signing key.
        DWORD StatusSeqStart;   // Status sequence number.
        DWORD CommandSeqStart;  // Command sequence number.
    } InitParams;

    paddingInfo.pszAlgId = BCRYPT_SHA512_ALGORITHM;

    //  Decrypt the input using the decoder's private key.

    hr = BCryptOpenAlgorithmProvider(
        &hAlg,
        BCRYPT_RSA_ALGORITHM,
        MS_PRIMITIVE_PROVIDER,
        0
        );

    //  Import the private key.
    if (SUCCEEDED(hr))
    {
        hr = BCryptImportKeyPair(
            hAlg,
            NULL,
            BCRYPT_RSAPRIVATE_BLOB,
            &hKey,
            (PUCHAR)g_PrivateKey, //pbData,
            sizeof(g_PrivateKey), //cbData,
            0
            );
    }

    //  Decrypt the input data.

    if (SUCCEEDED(hr))
    {
        hr = BCryptDecrypt(
            hKey,
            (PBYTE)pParameters,
            OPM_ENCRYPTED_INITIALIZATION_PARAMETERS_SIZE,
            &paddingInfo,
            NULL,
            0,
            NULL,
            0,
            &DecryptedLength,
            BCRYPT_PAD_OAEP
            );
    }

    if (SUCCEEDED(hr))
    {
        pbDecryptedParams = new (std::nothrow) BYTE[DecryptedLength];

        if (pbDecryptedParams == NULL) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    if (SUCCEEDED(hr))
    {
         hr = BCryptDecrypt(
             hKey,
             (PBYTE)pParameters,
             OPM_ENCRYPTED_INITIALIZATION_PARAMETERS_SIZE,
             &paddingInfo,
             NULL,
             0,
             pbDecryptedParams,
             DecryptedLength,
             &DecryptedLength,
             BCRYPT_PAD_OAEP
             );
    }

    if (SUCCEEDED(hr))
    {
        InitParams *Params = (InitParams *)pbDecryptedParams;
        
        //  Check the random number.
        if (0 != memcmp(&m_RandomNumber, &Params->guidCOPPRandom, sizeof(m_RandomNumber)))
        {
            hr = E_ACCESSDENIED;
        } 
        else 
        {
            //  Save the key and the sequence numbers.

            CopyMemory(m_AESKey.abRandomNumber, &Params->guidKDI, sizeof(m_AESKey));
            m_StatusSequenceNumber = Params->StatusSeqStart;
            m_CommandSequenceNumber = Params->CommandSeqStart;
        }
    }

    //  Clean up.

    if (hKey)
    {
        BCryptDestroyKey(hKey);
    }
    if (hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg, 0);
    }
    delete [] pbDecryptedParams;

    return hr;
}
```



Dans la méthode [**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) , implémentez la demande d’état d' [**informations d’extraction de \_ \_ codec \_ OPM**](opm-get-codec-info.md) . Les données d’entrée sont une structure de [**\_ \_ \_ \_ paramètres d’extraction de codec OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) qui contient le CLSID de votre MFT. Les données de sortie sont une structure d' [**\_ \_ \_ \_ informations de codec OPM obten**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) contenant la mérite du codec.


```C++
STDMETHODIMP CodecMerit::GetInformation( 
    const OPM_GET_INFO_PARAMETERS *Parameters,
    OPM_REQUESTED_INFORMATION *pRequest
    )
{

    HRESULT hr = S_OK;
    OPM_GET_CODEC_INFO_PARAMETERS *CodecInfoParameters;

    //  Check the MAC.
    OPM_OMAC Tag = { 0 };

    hr = ComputeOMAC(
        m_AESKey, 
        (PBYTE)Parameters + OPM_OMAC_SIZE, 
        sizeof(OPM_GET_INFO_PARAMETERS) - OPM_OMAC_SIZE, 
        &Tag
        );

    if (SUCCEEDED(hr))
    {
        if (0 != memcmp(Tag.abOMAC, &Parameters->omac, OPM_OMAC_SIZE))
        {
            hr = E_ACCESSDENIED;
        }
    }

    // Validate the status sequence number. This must be consecutive
    // from the previous sequence number.

    if (SUCCEEDED(hr))
    {
        if (Parameters->ulSequenceNumber != m_StatusSequenceNumber++)
        {
            hr = E_ACCESSDENIED;
        }
    }

    //  Check the status request.

    if (SUCCEEDED(hr))
    {
        if (Parameters->guidInformation != OPM_GET_CODEC_INFO) 
        {
            hr = E_NOTIMPL;
        }
    }

    //  Check parameters.

    if (SUCCEEDED(hr))
    {
        CodecInfoParameters = (OPM_GET_CODEC_INFO_PARAMETERS *)Parameters->abParameters;

        if (Parameters->cbParametersSize > OPM_GET_INFORMATION_PARAMETERS_SIZE ||
            Parameters->cbParametersSize < sizeof(ULONG) ||
            Parameters->cbParametersSize - sizeof(ULONG) != CodecInfoParameters->cbVerifier
            ) 
        {
            hr = E_INVALIDARG;
        }
    }

    //  The input data should consist of the CLSID of the decoder.

    if (SUCCEEDED(hr))
    {
        CodecInfoParameters = (OPM_GET_CODEC_INFO_PARAMETERS *)Parameters->abParameters;
    
        if (CodecInfoParameters->cbVerifier != sizeof(CLSID) ||
            0 != memcmp(&CLSID_MPEG1SampleDecoder,
                        CodecInfoParameters->Verifier,
                        CodecInfoParameters->cbVerifier)) 
        {
            hr = E_ACCESSDENIED;
        }
    }

    if (SUCCEEDED(hr))
    {
        // Now return the decoder merit to the caller.

        ZeroMemory(pRequest, sizeof(OPM_REQUESTED_INFORMATION));

        OPM_GET_CODEC_INFO_INFORMATION *pInfo = 
            (OPM_GET_CODEC_INFO_INFORMATION *)pRequest->abRequestedInformation;

        pInfo->Merit = DECODER_MERIT;
        pInfo->rnRandomNumber = Parameters->rnRandomNumber;

        pRequest->cbRequestedInformationSize = sizeof(OPM_GET_CODEC_INFO_INFORMATION);

        //  Sign it with the key.

        hr = ComputeOMAC(
            m_AESKey, 
            (PBYTE)pRequest + OPM_OMAC_SIZE, 
            sizeof(OPM_REQUESTED_INFORMATION) - OPM_OMAC_SIZE, 
            &pRequest->omac
            );
    }

    return hr;
}
```



La méthode [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) doit calculer un code D’AUTHENTIFICATION de message (Mac) à l’aide de l’algorithme OMAC-1 ; consultez [calcul de la valeur OMAC-1](opm-example-code.md).

Il n’est pas nécessaire de prendre en charge d’autres demandes d’État OPM.

Les méthodes [**IOPMVideoOutput :: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) et [**IOPMVideoOutput :: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) ne sont pas requises pour la mérite du codec. elles peuvent donc retourner **E \_ NOTIMPL**.


```C++
STDMETHODIMP CodecMerit::COPPCompatibleGetInformation( 
    const OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS *pParameters,
    OPM_REQUESTED_INFORMATION *pRequestedInformation)
{
    return E_NOTIMPL;
}

STDMETHODIMP CodecMerit::Configure( 
    const OPM_CONFIGURE_PARAMETERS *pParameters,
    ULONG ulAdditionalParametersSize,
    const BYTE *pbAdditionalParameters)
{
    return E_NOTIMPL;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[Écriture d’une table MFT personnalisée](writing-a-custom-mft.md)
</dt> </dl>

 

 



