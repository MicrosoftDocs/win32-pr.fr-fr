---
description: Événements de l’appareil
ms.assetid: b31500d6-a79d-4e6e-878e-6bd77055f1ad
title: Événements d’appareil (API audio principales)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0513fc49ee5f3cb2bfe95ca2330cb79b74720923
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515338"
---
# <a name="device-events-core-audio-apis"></a><span data-ttu-id="94250-103">Événements d’appareil (API audio principales)</span><span class="sxs-lookup"><span data-stu-id="94250-103">Device Events (Core Audio APIs)</span></span>

<span data-ttu-id="94250-104">Un événement d’appareil notifie les clients qu’une modification a été apportée à l’état d’un [périphérique de point de terminaison audio](audio-endpoint-devices.md) dans le système.</span><span class="sxs-lookup"><span data-stu-id="94250-104">A device event notifies clients of a change in the status of an [audio endpoint device](audio-endpoint-devices.md) in the system.</span></span> <span data-ttu-id="94250-105">Voici quelques exemples d’événements d’appareil :</span><span class="sxs-lookup"><span data-stu-id="94250-105">The following are examples of device events:</span></span>

-   <span data-ttu-id="94250-106">L’utilisateur active ou désactive un périphérique de point de terminaison audio à partir de Gestionnaire de périphériques ou à partir du panneau de configuration multimédia Windows, Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="94250-106">The user enables or disables an audio endpoint device from Device Manager or from the Windows multimedia control panel, Mmsys.cpl.</span></span>
-   <span data-ttu-id="94250-107">L’utilisateur ajoute un adaptateur audio au système ou supprime un adaptateur audio du système.</span><span class="sxs-lookup"><span data-stu-id="94250-107">The user adds an audio adapter to the system or removes an audio adapter from the system.</span></span>
-   <span data-ttu-id="94250-108">L’utilisateur connecte un périphérique de point de terminaison audio à une prise jack audio avec la détection de la présence des prises jack ou supprime un périphérique de point de terminaison audio d’une telle Jack.</span><span class="sxs-lookup"><span data-stu-id="94250-108">The user plugs an audio endpoint device into an audio jack with jack-presence detection, or removes an audio endpoint device from such a jack.</span></span>
-   <span data-ttu-id="94250-109">L’utilisateur modifie le [rôle d’appareil](device-roles.md) affecté à un appareil.</span><span class="sxs-lookup"><span data-stu-id="94250-109">The user changes the [device role](device-roles.md) that is assigned to a device.</span></span>
-   <span data-ttu-id="94250-110">La valeur d’une [propriété d’un appareil](device-properties.md) change.</span><span class="sxs-lookup"><span data-stu-id="94250-110">The value of a [property of a device](device-properties.md) changes.</span></span>

<span data-ttu-id="94250-111">L’ajout ou la suppression d’un adaptateur audio génère des événements d’appareil pour tous les périphériques de point de terminaison audio qui se connectent à l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="94250-111">The addition or removal of an audio adapter generates device events for all of the audio endpoint devices that connect to the adapter.</span></span> <span data-ttu-id="94250-112">Les quatre premiers éléments de la liste précédente sont des exemples de modifications de l’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="94250-112">The first four items in the preceding list are examples of device state changes.</span></span> <span data-ttu-id="94250-113">Pour plus d’informations sur les États des appareils de point de terminaison audio, consultez [ \_ \_ constantes](device-state-xxx-constants.md)de l’état de l’appareil xxx.</span><span class="sxs-lookup"><span data-stu-id="94250-113">For more information about the device states of audio endpoint devices, see [DEVICE\_STATE\_XXX Constants](device-state-xxx-constants.md).</span></span> <span data-ttu-id="94250-114">Pour plus d’informations sur la détection de la présence des jacks, consultez [périphériques de point de terminaison audio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="94250-114">For more information about jack-presence detection, see [Audio Endpoint Devices](audio-endpoint-devices.md).</span></span>

<span data-ttu-id="94250-115">Un client peut s’inscrire pour être averti lorsque des événements d’appareil se produisent.</span><span class="sxs-lookup"><span data-stu-id="94250-115">A client can register to be notified when device events occur.</span></span> <span data-ttu-id="94250-116">En réponse à ces notifications, le client peut modifier dynamiquement la manière dont il utilise un appareil particulier, ou sélectionner un autre appareil à utiliser dans un but particulier.</span><span class="sxs-lookup"><span data-stu-id="94250-116">In response to these notifications, the client can dynamically change the way that it uses a particular device, or select a different device to use for a particular purpose.</span></span>

<span data-ttu-id="94250-117">Par exemple, si une application lit une piste audio via un ensemble de haut-parleurs USB et que l’utilisateur déconnecte les haut-parleur du connecteur USB, l’application reçoit une notification d’événement d’appareil.</span><span class="sxs-lookup"><span data-stu-id="94250-117">For example, if an application is playing an audio track through a set of USB speakers, and the user disconnects the speakers from the USB connector, the application receives a device-event notification.</span></span> <span data-ttu-id="94250-118">En réponse à l’événement, si l’application détecte qu’un ensemble de haut-parleurs de bureau est connecté à la carte audio intégrée sur la carte mère du système, l’application peut reprendre la piste audio via les haut-parleurs du bureau.</span><span class="sxs-lookup"><span data-stu-id="94250-118">In response to the event, if the application detects that a set of desktop speakers is connected to the integrated audio adapter on the system motherboard, the application can resume playing the audio track through the desktop speakers.</span></span> <span data-ttu-id="94250-119">Dans cet exemple, la transition des haut-parleurs USB aux haut-parleurs de bureau se produit automatiquement, sans que l’utilisateur soit obligé de rediriger explicitement l’application.</span><span class="sxs-lookup"><span data-stu-id="94250-119">In this example, the transition from USB speakers to desktop speakers occurs automatically, without requiring the user to intervene by explicitly redirecting the application.</span></span>

<span data-ttu-id="94250-120">Pour s’inscrire afin de recevoir des notifications d’appareils, un client appelle la méthode [**IMMDeviceEnumerator :: RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) .</span><span class="sxs-lookup"><span data-stu-id="94250-120">To register to receive device notifications, a client calls the [**IMMDeviceEnumerator::RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) method.</span></span> <span data-ttu-id="94250-121">Lorsque le client n’a plus besoin de notifications, il l’annule en appelant la méthode [**IMMDeviceEnumerator :: UnregisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) .</span><span class="sxs-lookup"><span data-stu-id="94250-121">When the client no longer requires notifications, it cancels them by calling the [**IMMDeviceEnumerator::UnregisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) method.</span></span> <span data-ttu-id="94250-122">Les deux méthodes acceptent un paramètre d’entrée, nommé *pNotify*, qui est un pointeur vers une instance d’interface [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) .</span><span class="sxs-lookup"><span data-stu-id="94250-122">Both methods take an input parameter, named *pNotify*, that is a pointer to an [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) interface instance.</span></span>

<span data-ttu-id="94250-123">L’interface **IMMNotificationClient** est implémentée par un client.</span><span class="sxs-lookup"><span data-stu-id="94250-123">The **IMMNotificationClient** interface is implemented by a client.</span></span> <span data-ttu-id="94250-124">L’interface contient plusieurs méthodes, chacune servant de routine de rappel pour un type particulier d’événement d’appareil.</span><span class="sxs-lookup"><span data-stu-id="94250-124">The interface contains several methods, each of which serves as a callback routine for a particular type of device event.</span></span> <span data-ttu-id="94250-125">Lorsqu’un événement d’appareil se produit dans un périphérique de point de terminaison audio, le module MMDevice appelle la méthode appropriée dans l’interface **IMMNotificationClient** de chaque client actuellement inscrit pour recevoir des notifications d’événements d’appareil.</span><span class="sxs-lookup"><span data-stu-id="94250-125">When a device event occurs in an audio endpoint device, the MMDevice module calls the appropriate method in the **IMMNotificationClient** interface of every client that is currently registered to receive device-event notifications.</span></span> <span data-ttu-id="94250-126">Ces appels passent une description de l’événement aux clients.</span><span class="sxs-lookup"><span data-stu-id="94250-126">These calls pass a description of the event to the clients.</span></span> <span data-ttu-id="94250-127">Pour plus d’informations, consultez [**IMMNotificationClient interface**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span><span class="sxs-lookup"><span data-stu-id="94250-127">For more information, see [**IMMNotificationClient Interface**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span></span>

<span data-ttu-id="94250-128">Un client qui est inscrit pour recevoir des notifications d’événements d’appareil reçoit des notifications de tous les types d’événements d’appareil qui se produisent dans tous les périphériques de point de terminaison audio du système.</span><span class="sxs-lookup"><span data-stu-id="94250-128">A client that is registered to receive device-event notifications will receive notifications of all types of device events that occur in all of the audio endpoint devices in the system.</span></span> <span data-ttu-id="94250-129">Si un client s’intéresse uniquement à certains types d’événements ou à certains appareils, les méthodes de son implémentation de **IMMNotificationClient** doivent filtrer les événements de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="94250-129">If a client is interested only in certain event types or in certain devices, then the methods in its **IMMNotificationClient** implementation should filter the events appropriately.</span></span>

<span data-ttu-id="94250-130">Le SDK Windows fournit des exemples qui incluent plusieurs implémentations de l' [**interface IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span><span class="sxs-lookup"><span data-stu-id="94250-130">The Windows SDK provides samples that include several implementations for the [**IMMNotificationClient Interface**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span></span> <span data-ttu-id="94250-131">Pour plus d’informations, consultez [les exemples du kit de développement logiciel (SDK) qui utilisent les API audio principales](sdk-samples-that-use-the-core-audio-apis.md).</span><span class="sxs-lookup"><span data-stu-id="94250-131">For more information, see [SDK Samples That Use the Core Audio APIs](sdk-samples-that-use-the-core-audio-apis.md).</span></span>

<span data-ttu-id="94250-132">L’exemple de code suivant montre une implémentation possible de l’interface **IMMNotificationClient** :</span><span class="sxs-lookup"><span data-stu-id="94250-132">The following code example shows a possible implementation of the **IMMNotificationClient** interface:</span></span>


```C++
//-----------------------------------------------------------
// Example implementation of IMMNotificationClient interface.
// When the status of audio endpoint devices change, the
// MMDevice module calls these methods to notify the client.
//-----------------------------------------------------------

#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

class CMMNotificationClient : public IMMNotificationClient
{
    LONG _cRef;
    IMMDeviceEnumerator *_pEnumerator;

    // Private function to print device-friendly name
    HRESULT _PrintDeviceName(LPCWSTR  pwstrId);

public:
    CMMNotificationClient() :
        _cRef(1),
        _pEnumerator(NULL)
    {
    }

    ~CMMNotificationClient()
    {
        SAFE_RELEASE(_pEnumerator)
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(
                                REFIID riid, VOID **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IMMNotificationClient) == riid)
        {
            AddRef();
            *ppvInterface = (IMMNotificationClient*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Callback methods for device-event notifications.

    HRESULT STDMETHODCALLTYPE OnDefaultDeviceChanged(
                                EDataFlow flow, ERole role,
                                LPCWSTR pwstrDeviceId)
    {
        char  *pszFlow = "?????";
        char  *pszRole = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (flow)
        {
        case eRender:
            pszFlow = "eRender";
            break;
        case eCapture:
            pszFlow = "eCapture";
            break;
        }

        switch (role)
        {
        case eConsole:
            pszRole = "eConsole";
            break;
        case eMultimedia:
            pszRole = "eMultimedia";
            break;
        case eCommunications:
            pszRole = "eCommunications";
            break;
        }

        printf("  -->New default device: flow = %s, role = %s\n",
               pszFlow, pszRole);
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceAdded(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Added device\n");
        return S_OK;
    };

    HRESULT STDMETHODCALLTYPE OnDeviceRemoved(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Removed device\n");
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceStateChanged(
                                LPCWSTR pwstrDeviceId,
                                DWORD dwNewState)
    {
        char  *pszState = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (dwNewState)
        {
        case DEVICE_STATE_ACTIVE:
            pszState = "ACTIVE";
            break;
        case DEVICE_STATE_DISABLED:
            pszState = "DISABLED";
            break;
        case DEVICE_STATE_NOTPRESENT:
            pszState = "NOTPRESENT";
            break;
        case DEVICE_STATE_UNPLUGGED:
            pszState = "UNPLUGGED";
            break;
        }

        printf("  -->New device state is DEVICE_STATE_%s (0x%8.8x)\n",
               pszState, dwNewState);

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnPropertyValueChanged(
                                LPCWSTR pwstrDeviceId,
                                const PROPERTYKEY key)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Changed device property "
               "{%8.8x-%4.4x-%4.4x-%2.2x%2.2x-%2.2x%2.2x%2.2x%2.2x%2.2x%2.2x}#%d\n",
               key.fmtid.Data1, key.fmtid.Data2, key.fmtid.Data3,
               key.fmtid.Data4[0], key.fmtid.Data4[1],
               key.fmtid.Data4[2], key.fmtid.Data4[3],
               key.fmtid.Data4[4], key.fmtid.Data4[5],
               key.fmtid.Data4[6], key.fmtid.Data4[7],
               key.pid);
        return S_OK;
    }
};

// Given an endpoint ID string, print the friendly device name.
HRESULT CMMNotificationClient::_PrintDeviceName(LPCWSTR pwstrId)
{
    HRESULT hr = S_OK;
    IMMDevice *pDevice = NULL;
    IPropertyStore *pProps = NULL;
    PROPVARIANT varString;

    CoInitialize(NULL);
    PropVariantInit(&varString);

    if (_pEnumerator == NULL)
    {
        // Get enumerator for audio endpoint devices.
        hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                              NULL, CLSCTX_INPROC_SERVER,
                              __uuidof(IMMDeviceEnumerator),
                              (void**)&_pEnumerator);
    }
    if (hr == S_OK)
    {
        hr = _pEnumerator->GetDevice(pwstrId, &pDevice);
    }
    if (hr == S_OK)
    {
        hr = pDevice->OpenPropertyStore(STGM_READ, &pProps);
    }
    if (hr == S_OK)
    {
        // Get the endpoint device's friendly-name property.
        hr = pProps->GetValue(PKEY_Device_FriendlyName, &varString);
    }
    printf("----------------------\nDevice name: \"%S\"\n"
           "  Endpoint ID string: \"%S\"\n",
           (hr == S_OK) ? varString.pwszVal : L"null device",
           (pwstrId != NULL) ? pwstrId : L"null ID");

    PropVariantClear(&varString);

    SAFE_RELEASE(pProps)
    SAFE_RELEASE(pDevice)
    CoUninitialize();
    return hr;
}
```



<span data-ttu-id="94250-133">La classe CMMNotificationClient de l’exemple de code précédent est une implémentation de l’interface **IMMNotificationClient** .</span><span class="sxs-lookup"><span data-stu-id="94250-133">The CMMNotificationClient class in the preceding code example is an implementation of the **IMMNotificationClient** interface.</span></span> <span data-ttu-id="94250-134">Comme **IMMNotificationClient** hérite de **IUnknown**, la définition de classe contient des implémentations des méthodes **IUnknown** **AddRef**, **Release** et **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="94250-134">Because **IMMNotificationClient** inherits from **IUnknown**, the class definition contains implementations of the **IUnknown** methods **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="94250-135">Les autres méthodes publiques de la définition de classe sont spécifiques à l’interface **IMMNotificationClient** .</span><span class="sxs-lookup"><span data-stu-id="94250-135">The remaining public methods in the class definition are specific to the **IMMNotificationClient** interface.</span></span> <span data-ttu-id="94250-136">Ces méthodes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="94250-136">These methods are:</span></span>

-   <span data-ttu-id="94250-137">**OnDefaultDeviceChanged**, qui est appelé lorsque l’utilisateur modifie le rôle d’appareil d’un périphérique de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="94250-137">**OnDefaultDeviceChanged**, which is called when the user changes the device role of an audio endpoint device.</span></span>
-   <span data-ttu-id="94250-138">**Événements ondeviceadded**, qui est appelé lorsque l’utilisateur ajoute un périphérique de point de terminaison audio au système.</span><span class="sxs-lookup"><span data-stu-id="94250-138">**OnDeviceAdded**, which is called when the user adds an audio endpoint device to the system.</span></span>
-   <span data-ttu-id="94250-139">**OnDeviceRemoved**, qui est appelé lorsque l’utilisateur supprime un périphérique de point de terminaison audio du système.</span><span class="sxs-lookup"><span data-stu-id="94250-139">**OnDeviceRemoved**, which is called when the user removes an audio endpoint device from the system.</span></span>
-   <span data-ttu-id="94250-140">**OnDeviceStateChanged**, qui est appelé lorsque l’état de l’appareil d’un périphérique de point de terminaison audio change.</span><span class="sxs-lookup"><span data-stu-id="94250-140">**OnDeviceStateChanged**, which is called when the device state of an audio endpoint device changes.</span></span> <span data-ttu-id="94250-141">(Pour plus d’informations sur les États des appareils, consultez [ \_ \_ constantes](device-state-xxx-constants.md)de l’état de l’appareil xxx.)</span><span class="sxs-lookup"><span data-stu-id="94250-141">(For more information about device states, see [DEVICE\_STATE\_ XXX Constants](device-state-xxx-constants.md).)</span></span>
-   <span data-ttu-id="94250-142">**OnPropertyValueChanged**, qui est appelé quand la valeur d’une propriété d’un périphérique de point de terminaison audio change.</span><span class="sxs-lookup"><span data-stu-id="94250-142">**OnPropertyValueChanged**, which is called when the value of a property of an audio endpoint device changes.</span></span>

<span data-ttu-id="94250-143">Chacune de ces méthodes accepte un paramètre d’entrée, *pwstrDeviceId*, qui est un pointeur vers une chaîne d’ID de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="94250-143">Each of these methods takes an input parameter, *pwstrDeviceId*, that is a pointer to an endpoint ID string.</span></span> <span data-ttu-id="94250-144">La chaîne identifie l’appareil de point de terminaison audio dans lequel l’événement d’appareil s’est produit.</span><span class="sxs-lookup"><span data-stu-id="94250-144">The string identifies the audio endpoint device in which the device event occurred.</span></span>

<span data-ttu-id="94250-145">Dans l’exemple de code précédent, \_ PrintDeviceName est une méthode privée dans la classe CMMNotificationClient qui imprime le nom convivial de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="94250-145">In the preceding code example, \_PrintDeviceName is a private method in the CMMNotificationClient class that prints the friendly name of the device.</span></span> <span data-ttu-id="94250-146">\_PrintDeviceName prend la chaîne d’ID de point de terminaison en tant que paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="94250-146">\_PrintDeviceName takes the endpoint ID string as an input parameter.</span></span> <span data-ttu-id="94250-147">Elle transmet la chaîne à la méthode [**IMMDeviceEnumerator :: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .</span><span class="sxs-lookup"><span data-stu-id="94250-147">It passes the string to the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="94250-148">**GetDevice** crée un objet d’appareil de point de terminaison pour représenter l’appareil et fournit l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) à cet objet.</span><span class="sxs-lookup"><span data-stu-id="94250-148">**GetDevice** creates an endpoint device object to represent the device and provides the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface to that object.</span></span> <span data-ttu-id="94250-149">Ensuite, \_ PrintDeviceName appelle la méthode [**IMMDevice :: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) pour récupérer l' **interface IPropertyStore** dans la Banque de propriétés de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="94250-149">Next, \_PrintDeviceName calls the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method to retrieve the **IPropertyStore** interface to the device's property store.</span></span> <span data-ttu-id="94250-150">Enfin, \_ PrintDeviceName appelle la méthode **IPropertyStore :: GetItem** pour obtenir la propriété friendly-name de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="94250-150">Finally, \_PrintDeviceName calls the **IPropertyStore::GetItem** method to obtain the friendly-name property of the device.</span></span> <span data-ttu-id="94250-151">Pour plus d’informations sur **IPropertyStore**, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="94250-151">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="94250-152">En plus des événements d’appareil, les clients peuvent s’inscrire pour recevoir des notifications d’événements de session audio et d’événements de volume de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="94250-152">In addition to device events, clients can register to receive notifications of audio-session events and endpoint-volume events.</span></span> <span data-ttu-id="94250-153">Pour plus d’informations, consultez [**interface IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) et [**interface IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).</span><span class="sxs-lookup"><span data-stu-id="94250-153">For more information, see [**IAudioSessionEvents Interface**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) and [**IAudioEndpointVolumeCallback Interface**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="94250-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="94250-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94250-155">Périphériques de point de terminaison audio</span><span class="sxs-lookup"><span data-stu-id="94250-155">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> </dl>

 

 



