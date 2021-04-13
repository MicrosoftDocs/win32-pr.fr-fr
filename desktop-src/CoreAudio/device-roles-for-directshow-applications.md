---
description: Rôles d’appareil pour les applications DirectShow
ms.assetid: 54f42bda-b4a0-465c-9ce6-9102d2908776
title: Rôles d’appareil pour les applications DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df8b43ddd56870b65fc9ec1e3bb600e8e6b79528
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482760"
---
# <a name="device-roles-for-directshow-applications"></a>Rôles d’appareil pour les applications DirectShow

> [!Note]  
> L' [API MMDevice](mmdevice-api.md) prend en charge les rôles d’appareil. Toutefois, l’interface utilisateur de Windows Vista n’implémente pas la prise en charge de cette fonctionnalité. La prise en charge de l’interface utilisateur pour les rôles d’appareil peut être implémentée dans une future version de Windows. Pour plus d’informations, consultez [rôles de périphérique dans Windows Vista](device-roles-in-windows-vista.md).

 

L’API DirectShow ne permet pas à une application de sélectionner l’appareil de [point de terminaison audio](audio-endpoint-devices.md) affecté à un rôle d' [appareil](device-roles.md)particulier. Toutefois, dans Windows Vista, les API audio de base peuvent être utilisées conjointement avec une application DirectShow pour activer la sélection d’appareils en fonction du rôle d’appareil. Avec l’aide des API audio de base, l’application peut :

-   Identifiez l’appareil de point de terminaison audio que l’utilisateur a affecté à un rôle d’appareil particulier.
-   Créez un filtre de rendu audio DirectShow avec une interface [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) qui encapsule l’appareil de point de terminaison audio.
-   Créez un graphique DirectShow qui incorpore le filtre.

Pour plus d’informations sur DirectShow et [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter), consultez la documentation SDK Windows.

L’exemple de code suivant montre comment créer un filtre de rendu audio DirectShow qui encapsule l’appareil de point de terminaison de rendu affecté à un rôle d’appareil particulier :


```C++
//-----------------------------------------------------------
// Create a DirectShow audio rendering filter that
// encapsulates the audio endpoint device that is currently
// assigned to the specified device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

// This application's audio session GUID
const GUID guidAudioSessionId = {
    0xb13ff52e, 0xa5cf, 0x4fca,
    {0x9f, 0xc3, 0x42, 0x26, 0x5b, 0x0b, 0x14, 0xfb}
};

HRESULT CreateAudioRenderer(ERole role, IBaseFilter** ppAudioRenderer)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;

    if (ppAudioRenderer == NULL)
    {
        return E_POINTER;
    }

    // Activate the IBaseFilter interface on the
    // audio renderer with the specified role.
    hr = CoCreateInstance(CLSID_MMDeviceEnumerator,
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    DIRECTX_AUDIO_ACTIVATION_PARAMS  daap;
    daap.cbDirectXAudioActivationParams = sizeof(daap);
    daap.guidAudioSession = guidAudioSessionId;
    daap.dwAudioStreamFlags = AUDCLNT_STREAMFLAGS_CROSSPROCESS;

    PROPVARIANT  var;
    PropVariantInit(&var);

    var.vt = VT_BLOB;
    var.blob.cbSize = sizeof(daap);
    var.blob.pBlobData = (BYTE*)&daap;

    hr = pDevice->Activate(__uuidof(IBaseFilter),
                           CLSCTX_ALL, &var,
                           (void**)ppAudioRenderer);
    EXIT_ON_ERROR(hr)

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    return hr;
}
```



Dans l’exemple de code précédent, la fonction CreateAudioRenderer accepte un rôle d’appareil (eConsole, eMultimedia ou eCommunications) comme paramètre d’entrée. Le deuxième paramètre est un pointeur par le biais duquel la fonction écrit l’adresse d’une instance d’interface [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) . En outre, l’exemple montre comment utiliser la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) pour affecter le flux audio de l’instance **IBaseFilter** à une session audio INTERprocessus avec un GUID de session spécifique à l’application (spécifié par la constante **guidAudioSessionId** ). Le troisième paramètre de l’appel d' **activation** pointe vers une structure qui contient le GUID de session et l’indicateur inter-processus. Si l’utilisateur exécute plusieurs instances de l’application, les flux audio de toutes les instances utilisent le même GUID de session et, par conséquent, appartiennent à la même session.

L’appelant peut également spécifier **null** comme troisième paramètre dans l’appel [**Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) pour affecter le flux à la session par défaut en tant que session spécifique au processus avec GUID de la valeur GUID de session GUID \_ null. Pour plus d’informations, consultez **IMMDevice :: Activate**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interopérabilité avec les API audio héritées](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
