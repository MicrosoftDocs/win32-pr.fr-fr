---
title: Obtention des fonctionnalités de format via IWMDMDevice
description: Obtention des fonctionnalités de format sur les appareils qui prennent en charge uniquement IWMDMDevice
ms.assetid: bff079a1-d192-4e53-9b1d-9ad3b5dcca51
keywords:
- Gestionnaire de périphériques Windows Media, fonctionnalités de l’appareil
- Gestionnaire de périphériques, fonctionnalités de l’appareil
- Guide de programmation, fonctionnalités de l’appareil
- applications de bureau, fonctionnalités de l’appareil
- création d’applications Windows Media Gestionnaire de périphériques, fonctionnalités de l’appareil
- écriture de fichiers sur des appareils, fonctionnalités de l’appareil
- Méthode IWMDMDevice
- Gestionnaire de périphériques Windows Media, méthode IWMDMDevice
- Gestionnaire de périphériques, méthode IWMDMDevice
- Guide de programmation, méthode IWMDMDevice
- applications de bureau, méthode IWMDMDevice
- création d’applications Windows Media Gestionnaire de périphériques, méthode IWMDMDevice
- écriture de fichiers sur des appareils, méthode IWMDMDevice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a923919611b40197b1deed30e781042e008ef41
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2019
ms.locfileid: "104313846"
---
# <a name="getting-format-capabilities-through-iwmdmdevice"></a><span data-ttu-id="849f6-116">Obtention des fonctionnalités de format via IWMDMDevice</span><span class="sxs-lookup"><span data-stu-id="849f6-116">Getting format capabilities through IWMDMDevice</span></span>

<span data-ttu-id="849f6-117">La méthode recommandée pour l’interrogation d’un appareil pour ses fonctionnalités de lecture est [**IWMDMDevice3 :: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span><span class="sxs-lookup"><span data-stu-id="849f6-117">The recommended method for querying a device for its playback capabilities is [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span></span> <span data-ttu-id="849f6-118">Toutefois, si un appareil ne prend pas en charge cette méthode, l’application peut appeler [**IWMDMDevice :: GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) pour récupérer un tableau de formats audio pris en charge en tant que structures [**\_ WAVEFORMATEX**](-waveformatex.md) et formats MIME sous forme de chaînes à partir de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="849f6-118">However, if a device does not support this method, the application instead can call [**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) to retrieve an array of supported audio formats as [**\_WAVEFORMATEX**](-waveformatex.md) structures and MIME formats as strings from the device.</span></span>

<span data-ttu-id="849f6-119">Les étapes suivantes montrent comment une application peut utiliser cette méthode pour interroger un appareil à la recherche de formats pris en charge :</span><span class="sxs-lookup"><span data-stu-id="849f6-119">The following steps show how an application can use this method to query a device for supported formats:</span></span>

1.  <span data-ttu-id="849f6-120">Appelez **GetFormatSupport** pour récupérer des tableaux de formats audio et MIME.</span><span class="sxs-lookup"><span data-stu-id="849f6-120">Call **GetFormatSupport** to retrieve arrays of both audio and mime formats.</span></span>
2.  <span data-ttu-id="849f6-121">Parcourez les formats audio récupérés et examinez chaque structure [**\_ WAVEFORMATEX**](-waveformatex.md) pour essayer de trouver un format audio acceptable.</span><span class="sxs-lookup"><span data-stu-id="849f6-121">Loop through the retrieved audio formats and examine each [**\_WAVEFORMATEX**](-waveformatex.md) structure to try to find an acceptable audio format</span></span>
3.  <span data-ttu-id="849f6-122">Parcourez les chaînes de format MIME récupérées (si nécessaire) pour trouver un type de fichier acceptable.</span><span class="sxs-lookup"><span data-stu-id="849f6-122">Loop through the retrieved MIME format strings (if desired) to find an acceptable file type.</span></span> <span data-ttu-id="849f6-123">Le kit de développement logiciel (SDK) ne définit pas de constantes pour les formats MIME ; vous devez utiliser les valeurs standard de l’industrie (qui se trouvent sur le site Web iana.org).</span><span class="sxs-lookup"><span data-stu-id="849f6-123">The SDK does not define constants for MIME formats; you should use industry standard values (which can be found at the iana.org Web site).</span></span> <span data-ttu-id="849f6-124">Un appareil doit répertorier les types MIME spécifiques qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="849f6-124">A device should list the specific MIME types that it supports.</span></span>

<span data-ttu-id="849f6-125">Le code C++ suivant illustre la récupération des fonctionnalités de format d’un appareil à l’aide de **GetFormatSupport**.</span><span class="sxs-lookup"><span data-stu-id="849f6-125">The following C++ code demonstrates retrieving format capabilities from a device, using **GetFormatSupport**.</span></span>


```C++
// Function to print out device caps for a device 
// that supports only IWMDMDevice.
void CWMDMController::GetCaps(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get all capabilities for audio and mime support.
    _WAVEFORMATEX* pAudioFormats;
    LPWSTR* pMimeFormats;
    UINT numAudioFormats = 0;
    UINT numMimeFormats = 0;
    hr = pDevice->GetFormatSupport(
        &pAudioFormats,
        &numAudioFormats,
        &pMimeFormats,
        &numMimeFormats);
    if (FAILED(hr)) return;

    // Print out audio format data.
    if (numAudioFormats > 0)
    {
        // TODO: Display a banner for the supported audio-format listing.
    }
    else
    {
        // TODO: Display a message indicating that no audio formats are supported.
    }
    for (int i = 0; i < numAudioFormats; i++)
    {
       // TODO: For each valid audio format, display the max channel, 
       // max samples/second, avg. bytes/sec, block alignment, and 
       // max bits/sample values.
    }

    // Print out MIME formats.
    if (numMimeFormats > 0)
        // TODO: Display a banner to precede the MIME format listing.
    else
        // TODO: Display a banner indicating that no MIME formats are supported.
    for (i = 0; i < numMimeFormats; i++)
    {
        // TODO: Display the specified MIME format.
    }
    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="849f6-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="849f6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="849f6-127">**Découverte des fonctionnalités de format des appareils**</span><span class="sxs-lookup"><span data-stu-id="849f6-127">**Discovering Device Format Capabilities**</span></span>](discovering-device-format-capabilities.md)
</dt> <dt>

[<span data-ttu-id="849f6-128">**Obtention des fonctionnalités de format sur les appareils qui prennent en charge IWMDMDevice3**</span><span class="sxs-lookup"><span data-stu-id="849f6-128">**Getting Format Capabilities on Devices That Support IWMDMDevice3**</span></span>](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
</dt> </dl>

 

 




