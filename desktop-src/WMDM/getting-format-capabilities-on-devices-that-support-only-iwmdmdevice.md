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
# <a name="getting-format-capabilities-through-iwmdmdevice"></a>Obtention des fonctionnalités de format via IWMDMDevice

La méthode recommandée pour l’interrogation d’un appareil pour ses fonctionnalités de lecture est [**IWMDMDevice3 :: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability). Toutefois, si un appareil ne prend pas en charge cette méthode, l’application peut appeler [**IWMDMDevice :: GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) pour récupérer un tableau de formats audio pris en charge en tant que structures [**\_ WAVEFORMATEX**](-waveformatex.md) et formats MIME sous forme de chaînes à partir de l’appareil.

Les étapes suivantes montrent comment une application peut utiliser cette méthode pour interroger un appareil à la recherche de formats pris en charge :

1.  Appelez **GetFormatSupport** pour récupérer des tableaux de formats audio et MIME.
2.  Parcourez les formats audio récupérés et examinez chaque structure [**\_ WAVEFORMATEX**](-waveformatex.md) pour essayer de trouver un format audio acceptable.
3.  Parcourez les chaînes de format MIME récupérées (si nécessaire) pour trouver un type de fichier acceptable. Le kit de développement logiciel (SDK) ne définit pas de constantes pour les formats MIME ; vous devez utiliser les valeurs standard de l’industrie (qui se trouvent sur le site Web iana.org). Un appareil doit répertorier les types MIME spécifiques qu’il prend en charge.

Le code C++ suivant illustre la récupération des fonctionnalités de format d’un appareil à l’aide de **GetFormatSupport**.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Découverte des fonctionnalités de format des appareils**](discovering-device-format-capabilities.md)
</dt> <dt>

[**Obtention des fonctionnalités de format sur les appareils qui prennent en charge IWMDMDevice3**](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
</dt> </dl>

 

 




