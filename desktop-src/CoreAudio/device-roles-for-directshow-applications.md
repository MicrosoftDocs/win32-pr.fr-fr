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
# <a name="device-roles-for-directshow-applications"></a><span data-ttu-id="c3cbb-103">Rôles d’appareil pour les applications DirectShow</span><span class="sxs-lookup"><span data-stu-id="c3cbb-103">Device Roles for DirectShow Applications</span></span>

> [!Note]  
> <span data-ttu-id="c3cbb-104">L' [API MMDevice](mmdevice-api.md) prend en charge les rôles d’appareil.</span><span class="sxs-lookup"><span data-stu-id="c3cbb-104">The [MMDevice API](mmdevice-api.md) supports device roles.</span></span> <span data-ttu-id="c3cbb-105">Toutefois, l’interface utilisateur de Windows Vista n’implémente pas la prise en charge de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="c3cbb-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="c3cbb-106">La prise en charge de l’interface utilisateur pour les rôles d’appareil peut être implémentée dans une future version de Windows.</span><span class="sxs-lookup"><span data-stu-id="c3cbb-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="c3cbb-107">Pour plus d’informations, consultez [rôles de périphérique dans Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="c3cbb-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="c3cbb-108">L’API DirectShow ne permet pas à une application de sélectionner l’appareil de [point de terminaison audio](audio-endpoint-devices.md) affecté à un rôle d' [appareil](device-roles.md)particulier.</span><span class="sxs-lookup"><span data-stu-id="c3cbb-108">The DirectShow API does not provide a means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that is assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="c3cbb-109">Toutefois, dans Windows Vista, les API audio de base peuvent être utilisées conjointement avec une application DirectShow pour activer la sélection d’appareils en fonction du rôle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="c3cbb-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a DirectShow application to enable device selection based on device role.</span></span> <span data-ttu-id="c3cbb-110">Avec l’aide des API audio de base, l’application peut :</span><span class="sxs-lookup"><span data-stu-id="c3cbb-110">With the help of the core audio APIs, the application can:</span></span>

-   <span data-ttu-id="c3cbb-111">Identifiez l’appareil de point de terminaison audio que l’utilisateur a affecté à un rôle d’appareil particulier.</span><span class="sxs-lookup"><span data-stu-id="c3cbb-111">Identify the audio endpoint device that the user has assigned to a particular device role.</span></span>
-   <span data-ttu-id="c3cbb-112">Créez un filtre de rendu audio DirectShow avec une interface [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) qui encapsule l’appareil de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="c3cbb-112">Create a DirectShow audio rendering filter with an [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) interface that encapsulates the audio endpoint device.</span></span>
-   <span data-ttu-id="c3cbb-113">Créez un graphique DirectShow qui incorpore le filtre.</span><span class="sxs-lookup"><span data-stu-id="c3cbb-113">Build a DirectShow graph that incorporates the filter.</span></span>

<span data-ttu-id="c3cbb-114">Pour plus d’informations sur DirectShow et [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter), consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="c3cbb-114">For more information about DirectShow and [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter), see the Windows SDK documentation.</span></span>

<span data-ttu-id="c3cbb-115">L’exemple de code suivant montre comment créer un filtre de rendu audio DirectShow qui encapsule l’appareil de point de terminaison de rendu affecté à un rôle d’appareil particulier :</span><span class="sxs-lookup"><span data-stu-id="c3cbb-115">The following code example shows how to create a DirectShow audio rendering filter that encapsulates the rendering endpoint device that is assigned to a particular device role:</span></span>


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



<span data-ttu-id="c3cbb-116">Dans l’exemple de code précédent, la fonction CreateAudioRenderer accepte un rôle d’appareil (eConsole, eMultimedia ou eCommunications) comme paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="c3cbb-116">In the preceding code example, the CreateAudioRenderer function accepts a device role (eConsole, eMultimedia, or eCommunications) as an input parameter.</span></span> <span data-ttu-id="c3cbb-117">Le deuxième paramètre est un pointeur par le biais duquel la fonction écrit l’adresse d’une instance d’interface [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="c3cbb-117">The second parameter is a pointer through which the function writes the address of an [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) interface instance.</span></span> <span data-ttu-id="c3cbb-118">En outre, l’exemple montre comment utiliser la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) pour affecter le flux audio de l’instance **IBaseFilter** à une session audio INTERprocessus avec un GUID de session spécifique à l’application (spécifié par la constante **guidAudioSessionId** ).</span><span class="sxs-lookup"><span data-stu-id="c3cbb-118">In addition, the example shows how to use the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to assign the audio stream in the **IBaseFilter** instance to a cross-process audio session with an application-specific session GUID (specified by the **guidAudioSessionId** constant).</span></span> <span data-ttu-id="c3cbb-119">Le troisième paramètre de l’appel d' **activation** pointe vers une structure qui contient le GUID de session et l’indicateur inter-processus.</span><span class="sxs-lookup"><span data-stu-id="c3cbb-119">The third parameter in the **Activate** call points to a structure that contains the session GUID and cross-process flag.</span></span> <span data-ttu-id="c3cbb-120">Si l’utilisateur exécute plusieurs instances de l’application, les flux audio de toutes les instances utilisent le même GUID de session et, par conséquent, appartiennent à la même session.</span><span class="sxs-lookup"><span data-stu-id="c3cbb-120">If the user runs multiple instances of the application, then the audio streams from all the instances use the same session GUID and thus belong to the same session.</span></span>

<span data-ttu-id="c3cbb-121">L’appelant peut également spécifier **null** comme troisième paramètre dans l’appel [**Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) pour affecter le flux à la session par défaut en tant que session spécifique au processus avec GUID de la valeur GUID de session GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="c3cbb-121">Alternatively, the caller can specify **NULL** as the third parameter in the [**Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) call to assign the stream to the default session as the process-specific session with session GUID value GUID\_NULL.</span></span> <span data-ttu-id="c3cbb-122">Pour plus d’informations, consultez **IMMDevice :: Activate**.</span><span class="sxs-lookup"><span data-stu-id="c3cbb-122">For more information, see **IMMDevice::Activate**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3cbb-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3cbb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3cbb-124">Interopérabilité avec les API audio héritées</span><span class="sxs-lookup"><span data-stu-id="c3cbb-124">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
