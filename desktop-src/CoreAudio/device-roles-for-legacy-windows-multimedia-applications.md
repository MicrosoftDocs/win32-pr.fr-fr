---
description: rôles d’appareil pour les Applications multimédias héritées Windows
ms.assetid: 54dcaa0e-2652-406d-ba24-c8885924acc6
title: rôles d’appareil pour les Applications multimédias héritées Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a4ad6728659e4c865aed773575268844fe330e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114998"
---
# <a name="device-roles-for-legacy-windows-multimedia-applications"></a>rôles d’appareil pour les Applications multimédias héritées Windows

> [!Note]  
> L’API MMDevice prend en charge les rôles d’appareil. toutefois, l’interface utilisateur de Windows Vista n’implémente pas la prise en charge de cette fonctionnalité. La prise en charge de l’interface utilisateur pour les rôles d’appareil peut être implémentée dans une future version de Windows. pour plus d’informations, consultez [rôles d’appareil dans Windows Vista](device-roles-in-windows-vista.md).

 

les fonctions **waveOutXxx** et **waveInXxx** multimédias Windows héritées ne permettent pas à une application de sélectionner l’appareil de [point de terminaison audio](audio-endpoint-devices.md) que l’utilisateur a affecté à un [rôle d’appareil](device-roles.md)particulier. toutefois, dans Windows Vista, les api audio de base peuvent être utilisées conjointement avec une application multimédia Windows pour activer la sélection des appareils en fonction du rôle de l’appareil. Par exemple, à l’aide de l' [API MMDevice](mmdevice-api.md), une application **waveOutXxx** peut identifier l’appareil de point de terminaison audio qui est affecté à un rôle, identifier l’appareil de sortie de forme d’onde correspondant et appeler la fonction **waveOutOpen** pour ouvrir une instance de l’appareil. pour plus d’informations sur **waveOutXxx** et **waveInXxx**, consultez la documentation SDK Windows.

L’exemple de code suivant montre comment obtenir l’ID de périphérique de la forme d’onde pour le périphérique de point de terminaison de rendu affecté à un rôle d’appareil particulier :


```C++
//-----------------------------------------------------------
// This function gets the waveOut ID of the audio endpoint
// device that is currently assigned to the specified device
// role. The caller can use the waveOut ID to open the
// waveOut device that corresponds to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetWaveOutId(ERole role, int *pWaveOutId)
{
    HRESULT hr;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    WCHAR *pstrEndpointIdKey = NULL;
    WCHAR *pstrEndpointId = NULL;

    if (pWaveOutId == NULL)
    {
        return E_POINTER;
    }

    // Create an audio endpoint device enumerator.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get the audio endpoint device that the user has
    // assigned to the specified device role.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    // Get the endpoint ID string of the audio endpoint device.
    hr = pDevice->GetId(&pstrEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Get the size of the endpoint ID string.
    size_t  cbEndpointIdKey;

    hr = StringCbLength(pstrEndpointIdKey,
                        STRSAFE_MAX_CCH * sizeof(WCHAR),
                        &cbEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Include terminating null in string size.
    cbEndpointIdKey += sizeof(WCHAR);

    // Allocate a buffer for a second string of the same size.
    pstrEndpointId = (WCHAR*)CoTaskMemAlloc(cbEndpointIdKey);
    if (pstrEndpointId == NULL)
    {
        EXIT_ON_ERROR(hr = E_OUTOFMEMORY)
    }

    // Each for-loop iteration below compares the endpoint ID
    // string of the audio endpoint device to the endpoint ID
    // string of an enumerated waveOut device. If the strings
    // match, then we've found the waveOut device that is
    // assigned to the specified device role.
    int waveOutId;
    int cWaveOutDevices = waveOutGetNumDevs();

    for (waveOutId = 0; waveOutId < cWaveOutDevices; waveOutId++)
    {
        MMRESULT mmr;
        size_t cbEndpointId;

        // Get the size (including the terminating null) of
        // the endpoint ID string of the waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEIDSIZE,
                             (DWORD_PTR)&cbEndpointId, NULL);
        if (mmr != MMSYSERR_NOERROR ||
            cbEndpointIdKey != cbEndpointId)  // do sizes match?
        {
            continue;  // not a matching device
        }

        // Get the endpoint ID string for this waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEID,
                             (DWORD_PTR)pstrEndpointId,
                             cbEndpointId);
        if (mmr != MMSYSERR_NOERROR)
        {
            continue;
        }

        // Check whether the endpoint ID string of this waveOut
        // device matches that of the audio endpoint device.
        if (lstrcmpi(pstrEndpointId, pstrEndpointIdKey) == 0)
        {
            *pWaveOutId = waveOutId;  // found match
            hr = S_OK;
            break;
        }
    }

    if (waveOutId == cWaveOutDevices)
    {
        // We reached the end of the for-loop above without
        // finding a waveOut device with a matching endpoint
        // ID string. This behavior is quite unexpected.
        hr = E_UNEXPECTED;
    }

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    CoTaskMemFree(pstrEndpointIdKey);  // NULL pointer okay
    CoTaskMemFree(pstrEndpointId);
    return hr;
}
```



Dans l’exemple de code précédent, la fonction GetWaveOutId accepte un rôle d’appareil (eConsole, eMultimedia ou eCommunications) comme paramètre d’entrée. Le deuxième paramètre est un pointeur par l’intermédiaire duquel la fonction écrit l’ID de périphérique de la forme d’onde pour le périphérique de sortie de forme d’onde affecté au rôle spécifié. L’application peut ensuite appeler **waveOutOpen** avec cet ID pour ouvrir l’appareil.

La boucle principale de l’exemple de code précédent contient deux appels à la fonction **waveOutMessage** . Le premier appel envoie un \_ message DRV QUERYFUNCTIONINSTANCEIDSIZE pour récupérer la taille, en octets, de la [chaîne d’ID de point de terminaison](endpoint-id-strings.md) de l’appareil de forme d’onde identifiée par le paramètre *waveOutId* . (La chaîne ID du point de terminaison identifie le périphérique de point de terminaison audio sous-jacent de l’abstraction de l’appareil de forme d’onde.) La taille signalée par cet appel comprend l’espace pour le caractère null de fin à la fin de la chaîne. Le programme peut utiliser les informations de taille pour allouer une mémoire tampon suffisamment grande pour contenir l’intégralité de la chaîne d’ID de point de terminaison.

Le deuxième appel à **waveOutMessage** envoie un \_ message QUERYFUNCTIONINSTANCEID DRV pour récupérer la chaîne d’ID d’appareil de l’appareil de sortie Waveform. L’exemple de code compare cette chaîne à la chaîne d’ID de périphérique de l’appareil de point de terminaison audio avec le rôle d’appareil spécifié. Si les chaînes correspondent, la fonction écrit l’ID de périphérique de la forme d’onde à l’emplacement désigné par le paramètre *pWaveOutId*. L’appelant peut utiliser cet ID pour ouvrir l’appareil de sortie de forme d’onde qui a le rôle d’appareil spécifié.

Windows Vista prend en charge les \_ messages DRV QUERYFUNCTIONINSTANCEIDSIZE et DRV \_ QUERYFUNCTIONINSTANCEID. ils ne sont pas pris en charge dans les versions antérieures de Windows, y compris Windows Server 2003, Windows XP et Windows 2000.

La fonction de l’exemple de code précédent obtient l’ID de périphérique de la forme d’onde pour un périphérique de rendu, mais, avec quelques modifications, il peut être adapté pour obtenir l’ID de périphérique de la forme d’onde pour un périphérique de capture. L’application peut ensuite appeler **waveInOpen** avec cet ID pour ouvrir l’appareil. Pour modifier l’exemple de code précédent afin d’obtenir l’ID de périphérique de la forme d’onde pour le périphérique de point de terminaison de capture audio qui est affecté à un rôle particulier, procédez comme suit :

-   Remplacez tous les appels de fonction **waveOutXxx** de l’exemple précédent par les appels de fonction **waveInXxx** correspondants.
-   Remplacez le type de handle HWAVEOUT par HWAVEIN.
-   Remplacez la constante d’énumération [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) ERender par eCapture.

dans Windows Vista, les fonctions **waveOutOpen** et **waveInOpen** attribuent toujours les flux audio qu’ils créent à la session par défaut : la session spécifique au processus qui est identifiée par la valeur guid de la session guid \_ NULL.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interopérabilité avec les API audio héritées](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



