---
description: Rôles d’appareil pour les applications DirectSound
ms.assetid: 7d82d67f-aad8-4e5b-ac65-87d75774e613
title: Rôles d’appareil pour les applications DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3829817f8b00c7288aceb8d0b6d418d5793ae580
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950392"
---
# <a name="device-roles-for-directsound-applications"></a>Rôles d’appareil pour les applications DirectSound

> [!Note]  
> L' [API MMDevice](mmdevice-api.md) prend en charge les rôles d’appareil. Toutefois, l’interface utilisateur de Windows Vista n’implémente pas la prise en charge de cette fonctionnalité. La prise en charge de l’interface utilisateur pour les rôles d’appareil peut être implémentée dans une future version de Windows. Pour plus d’informations, consultez [rôles de périphérique dans Windows Vista](device-roles-in-windows-vista.md).

 

L’API DirectSound ne permet pas à une application de sélectionner l’appareil de [point de terminaison audio](audio-endpoint-devices.md) que l’utilisateur a affecté à un [rôle d’appareil](device-roles.md)particulier. Toutefois, dans Windows Vista, les API audio de base peuvent être utilisées conjointement avec une application DirectSound pour activer la sélection d’appareils en fonction du rôle d’appareil. Avec l’aide des API audio de base, l’application peut identifier l’appareil de point de terminaison audio qui est affecté à un rôle particulier, obtenir le GUID de l’appareil DirectSound pour l’appareil de point de terminaison et appeler la fonction **DirectSoundCreate** ou **DirectSoundCaptureCreate** pour créer une instance d’interface **IDirectSound** ou **IDirectSoundCapture** qui encapsule l’appareil de point de terminaison. Pour plus d’informations sur DirectSound, consultez la documentation SDK Windows.

L’exemple de code suivant montre comment obtenir le GUID de l’appareil DirectSound pour le périphérique de rendu ou de capture qui est actuellement affecté à un rôle d’appareil particulier :


```C++
//-----------------------------------------------------------
// Get the DirectSound or DirectSoundCapture device GUID for
// an audio endpoint device. If flow = eRender, the function
// gets the DirectSound device GUID for the rendering device
// with the specified device role. If flow = eCapture, the
// function gets the DirectSoundCapture device GUID for the
// capture device with the specified device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetDirectSoundGuid(EDataFlow flow, ERole role, GUID* pDevGuid)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IPropertyStore *pProps = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    if (pDevGuid == NULL)
    {
        return E_POINTER;
    }

    // Get a device enumerator for the audio endpoint
    // devices in the system.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get the endpoint device with the specified dataflow
    // direction (eRender or eCapture) and device role.
    hr = pEnumerator->GetDefaultAudioEndpoint(flow, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->OpenPropertyStore(STGM_READ, &pProps);
    EXIT_ON_ERROR(hr)

    // Get the DirectSound or DirectSoundCapture device GUID
    // (in WCHAR string format) for the endpoint device.
    hr = pProps->GetValue(PKEY_AudioEndpoint_GUID, &var);
    EXIT_ON_ERROR(hr)

    // Convert the WCHAR string to a GUID structure.
    hr = CLSIDFromString(var.pwszVal, pDevGuid);
    EXIT_ON_ERROR(hr)

Exit:
    PropVariantClear(&var);
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    SAFE_RELEASE(pProps);
    return hr;
}
```



Dans l’exemple de code précédent, la fonction GetDirectSoundGuid accepte un sens de workflow de données (eRender ou eCapture) et un rôle d’appareil (eConsole, eMultimedia ou eCommunications) comme paramètres d’entrée. Le troisième paramètre est un pointeur à travers lequel la fonction écrit un GUID d’appareil que l’application peut fournir comme paramètre d’entrée à la fonction **DirectSoundCreate** ou **DirectSoundCaptureCreate** .

L’exemple de code précédent obtient le GUID de l’appareil DirectSound en procédant comme suit :

-   Création d’une instance d’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) qui représente l’appareil de point de terminaison audio ayant la direction de flux de données et le rôle d’appareil spécifiés.
-   Ouverture de la Banque de propriétés de l’appareil de point de terminaison audio.
-   Obtention de la propriété de [**\_ \_ GUID AudioEndpoint**](pkey-audioendpoint-guid.md) de la bibliothèque de clés à partir de la Banque de propriétés. La valeur de la propriété est une représentation sous forme de chaîne du GUID de l’appareil DirectSound pour l’appareil de point de terminaison audio.
-   Appel de la fonction [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) pour convertir la représentation sous forme de chaîne du GUID de l’appareil en une structure GUID. Pour plus d’informations sur **CLSIDFromString**, consultez la documentation SDK Windows.

Après avoir obtenu un GUID d’appareil à partir de la fonction GetDirectSoundGuid, l’application peut appeler **DirectSoundCreate** ou **DIRECTSOUNDCAPTURECREATE** avec ce GUID pour créer l’appareil de rendu ou de capture DirectSound qui encapsule l’appareil de point de terminaison audio. Lorsque DirectSound crée un appareil de cette manière, il affecte toujours le flux audio de l’appareil à la session par défaut : la session audio spécifique au processus qui est identifiée par la valeur GUID de session GUID \_ null.

Si l’application requiert DirectSound pour assigner le flux à une session audio inter-processus ou à une session avec un GUID de session non **null** , il doit appeler la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) pour créer un objet **IDirectSound** ou **IDirectSoundCapture** au lieu d’utiliser la technique illustrée dans l’exemple de code précédent. Pour obtenir un exemple de code qui montre comment utiliser la méthode **Activate** pour spécifier une session audio inter-processus ou un GUID de session non **null** pour un flux, consultez [rôles d’appareil pour les applications DirectShow](device-roles-for-directshow-applications.md). L’exemple de code dans cette section montre comment créer un filtre DirectShow, mais, avec des modifications mineures, le code peut être adapté pour créer un appareil DirectSound.

La fonction GetDirectSoundGuid de l’exemple de code précédent appelle la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer un énumérateur pour les périphériques de point de terminaison audio dans le système. À moins que le programme appelant n’appelait auparavant la fonction [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) pour initialiser la bibliothèque com, l’appel **CoCreateInstance** échouera. Pour plus d’informations sur **CoCreateInstance**, **CoInitialize** et **CoInitializeEx**, consultez la documentation SDK Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interopérabilité avec les API audio héritées](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
