---
description: Mérite du codec
ms.assetid: 4ed594a0-2cc2-40d2-9b5c-dee59916fa1b
title: Mérite du codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ecd177c3c32084a030ce75c15cecd5d4c04fc3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556533"
---
# <a name="codec-merit"></a><span data-ttu-id="8735b-103">Mérite du codec</span><span class="sxs-lookup"><span data-stu-id="8735b-103">Codec Merit</span></span>

<span data-ttu-id="8735b-104">À compter de Windows 7, un Media Foundation codec peut se voir attribuer une valeur *mérite* .</span><span class="sxs-lookup"><span data-stu-id="8735b-104">Starting in Windows 7, a Media Foundation codec can be assigned a *merit* value.</span></span> <span data-ttu-id="8735b-105">Lorsque les codecs sont énumérés, les codecs avec des mérites plus élevés sont préférés par rapport aux codecs avec une valeur plus faible.</span><span class="sxs-lookup"><span data-stu-id="8735b-105">When codecs are enumerated, codecs with higher merit are preferred over codecs with lower merit.</span></span> <span data-ttu-id="8735b-106">Les codecs ayant n’importe quelle valeur mérite sont préférés sur les codecs sans mérite affecté.</span><span class="sxs-lookup"><span data-stu-id="8735b-106">Codecs with any merit value are preferred over codecs without an assigned merit.</span></span> <span data-ttu-id="8735b-107">Pour plus d’informations sur l’énumération des codecs, consultez [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="8735b-107">For details about codec enumeration, see [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span>

<span data-ttu-id="8735b-108">Les valeurs mérite sont attribuées par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8735b-108">Merit values are assigned by Microsoft.</span></span> <span data-ttu-id="8735b-109">Actuellement, seuls les codecs matériels peuvent recevoir une valeur mérite.</span><span class="sxs-lookup"><span data-stu-id="8735b-109">Currently, only hardware codecs are eligible to receive a merit value.</span></span> <span data-ttu-id="8735b-110">Le fournisseur du codec reçoit également un certificat numérique, qui est utilisé pour vérifier la valeur mérite du codec.</span><span class="sxs-lookup"><span data-stu-id="8735b-110">The codec vendor is also issued a digital certificate, which is used to verify the codec's merit value.</span></span> <span data-ttu-id="8735b-111">Pour obtenir un certificat, envoyez une demande par courrier électronique à wmla@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="8735b-111">To obtain a certificate, send an email request to wmla@microsoft.com.</span></span> <span data-ttu-id="8735b-112">Le processus d’obtention d’un certificat consiste à signer une licence et à fournir un ensemble de fichiers d’informations à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8735b-112">The process for obtaining a certificate includes signing a license and providing a set of information files to Microsoft.</span></span>

<span data-ttu-id="8735b-113">La mérite du codec fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="8735b-113">Codec merit works as follows:</span></span>

1.  <span data-ttu-id="8735b-114">Le fournisseur du codec implémente l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8735b-114">The codec vendor implements one of the following:</span></span>
    -   <span data-ttu-id="8735b-115">Un mini-pilote AVStream.</span><span class="sxs-lookup"><span data-stu-id="8735b-115">An AVStream mini-driver.</span></span> <span data-ttu-id="8735b-116">Media Foundation fournit une table MFT de proxy standard pour les pilotes AVStream.</span><span class="sxs-lookup"><span data-stu-id="8735b-116">Media Foundation provides an standard proxy MFT for AVStream drivers.</span></span> <span data-ttu-id="8735b-117">C'est l'option recommandée.</span><span class="sxs-lookup"><span data-stu-id="8735b-117">This is the recommended option.</span></span>
    -   <span data-ttu-id="8735b-118">Une Media Foundation transformation (MFT) qui agit comme un proxy pour le matériel.</span><span class="sxs-lookup"><span data-stu-id="8735b-118">A Media Foundation transform (MFT) that acts as a proxy to the hardware.</span></span> <span data-ttu-id="8735b-119">Pour plus d’informations, consultez [Hardware MFTS](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="8735b-119">For more information, see [Hardware MFTs](hardware-mfts.md).</span></span>
2.  <span data-ttu-id="8735b-120">La valeur mérite du codec est stockée dans le registre pour une recherche rapide.</span><span class="sxs-lookup"><span data-stu-id="8735b-120">The codec's merit value is stored in the registry for quick lookup.</span></span>
3.  <span data-ttu-id="8735b-121">La fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) trie les codecs dans l’ordre de leur mérite.</span><span class="sxs-lookup"><span data-stu-id="8735b-121">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function sorts codecs in order of merit.</span></span> <span data-ttu-id="8735b-122">Les codecs dont les valeurs méritent s’affichent dans la liste derrière les codecs inscrits localement (voir [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), mais avant les autres codecs.</span><span class="sxs-lookup"><span data-stu-id="8735b-122">Codecs with merit values appear in the list behind locally registered codecs (see [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), but ahead of other codecs.</span></span>
4.  <span data-ttu-id="8735b-123">Lorsque la table MFT est créée, le mérite du codec est vérifié à l’aide de l’API de [sortie Protection Manager](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="8735b-123">When the MFT is created, the codec's merit is verified using the [Output Protection Manager](output-protection-manager.md) (OPM) API.</span></span>
5.  <span data-ttu-id="8735b-124">Pour une table MFT de proxy, le codec implémente l’interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) .</span><span class="sxs-lookup"><span data-stu-id="8735b-124">For a proxy MFT, the codec implements the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface.</span></span> <span data-ttu-id="8735b-125">Pour un pilote AVStream, le codec implémente le \_ jeu de propriétés KSPROPSETID OPMVideoOutput.</span><span class="sxs-lookup"><span data-stu-id="8735b-125">For an AVStream driver, the codec implements the KSPROPSETID\_OPMVideoOutput property set.</span></span>

<span data-ttu-id="8735b-126">Le diagramme suivant montre comment la mérite est vérifiée dans les deux cas :</span><span class="sxs-lookup"><span data-stu-id="8735b-126">The following diagram shows how merit is verified in both cases:</span></span>

![Diagramme montrant deux processus : l’un domine par le biais du pilote MFT et du pilote AVStream de Media Foundation proxy, l’autre via une table MFT de proxy personnalisée](images/codecmerit.png)

## <a name="custom-proxy-mft"></a><span data-ttu-id="8735b-128">MFT du proxy personnalisé</span><span class="sxs-lookup"><span data-stu-id="8735b-128">Custom Proxy MFT</span></span>

<span data-ttu-id="8735b-129">Si vous fournissez une table MFT du proxy pour le codec matériel, mettez en œuvre la valeur du codec comme suit :</span><span class="sxs-lookup"><span data-stu-id="8735b-129">If you provide a proxy MFT for the hardware codec, implement the codec merit value as follows:</span></span>

1.  <span data-ttu-id="8735b-130">Implémentez l’interface [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) dans la table MFT.</span><span class="sxs-lookup"><span data-stu-id="8735b-130">Implement the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface in the MFT.</span></span> <span data-ttu-id="8735b-131">L’exemple de code est présenté dans la section suivante de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="8735b-131">Example code is shown in the next section of this topic.</span></span>
2.  <span data-ttu-id="8735b-132">Ajoutez l' [attribut \_ \_ \_ attribut de mérite du codec MFT](mft-codec-merit-attribute.md) au registre comme suit :</span><span class="sxs-lookup"><span data-stu-id="8735b-132">Add the [MFT\_CODEC\_MERIT\_Attribute](mft-codec-merit-attribute.md) attribute to the registry, as follows:</span></span>

    1.  <span data-ttu-id="8735b-133">Appelez [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un nouveau magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="8735b-133">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
    2.  <span data-ttu-id="8735b-134">Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) pour définir l’attribut de [ \_ \_ mérite \_ du codec MFT](mft-codec-merit-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="8735b-134">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to set the [MFT\_CODEC\_MERIT\_Attribute](mft-codec-merit-attribute.md) attribute.</span></span> <span data-ttu-id="8735b-135">La valeur de l’attribut est le mérite affecté au codec.</span><span class="sxs-lookup"><span data-stu-id="8735b-135">The value of the attribute is the codec's assigned merit.</span></span>
    3.  <span data-ttu-id="8735b-136">Appelez [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) pour inscrire la table MFT.</span><span class="sxs-lookup"><span data-stu-id="8735b-136">Call [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) to register the MFT.</span></span> <span data-ttu-id="8735b-137">Transmettez le magasin d’attributs dans le paramètre *pAttributes* .</span><span class="sxs-lookup"><span data-stu-id="8735b-137">Pass the attribute store in the *pAttributes* parameter.</span></span>

3.  <span data-ttu-id="8735b-138">L’application appelle [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="8735b-138">The application calls [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="8735b-139">Cette fonction retourne un tableau de pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , un pour chaque codec qui correspond aux critères d’énumération.</span><span class="sxs-lookup"><span data-stu-id="8735b-139">This function returns an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, one for each codec that matches the enumeration criteria.</span></span>
4.  <span data-ttu-id="8735b-140">L’application appelle [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) pour créer la table MFT.</span><span class="sxs-lookup"><span data-stu-id="8735b-140">The application calls [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to create the MFT.</span></span>
5.  <span data-ttu-id="8735b-141">La méthode [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) appelle la fonction [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) pour vérifier le certificat et la valeur mérite.</span><span class="sxs-lookup"><span data-stu-id="8735b-141">The [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method calls the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function to verify the certificate and the merit value.</span></span>
6.  <span data-ttu-id="8735b-142">La fonction [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) appelle [**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) et envoie une demande d’état d’informations d' [**\_ extraction de \_ codec \_ OPM**](opm-get-codec-info.md) .</span><span class="sxs-lookup"><span data-stu-id="8735b-142">The [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function calls [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) and sends an [**OPM\_GET\_CODEC\_INFO**](opm-get-codec-info.md) status request.</span></span> <span data-ttu-id="8735b-143">Cette demande d’État retourne la valeur mérite attribuée au codec.</span><span class="sxs-lookup"><span data-stu-id="8735b-143">This status request returns the codec's assigned merit value.</span></span> <span data-ttu-id="8735b-144">Si cette valeur ne correspond pas à la valeur de Registre, [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) peut échouer.</span><span class="sxs-lookup"><span data-stu-id="8735b-144">If this value does not match the registry value, [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) may fail.</span></span>

<span data-ttu-id="8735b-145">Le code suivant montre comment ajouter la valeur mérite au registre lorsque vous inscrivez la table MFT :</span><span class="sxs-lookup"><span data-stu-id="8735b-145">The following code shows how to add the merit value to the registry when you register the MFT:</span></span>


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



### <a name="implementing-iopmvideooutput-for-codec-merit"></a><span data-ttu-id="8735b-146">Implémentation de IOPMVideoOutput pour la mérite du codec</span><span class="sxs-lookup"><span data-stu-id="8735b-146">Implementing IOPMVideoOutput for Codec Merit</span></span>

<span data-ttu-id="8735b-147">Le code suivant montre comment implémenter [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pour la mérite du codec.</span><span class="sxs-lookup"><span data-stu-id="8735b-147">The following code shows how to implement [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) for codec merit.</span></span> <span data-ttu-id="8735b-148">Pour une description plus générale de l’API OPM, consultez [sortie Protection Manager](output-protection-manager.md).</span><span class="sxs-lookup"><span data-stu-id="8735b-148">For a more general discussion of the OPM API, see [Output Protection Manager](output-protection-manager.md).</span></span>

> [!Note]  
> <span data-ttu-id="8735b-149">Le code présenté ici n’a pas d’obscurcissement ou d’autres mécanismes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8735b-149">The code shown here has no obfuscation or other security mechanisms.</span></span> <span data-ttu-id="8735b-150">Il est destiné à illustrer l’implémentation de base de la demande d’État et de la négociation OPM.</span><span class="sxs-lookup"><span data-stu-id="8735b-150">It is meant to show the basic implementation of the OPM handshake and status request.</span></span>

 

<span data-ttu-id="8735b-151">Cet exemple suppose que *g \_ TestCert* est un tableau d’octets qui contient la chaîne de certificats du codec et que *g \_ PrivateKey* est un tableau d’octets qui contient la clé privée du certificat :</span><span class="sxs-lookup"><span data-stu-id="8735b-151">This example assumes that *g\_TestCert* is a byte array that contains the codec's certificate chain, and *g\_PrivateKey* is a byte array that contains the private key from the certificate:</span></span>


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



<span data-ttu-id="8735b-152">Dans la méthode [**IOPMVideoOutput :: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) , générez un nombre aléatoire pour le protocole de transfert.</span><span class="sxs-lookup"><span data-stu-id="8735b-152">In the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method, generate a random number for the handshake.</span></span> <span data-ttu-id="8735b-153">Retournez ce numéro et le certificat à l’appelant :</span><span class="sxs-lookup"><span data-stu-id="8735b-153">Return this number and the certificate to the caller:</span></span>


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



<span data-ttu-id="8735b-154">La méthode [**IOPMVideoOutput :: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) termine le protocole de transfert OPM :</span><span class="sxs-lookup"><span data-stu-id="8735b-154">The [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) method completes the OPM handshake:</span></span>


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



<span data-ttu-id="8735b-155">Dans la méthode [**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) , implémentez la demande d’état d' [**informations d’extraction de \_ \_ codec \_ OPM**](opm-get-codec-info.md) .</span><span class="sxs-lookup"><span data-stu-id="8735b-155">In the [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method, implement the [**OPM\_GET\_CODEC\_INFO**](opm-get-codec-info.md) status request.</span></span> <span data-ttu-id="8735b-156">Les données d’entrée sont une structure de [**\_ \_ \_ \_ paramètres d’extraction de codec OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) qui contient le CLSID de votre MFT.</span><span class="sxs-lookup"><span data-stu-id="8735b-156">The input data is an [**OPM\_GET\_CODEC\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) structure that contains the CLSID of your MFT.</span></span> <span data-ttu-id="8735b-157">Les données de sortie sont une structure d' [**\_ \_ \_ \_ informations de codec OPM obten**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) contenant la mérite du codec.</span><span class="sxs-lookup"><span data-stu-id="8735b-157">The output data is an [**OPM\_GET\_CODEC\_INFO\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) structure that contains the codec merit.</span></span>


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



<span data-ttu-id="8735b-158">La méthode [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) doit calculer un code D’AUTHENTIFICATION de message (Mac) à l’aide de l’algorithme OMAC-1 ; consultez [calcul de la valeur OMAC-1](opm-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="8735b-158">The [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method must compute a Message Authentication Code (MAC) using the OMAC-1 algorithm; see [Computing the OMAC-1 Value](opm-example-code.md).</span></span>

<span data-ttu-id="8735b-159">Il n’est pas nécessaire de prendre en charge d’autres demandes d’État OPM.</span><span class="sxs-lookup"><span data-stu-id="8735b-159">It is not necessary to support any other OPM status requests.</span></span>

<span data-ttu-id="8735b-160">Les méthodes [**IOPMVideoOutput :: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) et [**IOPMVideoOutput :: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) ne sont pas requises pour la mérite du codec. elles peuvent donc retourner **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="8735b-160">The [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) and [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) methods are not required for codec merit, so these methods can return **E\_NOTIMPL**.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8735b-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8735b-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8735b-162">Transformations de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8735b-162">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="8735b-163">Écriture d’une table MFT personnalisée</span><span class="sxs-lookup"><span data-stu-id="8735b-163">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 



