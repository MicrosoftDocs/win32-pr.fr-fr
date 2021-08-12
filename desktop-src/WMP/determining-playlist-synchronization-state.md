---
title: Détermination de l’état de synchronisation des sélections
description: Détermination de l’état de synchronisation des sélections
ms.assetid: 634b659b-c3ae-4957-b17e-18fd92e915be
keywords:
- Lecteur Windows Media, sélections de synchronisation
- Lecteur Windows Media modèle objet, sélections de synchronisation
- modèle objet, sélections de synchronisation
- Lecteur Windows Media Mobile, sélections de synchronisation
- contrôle de ActiveX Lecteur Windows Media, sélections de synchronisation
- Lecteur Windows Media contrôle de ActiveX Mobile, sélections de synchronisation
- contrôle de ActiveX, sélections de synchronisation
- sélections, synchronisation
- sélections de métafichiers, synchronisation
- Windows Sélections de métafichiers multimédia, synchronisation
- appareils mobiles, détermination de l’état de sélection de synchronisation
- sélections de synchronisation, état de synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14af59f66d1b21eac00208ecc805f756761256e47a35042694bcd65e6f96558
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579458"
---
# <a name="determining-playlist-synchronization-state"></a>Détermination de l’état de synchronisation des sélections

Lecteur Windows Media 10 ou version ultérieure utilise l’attribut **SyncState** pour contenir des informations indiquant si un fichier multimédia numérique particulier a été copié sur un appareil mobile et, en cas de défaillance, si la copie a échoué parce que l’appareil n’a pas suffisamment de mémoire.

L’exemple de code suivant crée une fonction qui récupère ces informations à partir d’un fichier multimédia numérique. La fonction accepte les paramètres suivants :

-   *pMedia*. Pointeur vers une interface **IWMPMedia** qui représente le fichier multimédia numérique à inspecter.
-   *lPsIndex*. Index de partenariat de l’appareil actuel.
-   *pulOnDevice*. Pointeur vers une variable de **type long** qui reçoit la valeur indiquant si le fichier multimédia numérique a été copié sur l’appareil.
-   *pulDidNotFit*. Pointeur vers une variable de **type long** qui reçoit la valeur indiquant si l’opération de copie a échoué parce que l’appareil n’a pas suffisamment de mémoire.

Les informations contenues dans l’attribut **SyncState** sont encodées de manière au niveau du bit. Vous pouvez voir comment cette fonction est utilisée dans l’exemple de code dans l' [énumération des éléments multimédias](enumerating-the-media-items.md).


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPMedia3::getItemInfoByType**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype)
</dt> <dt>

[**Gestion des sélections de synchronisation**](managing-synchronization-playlists.md)
</dt> <dt>

[**Attribut SyncState**](syncstate-attribute.md)
</dt> </dl>

 

 




