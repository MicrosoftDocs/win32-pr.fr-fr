---
title: Authentification des messages
description: Authentification des messages
ms.assetid: 6cb49f6b-e303-4840-9343-9891e75e07a4
keywords:
- Gestionnaire de périphériques Windows Media, authentification des messages
- Gestionnaire de périphériques, authentification des messages
- applications de bureau, authentification des messages
- fournisseurs de services, authentification des messages
- Guide de programmation, authentification des messages
- authentification des messages
- code d’authentification de message (MAC)
- MAC (code d’authentification de message)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14805e2074509e918902aae9eb9e9680ca52a6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511002"
---
# <a name="message-authentication"></a><span data-ttu-id="953a9-111">Authentification des messages</span><span class="sxs-lookup"><span data-stu-id="953a9-111">Message Authentication</span></span>

<span data-ttu-id="953a9-112">L’authentification de message est un processus qui permet aux applications et aux fournisseurs de services de vérifier que les données transmises entre elles n’ont pas été falsifiées.</span><span class="sxs-lookup"><span data-stu-id="953a9-112">Message authentication is a process that enables applications and service providers to verify that data passed between them has not been tampered with.</span></span> <span data-ttu-id="953a9-113">Windows Media Gestionnaire de périphériques permet aux applications et aux fournisseurs de services d’effectuer l’authentification des messages à l’aide de codes d’authentification de message (MACs).</span><span class="sxs-lookup"><span data-stu-id="953a9-113">Windows Media Device Manager allows applications and service providers to perform message authentication by using message authentication codes (MACs).</span></span> <span data-ttu-id="953a9-114">Voici comment fonctionne l’authentification MAC :</span><span class="sxs-lookup"><span data-stu-id="953a9-114">Here is how MAC authentication works:</span></span>

<span data-ttu-id="953a9-115">L’expéditeur de données, généralement le fournisseur de services, passe un ou plusieurs éléments de données par le biais d’une fonction de chiffrement unidirectionnelle qui produit une signature unique, le MAC, pour toutes les données.</span><span class="sxs-lookup"><span data-stu-id="953a9-115">The data sender, usually the service provider, passes one or more pieces of data through a one-way cryptographic function that produces a single signature, the MAC, for all the data.</span></span> <span data-ttu-id="953a9-116">L’expéditeur envoie ensuite tous les éléments signés de données avec le MAC au récepteur (généralement l’application).</span><span class="sxs-lookup"><span data-stu-id="953a9-116">The sender then sends all the signed pieces of data together with the MAC to the receiver (usually the application).</span></span> <span data-ttu-id="953a9-117">Le destinataire transmet les données via la même fonction de chiffrement pour générer un MAC et le compare au MAC qui a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="953a9-117">The receiver passes the data through the same cryptographic function to generate a MAC and compares it to the MAC that was sent.</span></span> <span data-ttu-id="953a9-118">Si le MAC correspond, les données n’ont pas été modifiées.</span><span class="sxs-lookup"><span data-stu-id="953a9-118">If the MAC matches, the data has not been modified.</span></span>

<span data-ttu-id="953a9-119">Pour effectuer l’authentification MAC, l’application ou le fournisseur de services requiert une clé de chiffrement et un certificat correspondant.</span><span class="sxs-lookup"><span data-stu-id="953a9-119">To perform MAC authentication, the application or service provider requires an encryption key and a matching certificate.</span></span> <span data-ttu-id="953a9-120">Pour plus d’informations sur l’emplacement à utiliser, consultez [outils de développement](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="953a9-120">For information on where to get these, see [Tools for Development](tools-for-development.md).</span></span>

<span data-ttu-id="953a9-121">Les étapes suivantes décrivent la manière dont les données sont signées par l’expéditeur et sont ensuite contrôlées par le destinataire.</span><span class="sxs-lookup"><span data-stu-id="953a9-121">The following steps describe how data is signed by the sender, and later checked by the receiver.</span></span> <span data-ttu-id="953a9-122">Dans Windows Media Gestionnaire de périphériques, le fournisseur de services utilise la classe [CSecureChannelServer](csecurechannelserver-class.md) pour générer des Mac, et l’application utilise la classe [CSecureChannelClient](csecurechannelclient-class.md) .</span><span class="sxs-lookup"><span data-stu-id="953a9-122">In Windows Media Device Manager, the service provider uses the [CSecureChannelServer](csecurechannelserver-class.md) class to generate MACs, and the application uses the [CSecureChannelClient](csecurechannelclient-class.md) class.</span></span> <span data-ttu-id="953a9-123">Les deux classes fournissent des fonctions identiques avec des paramètres identiques, donc les étapes suivantes s’appliquent aux deux classes.</span><span class="sxs-lookup"><span data-stu-id="953a9-123">Both classes provide identical functions with identical parameters, so the following steps apply to both classes.</span></span>

<span data-ttu-id="953a9-124">L’expéditeur (en général, le fournisseur de services) :</span><span class="sxs-lookup"><span data-stu-id="953a9-124">The sender (typically the service provider):</span></span>

1.  <span data-ttu-id="953a9-125">Obtient les données à signer.</span><span class="sxs-lookup"><span data-stu-id="953a9-125">Get the data to be signed.</span></span>
2.  <span data-ttu-id="953a9-126">Créez un nouveau handle MAC en appelant **MACInit**.</span><span class="sxs-lookup"><span data-stu-id="953a9-126">Create a new MAC handle by calling **MACInit**.</span></span>
3.  <span data-ttu-id="953a9-127">Ajoutez un élément de données à signer dans le handle en appelant **MACUpdate**.</span><span class="sxs-lookup"><span data-stu-id="953a9-127">Add a piece of data to be signed to the handle by calling **MACUpdate**.</span></span> <span data-ttu-id="953a9-128">Cette fonction accepte le handle créé précédemment, ainsi qu’une partie des données qui doivent être signées.</span><span class="sxs-lookup"><span data-stu-id="953a9-128">This function accepts the previously created handle, plus a piece of data that must be signed.</span></span>
4.  <span data-ttu-id="953a9-129">Répétez l’étape 3 pour chaque élément de données supplémentaire qui doit être signé.</span><span class="sxs-lookup"><span data-stu-id="953a9-129">Repeat step 3 with each additional piece of data that must be signed.</span></span> <span data-ttu-id="953a9-130">Il n’a pas d’importance quant à l’ordre dans lequel les données sont ajoutées au MAC.</span><span class="sxs-lookup"><span data-stu-id="953a9-130">It does not matter in what order data is added to the MAC.</span></span>
5.  <span data-ttu-id="953a9-131">Copiez le MAC du handle vers une nouvelle mémoire tampon d’octets en appelant **MACFinal**.</span><span class="sxs-lookup"><span data-stu-id="953a9-131">Copy the MAC from the handle to a new byte buffer by calling **MACFinal**.</span></span> <span data-ttu-id="953a9-132">Cette fonction accepte le handle MAC et une mémoire tampon que vous allouez, et copie le MAC à partir du handle dans la mémoire tampon fournie.</span><span class="sxs-lookup"><span data-stu-id="953a9-132">This function accepts the MAC handle and a buffer that you allocate, and copies the MAC from the handle into the provided buffer.</span></span>

<span data-ttu-id="953a9-133">Lorsque vous effectuez une authentification MAC, il est important que l’expéditeur et le destinataire présentent les mêmes données dans le MAC.</span><span class="sxs-lookup"><span data-stu-id="953a9-133">When performing MAC authentication, it is important that both the sender and the receiver are putting the same data into the MAC.</span></span> <span data-ttu-id="953a9-134">Pour les méthodes d’application qui fournissent un MAC, en général, tous les paramètres sont inclus dans la valeur MAC (à l’exception du MAC lui-même, bien entendu).</span><span class="sxs-lookup"><span data-stu-id="953a9-134">For the application methods that provide a MAC, typically all parameters are included in the MAC value (except for the MAC itself, of course).</span></span> <span data-ttu-id="953a9-135">Par exemple, considérez la méthode **IWMDMOperation :: TransferObjectData** :</span><span class="sxs-lookup"><span data-stu-id="953a9-135">For example, consider the **IWMDMOperation::TransferObjectData** method:</span></span>

`HRESULT TransferObjectData(BYTE* pData, DWORD* pdwSize, BYTE[WMDM_MAC_LENGTH] abMac);`

<span data-ttu-id="953a9-136">Dans cette méthode, le MAC inclut *pData* et *pdwSize*.</span><span class="sxs-lookup"><span data-stu-id="953a9-136">In this method, the MAC would include *pData* and *pdwSize*.</span></span> <span data-ttu-id="953a9-137">Si vous n’incluez pas les deux paramètres, le MAC que vous créez ne correspondra pas au MAC passé à *abMac*.</span><span class="sxs-lookup"><span data-stu-id="953a9-137">If you do not include both the parameters, the MAC you create will not match the MAC passed to *abMac*.</span></span> <span data-ttu-id="953a9-138">Un fournisseur de services doit veiller à placer tous les paramètres requis dans la méthode d’application dans la valeur MAC.</span><span class="sxs-lookup"><span data-stu-id="953a9-138">A service provider must be sure to put all the required parameters in the application method into the MAC value.</span></span>

<span data-ttu-id="953a9-139">Le code C++ suivant illustre la création d’un MAC dans l’implémentation d’un fournisseur de services de [**IMDSPStorageGlobals :: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber).</span><span class="sxs-lookup"><span data-stu-id="953a9-139">The following C++ code demonstrates creating a MAC in a service provider's implementation of [**IMDSPStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber).</span></span>


```C++
HRESULT CMyDevice::GetSerialNumber(
    PWMDMID pSerialNumber, 
    BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT hr;

    // g_pSecureChannelServer is a global CSecureChannelServer object
    // created earlier.

    // Standard check that the CSecureChannelServer was authenticated previously.
    if ( !(g_pSecureChannelServer->fIsAuthenticated()) )
    {
        return WMDM_E_NOTCERTIFIED;
    }

    // Call a helper function to get the device serial number.
    hr = UtilGetSerialNumber(m_wcsName, pSerialNumber, TRUE);
    if(hr == HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED))
    {
        hr = WMDM_E_NOTSUPPORTED;
    }

    if(hr == S_OK)
    {
        // Create the MAC handle.
        HMAC hMAC;
        hr = g_pSecureChannelServer->MACInit(&hMAC);
        if(FAILED(hr))
            return hr;

        // Add the serial number to the MAC.
        g_pSecureChannelServer->MACUpdate(hMAC, (BYTE*)(pSerialNumber), sizeof(WMDMID));
        if(FAILED(hr))
            return hr;

        // Get the created MAC value from the handle.
        g_pSecureChannelServer->MACFinal(hMAC, abMac);
        if(FAILED(hr))
            return hr;
    }

    return hr;
}
```



<span data-ttu-id="953a9-140">Le récepteur (en général, l’application) :</span><span class="sxs-lookup"><span data-stu-id="953a9-140">The receiver (typically the application):</span></span>

<span data-ttu-id="953a9-141">Si le destinataire n’a pas implémenté l’interface [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) , il doit effectuer les mêmes étapes que l’expéditeur, puis comparer les deux valeurs Mac.</span><span class="sxs-lookup"><span data-stu-id="953a9-141">If the receiver has not implemented the [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) interface, it should perform the same steps as the sender, and then compare the two MAC values.</span></span> <span data-ttu-id="953a9-142">L’exemple de code C++ suivant montre comment une application vérifie le MAC reçu dans un appel à [**IWMDMStorageGlobals :: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) pour s’assurer que le numéro de série n’a pas été falsifié en transit.</span><span class="sxs-lookup"><span data-stu-id="953a9-142">The following C++ code example shows how an application would check the MAC received in a call to [**IWMDMStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) to ensure that the serial number was not tampered with in transit.</span></span>


```C++
//
// Get and verify the serial number.
//
WMDMID serialNumber;
BYTE receivedMAC[WMDM_MAC_LENGTH];
hr = pIWMDMDevice->GetSerialNumber(&serialNumber, receivedMAC);

// Check the MAC to guarantee the serial number has not been tampered with.
if (hr == S_OK)
{
    // Initialize a MAC handle, 
    // add all parameters to the MAC,
    // and retrieve the calculated MAC value.
    // m_pSAC is a global CSecureChannelClient object created earlier.
    HMAC hMAC;
    BYTE calculatedMAC[WMDM_MAC_LENGTH];
    hr = m_pSAC->MACInit(&hMAC);
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACUpdate(hMAC, (BYTE*)(&serialNumber), sizeof(serialNumber));
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACFinal(hMAC, (BYTE*)calculatedMAC);
    if(FAILED(hr))
        return hr;

    // If the two MAC values match, the MAC is authentic. 
    if (memcmp(calculatedMAC, receivedMAC, sizeof(calculatedMAC)) == 0)
    {
        // The MAC is authentic; print the serial number.
        CHAR* serialNumberBuffer = 
            new CHAR[serialNumber.SerialNumberLength + 1];
        ZeroMemory(serialNumberBuffer, 
            (serialNumber.SerialNumberLength + 1) * sizeof(CHAR));
        memcpy(serialNumberBuffer, serialNumber.pID, 
            serialNumber.SerialNumberLength * sizeof(CHAR));
        // TODO: Display the serial number.
        delete serialNumberBuffer;
    }
    else
    {
        // TODO: Display a message indicating that the serial number MAC 
        // does not match.
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="953a9-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="953a9-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="953a9-144">**Utilisation de canaux authentifiés sécurisés**</span><span class="sxs-lookup"><span data-stu-id="953a9-144">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 




