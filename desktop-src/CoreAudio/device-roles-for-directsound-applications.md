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
# <a name="device-roles-for-directsound-applications"></a><span data-ttu-id="5eda3-103">Rôles d’appareil pour les applications DirectSound</span><span class="sxs-lookup"><span data-stu-id="5eda3-103">Device Roles for DirectSound Applications</span></span>

> [!Note]  
> <span data-ttu-id="5eda3-104">L' [API MMDevice](mmdevice-api.md) prend en charge les rôles d’appareil.</span><span class="sxs-lookup"><span data-stu-id="5eda3-104">The [MMDevice API](mmdevice-api.md) supports device roles.</span></span> <span data-ttu-id="5eda3-105">Toutefois, l’interface utilisateur de Windows Vista n’implémente pas la prise en charge de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="5eda3-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="5eda3-106">La prise en charge de l’interface utilisateur pour les rôles d’appareil peut être implémentée dans une future version de Windows.</span><span class="sxs-lookup"><span data-stu-id="5eda3-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="5eda3-107">Pour plus d’informations, consultez [rôles de périphérique dans Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="5eda3-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="5eda3-108">L’API DirectSound ne permet pas à une application de sélectionner l’appareil de [point de terminaison audio](audio-endpoint-devices.md) que l’utilisateur a affecté à un [rôle d’appareil](device-roles.md)particulier.</span><span class="sxs-lookup"><span data-stu-id="5eda3-108">The DirectSound API does not provide a means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that the user has assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="5eda3-109">Toutefois, dans Windows Vista, les API audio de base peuvent être utilisées conjointement avec une application DirectSound pour activer la sélection d’appareils en fonction du rôle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="5eda3-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a DirectSound application to enable device selection based on device role.</span></span> <span data-ttu-id="5eda3-110">Avec l’aide des API audio de base, l’application peut identifier l’appareil de point de terminaison audio qui est affecté à un rôle particulier, obtenir le GUID de l’appareil DirectSound pour l’appareil de point de terminaison et appeler la fonction **DirectSoundCreate** ou **DirectSoundCaptureCreate** pour créer une instance d’interface **IDirectSound** ou **IDirectSoundCapture** qui encapsule l’appareil de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5eda3-110">With the help of the core audio APIs, the application can identify the audio endpoint device that is assigned to a particular role, get the DirectSound device GUID for the endpoint device, and call the **DirectSoundCreate** or **DirectSoundCaptureCreate** function to create an **IDirectSound** or **IDirectSoundCapture** interface instance that encapsulates the endpoint device.</span></span> <span data-ttu-id="5eda3-111">Pour plus d’informations sur DirectSound, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="5eda3-111">For more information about DirectSound, see the Windows SDK documentation.</span></span>

<span data-ttu-id="5eda3-112">L’exemple de code suivant montre comment obtenir le GUID de l’appareil DirectSound pour le périphérique de rendu ou de capture qui est actuellement affecté à un rôle d’appareil particulier :</span><span class="sxs-lookup"><span data-stu-id="5eda3-112">The following code example shows how to obtain the DirectSound device GUID for the rendering or capture device that is currently assigned to a particular device role:</span></span>


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



<span data-ttu-id="5eda3-113">Dans l’exemple de code précédent, la fonction GetDirectSoundGuid accepte un sens de workflow de données (eRender ou eCapture) et un rôle d’appareil (eConsole, eMultimedia ou eCommunications) comme paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5eda3-113">In the preceding code example, the GetDirectSoundGuid function accepts a data-flow direction (eRender or eCapture) and a device role (eConsole, eMultimedia, or eCommunications) as input parameters.</span></span> <span data-ttu-id="5eda3-114">Le troisième paramètre est un pointeur à travers lequel la fonction écrit un GUID d’appareil que l’application peut fournir comme paramètre d’entrée à la fonction **DirectSoundCreate** ou **DirectSoundCaptureCreate** .</span><span class="sxs-lookup"><span data-stu-id="5eda3-114">The third parameter is a pointer through which the function writes a device GUID that the application can supply as an input parameter to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function.</span></span>

<span data-ttu-id="5eda3-115">L’exemple de code précédent obtient le GUID de l’appareil DirectSound en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="5eda3-115">The preceding code example obtains the DirectSound device GUID by:</span></span>

-   <span data-ttu-id="5eda3-116">Création d’une instance d’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) qui représente l’appareil de point de terminaison audio ayant la direction de flux de données et le rôle d’appareil spécifiés.</span><span class="sxs-lookup"><span data-stu-id="5eda3-116">Creating an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface instance that represents the audio endpoint device that has the specified data-flow direction and device role.</span></span>
-   <span data-ttu-id="5eda3-117">Ouverture de la Banque de propriétés de l’appareil de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="5eda3-117">Opening the property store of the audio endpoint device.</span></span>
-   <span data-ttu-id="5eda3-118">Obtention de la propriété de [**\_ \_ GUID AudioEndpoint**](pkey-audioendpoint-guid.md) de la bibliothèque de clés à partir de la Banque de propriétés.</span><span class="sxs-lookup"><span data-stu-id="5eda3-118">Getting the [**PKEY\_AudioEndpoint\_GUID**](pkey-audioendpoint-guid.md) property from the property store.</span></span> <span data-ttu-id="5eda3-119">La valeur de la propriété est une représentation sous forme de chaîne du GUID de l’appareil DirectSound pour l’appareil de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="5eda3-119">The property value is a string representation of the DirectSound device GUID for the audio endpoint device.</span></span>
-   <span data-ttu-id="5eda3-120">Appel de la fonction [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) pour convertir la représentation sous forme de chaîne du GUID de l’appareil en une structure GUID.</span><span class="sxs-lookup"><span data-stu-id="5eda3-120">Calling the [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) function to convert the string representation of the device GUID to a GUID structure.</span></span> <span data-ttu-id="5eda3-121">Pour plus d’informations sur **CLSIDFromString**, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="5eda3-121">For more information about **CLSIDFromString**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="5eda3-122">Après avoir obtenu un GUID d’appareil à partir de la fonction GetDirectSoundGuid, l’application peut appeler **DirectSoundCreate** ou **DIRECTSOUNDCAPTURECREATE** avec ce GUID pour créer l’appareil de rendu ou de capture DirectSound qui encapsule l’appareil de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="5eda3-122">After obtaining a device GUID from the GetDirectSoundGuid function, the application can call **DirectSoundCreate** or **DirectSoundCaptureCreate** with this GUID to create the DirectSound rendering or capture device that encapsulates the audio endpoint device.</span></span> <span data-ttu-id="5eda3-123">Lorsque DirectSound crée un appareil de cette manière, il affecte toujours le flux audio de l’appareil à la session par défaut : la session audio spécifique au processus qui est identifiée par la valeur GUID de session GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="5eda3-123">When DirectSound creates a device in this way, it always assigns the device's audio stream to the default session—the process-specific audio session that is identified by the session GUID value GUID\_NULL.</span></span>

<span data-ttu-id="5eda3-124">Si l’application requiert DirectSound pour assigner le flux à une session audio inter-processus ou à une session avec un GUID de session non **null** , il doit appeler la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) pour créer un objet **IDirectSound** ou **IDirectSoundCapture** au lieu d’utiliser la technique illustrée dans l’exemple de code précédent.</span><span class="sxs-lookup"><span data-stu-id="5eda3-124">If the application requires DirectSound to assign the stream to a cross-process audio session or to a session with a non-**NULL** session GUID, it should call the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to create an **IDirectSound** or **IDirectSoundCapture** object instead of using the technique shown in the preceding code example.</span></span> <span data-ttu-id="5eda3-125">Pour obtenir un exemple de code qui montre comment utiliser la méthode **Activate** pour spécifier une session audio inter-processus ou un GUID de session non **null** pour un flux, consultez [rôles d’appareil pour les applications DirectShow](device-roles-for-directshow-applications.md).</span><span class="sxs-lookup"><span data-stu-id="5eda3-125">For a code example that shows how to use the **Activate** method to specify a cross-process audio session or a non-**NULL** session GUID for a stream, see [Device Roles for DirectShow Applications](device-roles-for-directshow-applications.md).</span></span> <span data-ttu-id="5eda3-126">L’exemple de code dans cette section montre comment créer un filtre DirectShow, mais, avec des modifications mineures, le code peut être adapté pour créer un appareil DirectSound.</span><span class="sxs-lookup"><span data-stu-id="5eda3-126">The code example in that section shows how to create a DirectShow filter, but, with minor modifications, the code can be adapted to create a DirectSound device.</span></span>

<span data-ttu-id="5eda3-127">La fonction GetDirectSoundGuid de l’exemple de code précédent appelle la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer un énumérateur pour les périphériques de point de terminaison audio dans le système.</span><span class="sxs-lookup"><span data-stu-id="5eda3-127">The GetDirectSoundGuid function in the preceding code example calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="5eda3-128">À moins que le programme appelant n’appelait auparavant la fonction [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) pour initialiser la bibliothèque com, l’appel **CoCreateInstance** échouera.</span><span class="sxs-lookup"><span data-stu-id="5eda3-128">Unless the calling program previously called either the [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="5eda3-129">Pour plus d’informations sur **CoCreateInstance**, **CoInitialize** et **CoInitializeEx**, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="5eda3-129">For more information about **CoCreateInstance**, **CoInitialize**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5eda3-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5eda3-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eda3-131">Interopérabilité avec les API audio héritées</span><span class="sxs-lookup"><span data-stu-id="5eda3-131">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
