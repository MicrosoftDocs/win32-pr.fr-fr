---
title: Détermination de l’état de synchronisation des sélections
description: Détermination de l’état de synchronisation des sélections
ms.assetid: 634b659b-c3ae-4957-b17e-18fd92e915be
keywords:
- Lecteur Windows Media, sélections de synchronisation
- Modèle objet du lecteur Windows Media, sélections de synchronisation
- modèle objet, sélections de synchronisation
- Lecteur Windows Media Mobile, sélections de synchronisation
- Contrôle ActiveX du lecteur Windows Media, sélections de synchronisation
- Contrôle ActiveX Windows Media Player Mobile, sélections de synchronisation
- Contrôle ActiveX, sélections de synchronisation
- sélections, synchronisation
- sélections de métafichiers, synchronisation
- Sélections de métafichiers Windows Media, synchronisation
- appareils mobiles, détermination de l’état de sélection de synchronisation
- sélections de synchronisation, état de synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9758cfbb73c698a40d6d4f48e645e57750d8a332
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106517993"
---
# <a name="determining-playlist-synchronization-state"></a><span data-ttu-id="d5677-115">Détermination de l’état de synchronisation des sélections</span><span class="sxs-lookup"><span data-stu-id="d5677-115">Determining Playlist Synchronization State</span></span>

<span data-ttu-id="d5677-116">Le lecteur Windows Media 10 ou version ultérieure utilise l’attribut **SyncState** pour contenir des informations indiquant si un fichier multimédia numérique particulier a été copié sur un appareil mobile et, en cas de défaillance, si la copie a échoué en raison d’une insuffisance de mémoire dans l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d5677-116">Windows Media Player 10 or later uses the **SyncState** attribute to contain information about whether a particular digital media file has been copied to a portable device and, in the case of a failure, whether copying failed because the device did not have enough memory.</span></span>

<span data-ttu-id="d5677-117">L’exemple de code suivant crée une fonction qui récupère ces informations à partir d’un fichier multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="d5677-117">The following example code creates a function that retrieves this information from a digital media file.</span></span> <span data-ttu-id="d5677-118">La fonction accepte les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="d5677-118">The function takes the following parameters:</span></span>

-   <span data-ttu-id="d5677-119">*pMedia*.</span><span class="sxs-lookup"><span data-stu-id="d5677-119">*pMedia*.</span></span> <span data-ttu-id="d5677-120">Pointeur vers une interface **IWMPMedia** qui représente le fichier multimédia numérique à inspecter.</span><span class="sxs-lookup"><span data-stu-id="d5677-120">Pointer to an **IWMPMedia** interface that represents the digital media file to inspect.</span></span>
-   <span data-ttu-id="d5677-121">*lPsIndex*.</span><span class="sxs-lookup"><span data-stu-id="d5677-121">*lPsIndex*.</span></span> <span data-ttu-id="d5677-122">Index de partenariat de l’appareil actuel.</span><span class="sxs-lookup"><span data-stu-id="d5677-122">Partnership index of the current device.</span></span>
-   <span data-ttu-id="d5677-123">*pulOnDevice*.</span><span class="sxs-lookup"><span data-stu-id="d5677-123">*pulOnDevice*.</span></span> <span data-ttu-id="d5677-124">Pointeur vers une variable de **type long** qui reçoit la valeur indiquant si le fichier multimédia numérique a été copié sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d5677-124">Pointer to a **long** variable that receives the value indicating whether the digital media file has been copied to the device.</span></span>
-   <span data-ttu-id="d5677-125">*pulDidNotFit*.</span><span class="sxs-lookup"><span data-stu-id="d5677-125">*pulDidNotFit*.</span></span> <span data-ttu-id="d5677-126">Pointeur vers une variable de **type long** qui reçoit la valeur indiquant si l’opération de copie a échoué parce que l’appareil n’a pas suffisamment de mémoire.</span><span class="sxs-lookup"><span data-stu-id="d5677-126">Pointer to a **long** variable that receives the value indicating whether the copy operation failed because the device did not have enough memory.</span></span>

<span data-ttu-id="d5677-127">Les informations contenues dans l’attribut **SyncState** sont encodées de manière au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="d5677-127">The information contained in the **SyncState** attribute is encoded in a bitwise fashion.</span></span> <span data-ttu-id="d5677-128">Vous pouvez voir comment cette fonction est utilisée dans l’exemple de code dans l' [énumération des éléments multimédias](enumerating-the-media-items.md).</span><span class="sxs-lookup"><span data-stu-id="d5677-128">You can see how this function is used in the example code in [Enumerating the Media Items](enumerating-the-media-items.md).</span></span>


```C++
STDMETHODIMP CSyncSettings::GetPartnershipSyncState(IWMPMedia* pMedia, long lPsIndex, ULONG *pulOnDevice, ULONG *pulDidNotFit)
{
    ATLASSERT(pMedia); 
    ATLASSERT(lPsIndex > 0 && 
              lPsIndex < 17);
    ATLASSERT(pulOnDevice);
    ATLASSERT(pulDidNotFit);
  
    CComVariant varSyncStateVal;   
    CComPtr<IWMPMedia> spMedia(pMedia); 
    CComPtr<IWMPMedia3> spMedia3;     
    HRESULT hr = spMedia.QueryInterface(&spMedia3); 
    ULONG ulSyncState = 0; // Stores the ulVal member of varSyncStateVal. 
    ULONG lLSB = 0; // Represents least significant bit: Did the media fail to copy because it would not fit?
    ULONG lMSB = 0; // Represents most significant bit: Is the media on the device?

    // Calculate the bit shift required to isolate the partnership bit 
    // pair from the SyncState attribute.
    const int iRshift = (lPsIndex - 1) * 2;

    if(SUCCEEDED(hr) && spMedia3)
    {       
        hr = spMedia3->getItemInfoByType(CComBSTR("SyncState"), CComBSTR(""), 0, &varSyncStateVal);
    }

    if(SUCCEEDED(hr) && varSyncStateVal.vt == VT_UI4)
    {   
        // Get the value.
        ulSyncState = varSyncStateVal.ulVal;

        // Shift the bit pair to the rightmost position.
        ulSyncState >>= iRshift; 

        // Mask the rightmost bit pair.
        ulSyncState &= 3;

        // Get the LSB         
        lLSB = ulSyncState & ~2; // Sets the 2E1 bit to zero. 

        // Get the MSB
        ulSyncState >>= 1;
        lMSB = ulSyncState;       
    }

    // Return the bits.
    *pulOnDevice = lMSB;
    *pulDidNotFit = lLSB;

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d5677-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5677-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5677-130">**Interface IWMPMedia**</span><span class="sxs-lookup"><span data-stu-id="d5677-130">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="d5677-131">**IWMPMedia3::getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="d5677-131">**IWMPMedia3::getItemInfoByType**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype)
</dt> <dt>

[<span data-ttu-id="d5677-132">**Gestion des sélections de synchronisation**</span><span class="sxs-lookup"><span data-stu-id="d5677-132">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="d5677-133">**Attribut SyncState**</span><span class="sxs-lookup"><span data-stu-id="d5677-133">**SyncState Attribute**</span></span>](syncstate-attribute.md)
</dt> </dl>

 

 




