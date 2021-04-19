---
description: Cette rubrique contient un exemple de code pour l’utilisation de Output Protection Manager.
ms.assetid: ad2303a0-f3f3-43a0-83eb-023640da2ece
title: Exemple de code OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9883643829815d27725c392e2c4f13f34e816988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518367"
---
# <a name="opm-example-code"></a><span data-ttu-id="17e23-103">Exemple de code OPM</span><span class="sxs-lookup"><span data-stu-id="17e23-103">OPM Example Code</span></span>

<span data-ttu-id="17e23-104">Cette rubrique contient un exemple de code pour l’utilisation de [Output Protection Manager](output-protection-manager.md).</span><span class="sxs-lookup"><span data-stu-id="17e23-104">This topic contains example code for using [Output Protection Manager](output-protection-manager.md).</span></span>

<span data-ttu-id="17e23-105">L’exemple de code de cette rubrique montre comment effectuer le protocole de transfert OPM, envoyer une demande d’État et envoyer une commande OPM.</span><span class="sxs-lookup"><span data-stu-id="17e23-105">The example code in this topic demonstrates how to perform the OPM handshake, send a status request, and send an OPM command.</span></span> <span data-ttu-id="17e23-106">Pour les opérations de chiffrement, le code utilise l’API de chiffrement : Next Generation (CNG).</span><span class="sxs-lookup"><span data-stu-id="17e23-106">For cryptographic operations, the code uses Cryptography API: Next Generation (CNG).</span></span> <span data-ttu-id="17e23-107">L’objectif de cette rubrique est d’illustrer la fonctionnalité OPM, de sorte que les tâches associées au certificat X. 509, telles que l’analyse et la validation du certificat, ne sont pas affichées.</span><span class="sxs-lookup"><span data-stu-id="17e23-107">The focus of this topic is to show OPM functionality, so tasks related to the X.509 certificate, such as parsing and validating the certificate, are not shown.</span></span>

<span data-ttu-id="17e23-108">Les procédures présentées dans cette rubrique sont expliquées plus en détail dans [utilisation de Output Protection Manager](using-output-protection-manager.md).</span><span class="sxs-lookup"><span data-stu-id="17e23-108">The procedures shown in this topic are explained in more detail in [Using Output Protection Manager](using-output-protection-manager.md).</span></span>

-   [<span data-ttu-id="17e23-109">Exécution de la liaison OPM</span><span class="sxs-lookup"><span data-stu-id="17e23-109">Performing the OPM Handshake</span></span>](#performing-the-opm-handshake)
-   [<span data-ttu-id="17e23-110">Envoi d’une demande d’État OPM</span><span class="sxs-lookup"><span data-stu-id="17e23-110">Sending an OPM Status Request</span></span>](#sending-an-opm-status-request)
-   [<span data-ttu-id="17e23-111">Envoi d’une commande OPM</span><span class="sxs-lookup"><span data-stu-id="17e23-111">Sending an OPM Command</span></span>](#sending-an-opm-command)
-   [<span data-ttu-id="17e23-112">Calcul de la valeur OMAC-1</span><span class="sxs-lookup"><span data-stu-id="17e23-112">Computing the OMAC-1 Value</span></span>](#computing-the-omac-1-value)
-   [<span data-ttu-id="17e23-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17e23-113">Related topics</span></span>](#related-topics)

## <a name="performing-the-opm-handshake"></a><span data-ttu-id="17e23-114">Exécution de la liaison OPM</span><span class="sxs-lookup"><span data-stu-id="17e23-114">Performing the OPM Handshake</span></span>

1.  <span data-ttu-id="17e23-115">Après avoir énuméré les appareils OPM et sélectionné une sortie vidéo (non illustrée), la première étape consiste à appeler [**IOPMVideoOutput :: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) pour obtenir la chaîne de certificats X. 509 de l’appareil :</span><span class="sxs-lookup"><span data-stu-id="17e23-115">After enumerating the OPM devices and selecting a video output (not shown), the first step is to call [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) to get the device's X.509 certificate chain:</span></span>

    ```C++
        OPM_RANDOM_NUMBER random;   // Random number from driver.
        ZeroMemory(&random, sizeof(random));

        BYTE *pbCertificate = NULL; // Pointer to a buffer to hold the certificate.
        ULONG cbCertificate = 0;    // Size of the certificate in bytes.

        PUBLIC_KEY_VALUES *pKey = NULL; // The driver's public key.

        // Get the driver's certificate chain + random number
        hr = pVideoOutput->StartInitialization(
            &random, 
            &pbCertificate, 
            &cbCertificate
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Validate the X.509 certificate. (Not shown.)
        hr = ValidateX509Certificate(pbCertificate, cbCertificate);

        if (FAILED(hr))
        {
            goto done;
        }

        // Get the public key from the certificate. (Not shown.)
        hr = GetPublicKeyFromCertificate(
            pbCertificate,
            cbCertificate,
            &pKey
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Load and initialize a CNG provider (Cryptography API: Next Generation)

        BCRYPT_ALG_HANDLE hAlg = 0;

        hr = BCryptOpenAlgorithmProvider(
            &hAlg, 
            BCRYPT_RSA_ALGORITHM, 
            MS_PRIMITIVE_PROVIDER, 
            0
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Import the public key into the CNG provider.

        BCRYPT_KEY_HANDLE hPublicKey = 0;

        // Import the RSA public key.
        hr = ImportRsaPublicKey(hAlg, pKey, &hPublicKey);

        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  <span data-ttu-id="17e23-116">L’application doit valider la chaîne de certificats et récupérer la clé publique du certificat feuille de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="17e23-116">The application must validate the certificate chain and get the public key from the leaf certificate in the chain.</span></span> <span data-ttu-id="17e23-117">Ces étapes ne sont pas indiquées ici.</span><span class="sxs-lookup"><span data-stu-id="17e23-117">Those steps are not shown here.</span></span>
3.  <span data-ttu-id="17e23-118">Une fois que vous disposez de la clé publique, vous pouvez importer la clé dans un fournisseur d’algorithme CNG.</span><span class="sxs-lookup"><span data-stu-id="17e23-118">Once you have the public key, you can import the key into a CNG algorithm provider.</span></span> <span data-ttu-id="17e23-119">Appelez la fonction **BCryptOpenAlgorithmProvider** pour charger le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="17e23-119">Call the **BCryptOpenAlgorithmProvider** function to load the provider.</span></span> <span data-ttu-id="17e23-120">La fonction définie par l’application `ImportRsaPublicKey` importe la clé et retourne un descripteur à la clé importée :</span><span class="sxs-lookup"><span data-stu-id="17e23-120">The application-defined `ImportRsaPublicKey` function imports the key and returns a handle to the imported key:</span></span>
    ```C++
    void ReverseMemCopy(BYTE *pbDest, BYTE const *pbSource, DWORD cb)
    {
        for (DWORD i = 0; i < cb; i++) 
        {
            pbDest[cb - 1 - i] = pbSource[i];
        }
    }
    ```

    

    ```C++
    //------------------------------------------------------------------------
    //
    // ImportRsaPublicKey
    //
    // Converts an RSA public key from an RSAPUBKEY blob into an 
    // BCRYPT_RSAKEY_BLOB and sets the public key on the CNG provider.
    //
    //------------------------------------------------------------------------

    HRESULT ImportRsaPublicKey(
        BCRYPT_ALG_HANDLE hAlg,     // CNG provider
        PUBLIC_KEY_VALUES *pKey,    // Pointer to the RSAPUBKEY blob.
        BCRYPT_KEY_HANDLE *phKey    // Receives a handle the imported public key.
        )
    {
        HRESULT hr = S_OK;

        BYTE *pbPublicKey = NULL;
        DWORD cbKey = 0;

        // Layout of the RSA public key blob:

        //  +----------------------------------------------------------------+
        //  |     BCRYPT_RSAKEY_BLOB    | BE( dwExp ) |   BE( Modulus )      |
        //  +----------------------------------------------------------------+
        //
        //  sizeof(BCRYPT_RSAKEY_BLOB)       cbExp           cbModulus 
        //  <--------------------------><------------><---------------------->
        //
        //   BE = Big Endian Format                                                     

        DWORD cbModulus = (pKey->rsapubkey.bitlen + 7) / 8;
        DWORD dwExp = pKey->rsapubkey.pubexp;
        DWORD cbExp = (dwExp & 0xFF000000) ? 4 :
                      (dwExp & 0x00FF0000) ? 3 :
                      (dwExp & 0x0000FF00) ? 2 : 1;

        BCRYPT_RSAKEY_BLOB *pRsaBlob;
        PBYTE pbCurrent;

        hr = DWordAdd(cbModulus, sizeof(BCRYPT_RSAKEY_BLOB), &cbKey);

        if (FAILED(hr))
        {
            goto done;
        }

        cbKey += cbExp;

        pbPublicKey = (BYTE*)CoTaskMemAlloc(cbKey);
        if (NULL == pbPublicKey) 
        {
            hr = E_OUTOFMEMORY;
            goto done;
        }    
        
        ZeroMemory(pbPublicKey, cbKey);
        pRsaBlob = (BCRYPT_RSAKEY_BLOB *)(pbPublicKey);
        
        // Make the Public Key Blob Header
        pRsaBlob->Magic = BCRYPT_RSAPUBLIC_MAGIC;
        pRsaBlob->BitLength = pKey->rsapubkey.bitlen;
        pRsaBlob->cbPublicExp = cbExp;
        pRsaBlob->cbModulus = cbModulus;
        pRsaBlob->cbPrime1 = 0;
        pRsaBlob->cbPrime2 = 0;

        pbCurrent = (PBYTE)(pRsaBlob + 1);
        
        // Copy pubExp Big Endian 
        ReverseMemCopy(pbCurrent, (PBYTE)&dwExp, cbExp);
        pbCurrent += cbExp;

        // Copy Modulus Big Endian 
        ReverseMemCopy(pbCurrent, pKey->modulus, cbModulus);

        // Set the key.
        hr = BCryptImportKeyPair(
            hAlg, 
            NULL, 
            BCRYPT_RSAPUBLIC_BLOB, 
            phKey,
            (PUCHAR)pbPublicKey,
            cbKey,
            0
            );

    done:
        CoTaskMemFree(pbPublicKey);
        return hr;
    }
    ```

    

4.  <span data-ttu-id="17e23-121">Ensuite, préparez la mémoire tampon qui contient les numéros de séquence de départ et la clé de session AES.</span><span class="sxs-lookup"><span data-stu-id="17e23-121">Next, prepare the buffer that contains the starting sequence numbers and the AES session key.</span></span>
    ```C++
    void CopyAndAdvancePtr(BYTE*& pDest, const BYTE* pSrc, DWORD cb)
    {
        memcpy(pDest, pSrc, cb);
        pDest += cb;
    }
    ```

    

    ```C++
        //--------------------------------------------------------------------
        // Prepare the signature for key exchnage.
        //--------------------------------------------------------------------

        UINT uStatusSeq = 0;     // Status sequence number.
        UINT uCommandSeq = 0;    // Command sequence number.

        OPM_RANDOM_NUMBER AesKey;   // Session key

        // Generate the starting sequence number for queries.
        hr = BCryptGenRandom(
            NULL, 
            (BYTE*)&uStatusSeq, 
            sizeof(UINT), 
            BCRYPT_USE_SYSTEM_PREFERRED_RNG
            );

        if (FAILED(hr))
        {
            goto done;
        }


        // Generate the starting sequence number for commands.
        hr = BCryptGenRandom(
            NULL, 
            (BYTE*)&uCommandSeq, 
            sizeof(UINT), 
            BCRYPT_USE_SYSTEM_PREFERRED_RNG
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Generate the AES session key.
        hr = BCryptGenRandom(
            NULL, 
            (BYTE*)&AesKey, 
            sizeof(AesKey), 
            BCRYPT_USE_SYSTEM_PREFERRED_RNG
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Fill in the initialization structure.
        OPM_ENCRYPTED_INITIALIZATION_PARAMETERS initParams;
        ZeroMemory(&initParams, sizeof(initParams));
        
        // Use a temporary pointer for copying into the array.
        BYTE *pBuffer = &initParams.abEncryptedInitializationParameters[0];

        CopyAndAdvancePtr(pBuffer, random.abRandomNumber, sizeof(random)); // Random number from the friver.
        CopyAndAdvancePtr(pBuffer, AesKey.abRandomNumber, sizeof(AesKey)); // Session key.
        CopyAndAdvancePtr(pBuffer, (BYTE*)&uStatusSeq, sizeof(uStatusSeq));
        CopyAndAdvancePtr(pBuffer, (BYTE*)&uCommandSeq, sizeof(uCommandSeq));
    ```

    

5.  <span data-ttu-id="17e23-122">Chiffrez cette mémoire tampon avec le chiffrement RSAES-OAEP, à l’aide de la clé publique du pilote.</span><span class="sxs-lookup"><span data-stu-id="17e23-122">Encrypt this buffer with RSAES-OAEP encryption, using the driver's public key.</span></span>
    ```C++
        //--------------------------------------------------------------------
        // RSAES-OAEP encrypt the signature. Use SHA2 hashing algorithm.
        //--------------------------------------------------------------------

        PBYTE pbDataIn = &initParams.abEncryptedInitializationParameters[0];
        ULONG cbDataIn = (ULONG)(pBuffer - pbDataIn);  

        DWORD cbOutput = 0;
        DWORD cbDataOut= 0;

        BYTE *pbDataOut = NULL;

        BCRYPT_OAEP_PADDING_INFO paddingInfo;
        ZeroMemory(&paddingInfo, sizeof(paddingInfo));

        paddingInfo.pszAlgId = BCRYPT_SHA512_ALGORITHM;

        //Encrypt the signature.
        hr = BCryptEncrypt(
            hPublicKey,
            (PUCHAR)pbDataIn,
            cbDataIn,
            &paddingInfo,
            NULL,
            0,
            NULL,
            0,
            &cbOutput,
            BCRYPT_PAD_OAEP
            );

        if (FAILED(hr))
        {
            goto done;
        }


        pbDataOut = new (std::nothrow) BYTE[cbOutput];
        if (NULL == pbDataOut) 
        {
            hr = E_OUTOFMEMORY;
            goto done;
        }
        
        hr = BCryptEncrypt(
            hPublicKey,
            (PUCHAR)pbDataIn,
            cbDataIn,
            &paddingInfo,
            NULL,
            0,
            pbDataOut,
            cbOutput,
            &cbDataOut,
            BCRYPT_PAD_OAEP
            );

        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

6.  <span data-ttu-id="17e23-123">Appelez [**IOPMVideoOutput :: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) pour terminer le protocole de transfert.</span><span class="sxs-lookup"><span data-stu-id="17e23-123">Call [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) to complete the handshake.</span></span>
    ```C++
        // Complete the handshake.
        hr = pVideoOutput->FinishInitialization(
            (OPM_ENCRYPTED_INITIALIZATION_PARAMETERS *)pbDataOut
            );

        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

## <a name="sending-an-opm-status-request"></a><span data-ttu-id="17e23-124">Envoi d’une demande d’État OPM</span><span class="sxs-lookup"><span data-stu-id="17e23-124">Sending an OPM Status Request</span></span>

<span data-ttu-id="17e23-125">L’exemple suivant montre comment envoyer la demande d’état de [**\_ type d’obtention de \_ connecteur \_ OPM**](opm-get-connector-type.md) .</span><span class="sxs-lookup"><span data-stu-id="17e23-125">The next example shows how to send the [**OPM\_GET\_CONNECTOR\_TYPE**](opm-get-connector-type.md) status request.</span></span>

1.  <span data-ttu-id="17e23-126">Remplissez une structure [**de \_ \_ \_ paramètres OPM obtenir**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) des informations avec les informations relatives à la demande d’État.</span><span class="sxs-lookup"><span data-stu-id="17e23-126">Fill in an [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure with the information for the status request.</span></span>
    ```C++
        //--------------------------------------------------------------------
        // Prepare the status request structure.
        //--------------------------------------------------------------------

        OPM_GET_INFO_PARAMETERS     StatusInput;
        OPM_REQUESTED_INFORMATION   StatusOutput;

        ZeroMemory(&StatusInput, sizeof(StatusInput));
        ZeroMemory(&StatusOutput, sizeof(StatusOutput));

        hr = BCryptGenRandom(
            NULL, 
            (BYTE*)&(StatusInput.rnRandomNumber), 
            OPM_128_BIT_RANDOM_NUMBER_SIZE, 
            BCRYPT_USE_SYSTEM_PREFERRED_RNG
            );

        if (FAILED(hr))
        {
            goto done;
        }

        StatusInput.guidInformation = OPM_GET_CONNECTOR_TYPE; // Request GUID.
        StatusInput.ulSequenceNumber = uStatusSeq;            // Sequence number.

        //  Sign the request structure, not including the omac field.

        hr = ComputeOMAC(
            AesKey,                                             // Session key.
            (BYTE*)&StatusInput + OPM_OMAC_SIZE,                // Data
            sizeof(OPM_GET_INFO_PARAMETERS) - OPM_OMAC_SIZE,    // Size
            &StatusInput.omac                                   // Receives the OMAC
            );

        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  <span data-ttu-id="17e23-127">Le membre **OMAC** de la structure des paramètres de l' [**extraction des \_ \_ informations \_ de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) est un Mac CBC à clé unique (OMAC) calculé pour le reste de la structure.</span><span class="sxs-lookup"><span data-stu-id="17e23-127">The **omac** member of the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure is a one-key CBC MAC (OMAC) computed for the rest of the structure.</span></span> <span data-ttu-id="17e23-128">La fonction ComputeOMAC (illustrée plus loin) est déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="17e23-128">The ComputeOMAC function (shown later) is declared as follows:</span></span>
    ```C++
    HRESULT ComputeOMAC(
        OPM_RANDOM_NUMBER&  AesKey,     // Session key
        PUCHAR pb,                      // Data
        DWORD cb,                       // Size
        OPM_OMAC *pTag                  // Receives the OMAC
        );
    ```

    

3.  <span data-ttu-id="17e23-129">Appelez [**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) pour envoyer la demande d’État.</span><span class="sxs-lookup"><span data-stu-id="17e23-129">Call [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) to send the status request.</span></span>
    ```C++
        //  Send the status request.
        hr = pVideoOutput->GetInformation(&StatusInput, &StatusOutput);

        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

4.  <span data-ttu-id="17e23-130">Le pilote écrit la réponse à la structure d' [**\_ \_ informations OPM demandée**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) .</span><span class="sxs-lookup"><span data-stu-id="17e23-130">The driver writes the response to the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure.</span></span> <span data-ttu-id="17e23-131">La structure de la réponse comprend une valeur OMAC calculée pour le reste de la structure.</span><span class="sxs-lookup"><span data-stu-id="17e23-131">The response structure includes an OMAC value, computed for the remainder of the structure.</span></span> <span data-ttu-id="17e23-132">Vérifiez cette valeur avant d’approuver les données de réponse :</span><span class="sxs-lookup"><span data-stu-id="17e23-132">Verify this value before trusting the response data:</span></span>
    ```C++
        //--------------------------------------------------------------------
        // Verify the signature.
        //--------------------------------------------------------------------

        OPM_OMAC rgbSignature = { 0 };

        // Calculate our own signature.

        hr = ComputeOMAC(
            AesKey,
            (BYTE*)&StatusOutput + OPM_OMAC_SIZE, 
            sizeof(OPM_REQUESTED_INFORMATION) - OPM_OMAC_SIZE, 
            &rgbSignature
            );

        if (FAILED(hr))
        {
            goto done;
        }

        if (memcmp(StatusOutput.omac.abOMAC, rgbSignature.abOMAC, OPM_OMAC_SIZE))
        {
            // The signature does not match.
            hr = E_FAIL; 
            goto done;
        }

        // Update the sequence number.
        uStatusSeq++;
    ```

    

5.  <span data-ttu-id="17e23-133">Le membre **abRequestedInformation** de la structure d' [**\_ \_ informations demandée par OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) contient les données de réponse.</span><span class="sxs-lookup"><span data-stu-id="17e23-133">The **abRequestedInformation** member of the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure contains the response data.</span></span> <span data-ttu-id="17e23-134">Pour la demande de type de connecteur de l' [**\_ offre \_ \_ OPM**](opm-get-connector-type.md) , les données de réponse se composent d’une structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="17e23-134">For the [**OPM\_GET\_CONNECTOR\_TYPE**](opm-get-connector-type.md) request, the response data consists of a [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span>
    ```C++
        // Examine the response. 
        // The response data is an OPM_STANDARD_INFORMATION structure.

        OPM_STANDARD_INFORMATION StatusInfo;
        ZeroMemory(&StatusInfo, sizeof(StatusInfo));

        ULONG cbLen = min(sizeof(OPM_STANDARD_INFORMATION), StatusOutput.cbRequestedInformationSize);    

        if (cbLen != 0)
        {
            // Copy the repinse into the array.
            CopyMemory((BYTE*)&StatusInfo, StatusOutput.abRequestedInformation, cbLen);
        }
        
        //  Verify the random number.
        if (0!= memcmp(
            (BYTE*)&StatusInfo.rnRandomNumber, 
            (BYTE*)&StatusInput.rnRandomNumber, 
            sizeof(OPM_RANDOM_NUMBER)) 
            ) 
        {
            hr = E_FAIL;
            goto done;
        }    

        // Verify the status of the OPM session.
        if (StatusInfo.ulStatusFlags != OPM_STATUS_NORMAL)
        {
            // Abnormal status
            hr = E_FAIL;
            goto done;
        }    
        
        ULONG ConnectorType = StatusInfo.ulInformation & OPM_BUS_TYPE_MASK;
    ```

    

## <a name="sending-an-opm-command"></a><span data-ttu-id="17e23-135">Envoi d’une commande OPM</span><span class="sxs-lookup"><span data-stu-id="17e23-135">Sending an OPM Command</span></span>

<span data-ttu-id="17e23-136">L’exemple suivant montre comment activer High-Bandwidth protection du contenu numérique (HDCP) en envoyant la commande [**de \_ \_ \_ niveau de protection Set pour OPM**](opm-set-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="17e23-136">The next example shows how to enable High-Bandwidth Digital Content Protection (HDCP) by sending the [**OPM\_SET\_PROTECTION\_LEVEL**](opm-set-protection-level.md) command.</span></span>

1.  <span data-ttu-id="17e23-137">Toutes les commandes OPM utilisent la structure de [**\_ \_ paramètres OPM configure**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) pour les données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="17e23-137">All OPM commands use the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure for input data.</span></span> <span data-ttu-id="17e23-138">Le tableau **abParameters** dans cette structure contient des données spécifiques à la commande.</span><span class="sxs-lookup"><span data-stu-id="17e23-138">The **abParameters** array in this structure contains command-specific data.</span></span> <span data-ttu-id="17e23-139">Pour la commande de [**niveau de \_ protection de Set \_ \_ OPM**](opm-set-protection-level.md) , le tableau **abParameters** contient une structure de [**paramètres de \_ \_ \_ niveau \_ de protection défini par OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) .</span><span class="sxs-lookup"><span data-stu-id="17e23-139">For the [**OPM\_SET\_PROTECTION\_LEVEL**](opm-set-protection-level.md) command, the **abParameters** array contains an [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) structure.</span></span> <span data-ttu-id="17e23-140">Renseignez cette structure comme suit :</span><span class="sxs-lookup"><span data-stu-id="17e23-140">Fill in this structure as follows:</span></span>
    ```C++
        //--------------------------------------------------------------------
        // Prepare the command structure.
        //--------------------------------------------------------------------

        // Data specific to the OPM_SET_PROTECTION_LEVEL command.
        OPM_SET_PROTECTION_LEVEL_PARAMETERS CommandInput;

        ZeroMemory(&CommandInput, sizeof(CommandInput));

        CommandInput.ulProtectionType = OPM_PROTECTION_TYPE_HDCP;   
        CommandInput.ulProtectionLevel = OPM_HDCP_ON;        

        ULONG ulAdditionalParametersSize = 0;
        BYTE* pbAdditionalParameters = NULL;
    ```

    

2.  <span data-ttu-id="17e23-141">Ensuite, renseignez la structure des [**\_ \_ paramètres de configuration OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) et calculez le OMAC.</span><span class="sxs-lookup"><span data-stu-id="17e23-141">Next, fill in the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure and compute the OMAC.</span></span>
    ```C++
        // Common command parameters
        OPM_CONFIGURE_PARAMETERS Command;
        ZeroMemory(&Command, sizeof(Command));

        Command.guidSetting = OPM_SET_PROTECTION_LEVEL;
        Command.ulSequenceNumber = uCommandSeq;
        Command.cbParametersSize = sizeof(OPM_SET_PROTECTION_LEVEL_PARAMETERS);
        CopyMemory(&Command.abParameters[0], (BYTE*)&CommandInput, Command.cbParametersSize);

        //  Sign the command structure, not including the omac field.
        hr = ComputeOMAC(
            AesKey,
            (BYTE*)&Command + OPM_OMAC_SIZE, 
            sizeof(OPM_CONFIGURE_PARAMETERS) - OPM_OMAC_SIZE,
            &Command.omac
            );

        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

3.  <span data-ttu-id="17e23-142">Pour envoyer la commande, appelez [**IOPMVideoOutput :: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span><span class="sxs-lookup"><span data-stu-id="17e23-142">To send the command, call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span></span> <span data-ttu-id="17e23-143">N’oubliez pas d’incrémenter le numéro de séquence de commande après chaque commande.</span><span class="sxs-lookup"><span data-stu-id="17e23-143">Remember to increment the command sequence number after each command.</span></span>
    ```C++
        //  Send the command.
        hr = pVideoOutput->Configure(
            &Command, 
            0,      // Size of additional command data.
            NULL    // Additional command data.
            );

        if (FAILED(hr))
        {
            goto done;
        }

        //  Update the sequence number.
        uCommandSeq++;    
    ```

    

4.  <span data-ttu-id="17e23-144">Pour vérifier que la protection HDCP est activée, envoyez une demande d’état de niveau de protection de l' [**\_ offre \_ \_ \_ OPM**](opm-get-virtual-protection-level.md) (non illustrée).</span><span class="sxs-lookup"><span data-stu-id="17e23-144">To verify that HDCP is enabled, send an [**OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL**](opm-get-virtual-protection-level.md) status request (not shown).</span></span>

## <a name="computing-the-omac-1-value"></a><span data-ttu-id="17e23-145">Calcul de la valeur OMAC-1</span><span class="sxs-lookup"><span data-stu-id="17e23-145">Computing the OMAC-1 Value</span></span>

<span data-ttu-id="17e23-146">Le code suivant montre comment calculer la valeur OMAC-1 utilisée pour signer la commande OPM et les structures de demande.</span><span class="sxs-lookup"><span data-stu-id="17e23-146">The following code shows how to compute the OMAC-1 value that is used to sign the OPM command and request structures.</span></span>


```C++
// Helper functions for some bitwise operations.

#define AES_BLOCKLEN    (16)
#define AES_KEYSIZE_128 (16)

inline void XOR( 
    BYTE *lpbLHS, 
    const BYTE *lpbRHS, 
    DWORD cbSize = AES_BLOCKLEN 
    )
{
    for( DWORD i = 0; i < cbSize; i++ )
    {
        lpbLHS[i] ^= lpbRHS[i];
    }
}

inline void LShift(const BYTE *lpbOpd, BYTE *lpbRes)
{
    for( DWORD i = 0; i < AES_BLOCKLEN; i++ )
    {
        lpbRes[i] = lpbOpd[i] << 1;
        if( i < AES_BLOCKLEN - 1 )
        {
            lpbRes[i] |= ( (unsigned char)lpbOpd[i+1] ) >> 7;
        }
    }
}

//  Generate OMAC1 signature using AES128

HRESULT ComputeOMAC(
    OPM_RANDOM_NUMBER&  AesKey,     // Session key
    PUCHAR pb,                      // Data
    DWORD cb,                       // Size of the data
    OPM_OMAC *pTag                  // Receives the OMAC
    )
{
    HRESULT hr = S_OK;
    BCRYPT_ALG_HANDLE hAlg = NULL;
    BCRYPT_KEY_HANDLE hKey = NULL;
    DWORD cbKeyObject = 0;
    DWORD cbData = 0;
    PBYTE pbKeyObject = NULL;

    PUCHAR Key = (PUCHAR)AesKey.abRandomNumber;

    struct 
    {
        BCRYPT_KEY_DATA_BLOB_HEADER Header;
        UCHAR Key[AES_KEYSIZE_128];
    } KeyBlob;

    KeyBlob.Header.dwMagic = BCRYPT_KEY_DATA_BLOB_MAGIC;
    KeyBlob.Header.dwVersion = BCRYPT_KEY_DATA_BLOB_VERSION1;
    KeyBlob.Header.cbKeyData = AES_KEYSIZE_128;
    CopyMemory(KeyBlob.Key, Key, sizeof(KeyBlob.Key));

    BYTE rgbLU[OPM_OMAC_SIZE];
    BYTE rgbLU_1[OPM_OMAC_SIZE];
    BYTE rBuffer[OPM_OMAC_SIZE];

    hr = BCryptOpenAlgorithmProvider(
        &hAlg, 
        BCRYPT_AES_ALGORITHM, 
        MS_PRIMITIVE_PROVIDER, 
        0
        );

    //  Get the size needed for the key data
    if (S_OK == hr) 
    {
        hr = BCryptGetProperty(
            hAlg, 
            BCRYPT_OBJECT_LENGTH, 
            (PBYTE)&cbKeyObject, 
            sizeof(DWORD), 
            &cbData, 
            0
            );
    }

    //  Allocate the key data object
    if (S_OK == hr) 
    {
        pbKeyObject = new (std::nothrow) BYTE[cbKeyObject];
        if (NULL == pbKeyObject) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    //  Set to CBC chain mode
    if (S_OK == hr) 
    {
        hr = BCryptSetProperty(
            hAlg, 
            BCRYPT_CHAINING_MODE, 
            (PBYTE)BCRYPT_CHAIN_MODE_CBC, 
            sizeof(BCRYPT_CHAIN_MODE_CBC), 
            0
            );
    }

    //  Set the key
    if (S_OK == hr) 
    {
        hr = BCryptImportKey(hAlg, NULL, BCRYPT_KEY_DATA_BLOB, &hKey, 
            pbKeyObject, cbKeyObject, (PUCHAR)&KeyBlob, sizeof(KeyBlob), 0);
    }

    //  Encrypt 0s
    if (S_OK == hr) 
    {
        DWORD cbBuffer = sizeof(rBuffer);
        ZeroMemory(rBuffer, sizeof(rBuffer));

        hr = BCryptEncrypt(hKey, rBuffer, cbBuffer, NULL, NULL, 0, 
            rBuffer, sizeof(rBuffer), &cbBuffer, 0);
    }

    //  Compute OMAC1 parameters
    if (S_OK == hr)
    {
        const BYTE bLU_ComputationConstant = 0x87;
        LPBYTE pbL = rBuffer;

        LShift( pbL, rgbLU );
        if( pbL[0] & 0x80 )
        {
            rgbLU[OPM_OMAC_SIZE - 1] ^= bLU_ComputationConstant;
        }
        LShift( rgbLU, rgbLU_1 );
        if( rgbLU[0] & 0x80 )
        {
            rgbLU_1[OPM_OMAC_SIZE - 1] ^= bLU_ComputationConstant;
        }
    }

    //  Generate the hash. 
    if (S_OK == hr) 
    {
        // Redo the key to restart the CBC.

        BCryptDestroyKey(hKey);
        hKey = NULL;

        hr = BCryptImportKey(hAlg, NULL, BCRYPT_KEY_DATA_BLOB, &hKey,
            pbKeyObject, cbKeyObject, (PUCHAR)&KeyBlob, sizeof(KeyBlob), 0);
    }

    if (S_OK == hr) 
    {
        PUCHAR pbDataInCur = pb;
        cbData = cb;
        do
        {
            DWORD cbBuffer = 0;

            if (cbData > OPM_OMAC_SIZE) 
            {
                CopyMemory( rBuffer, pbDataInCur, OPM_OMAC_SIZE );

                hr = BCryptEncrypt(hKey, rBuffer, sizeof(rBuffer), NULL, 
                    NULL, 0, rBuffer, sizeof(rBuffer), &cbBuffer, 0);

                pbDataInCur += OPM_OMAC_SIZE;
                cbData -= OPM_OMAC_SIZE;
            }
            else 
            {   
                if (cbData == OPM_OMAC_SIZE)
                {
                    CopyMemory(rBuffer, pbDataInCur, OPM_OMAC_SIZE);
                    XOR(rBuffer, rgbLU);
                }
                else 
                {
                    ZeroMemory( rBuffer, OPM_OMAC_SIZE );
                    CopyMemory( rBuffer, pbDataInCur, cbData );
                    rBuffer[ cbData ] = 0x80;

                    XOR(rBuffer, rgbLU_1);
                }

                hr = BCryptEncrypt(hKey, rBuffer, sizeof(rBuffer), NULL, NULL, 
                    0, (PUCHAR)pTag->abOMAC, OPM_OMAC_SIZE, &cbBuffer, 0);

                cbData = 0;
            }
                
        } while( S_OK == hr && cbData > 0 );
    }

    //  Clean up
    if (hKey)
    {
        BCryptDestroyKey(hKey);
    }
    if (hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg, 0);
    }
    delete [] pbKeyObject;
    return hr;
}
```



<span data-ttu-id="17e23-147">L’algorithme OMAC-1 est décrit en détail dans <https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html> .</span><span class="sxs-lookup"><span data-stu-id="17e23-147">The OMAC-1 algorithm is described in detail at <https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html>.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17e23-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17e23-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17e23-149">Gestionnaire de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="17e23-149">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



