---
description: Propriétés de l’appareil
ms.assetid: ad8753ba-ad20-4122-b0f2-eb165f98db67
title: Propriétés de l’appareil (API audio principales)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a868e4bb806bd49d934febed164bcd70fba39f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514919"
---
# <a name="device-properties-core-audio-apis"></a><span data-ttu-id="d3830-103">Propriétés de l’appareil (API audio principales)</span><span class="sxs-lookup"><span data-stu-id="d3830-103">Device Properties (Core Audio APIs)</span></span>

<span data-ttu-id="d3830-104">Pendant le processus d’énumération des [appareils de point de terminaison audio](audio-endpoint-devices.md), une application cliente peut interroger les objets de point de terminaison pour leurs propriétés d’appareil.</span><span class="sxs-lookup"><span data-stu-id="d3830-104">During the process of enumerating [audio endpoint devices](audio-endpoint-devices.md), a client application can interrogate the endpoint objects for their device properties.</span></span> <span data-ttu-id="d3830-105">Les propriétés de l’appareil sont exposées dans l’implémentation de l’interface **IPropertyStore** de l’API MMDevice.</span><span class="sxs-lookup"><span data-stu-id="d3830-105">The device properties are exposed in MMDevice API's implementation of the **IPropertyStore** interface.</span></span> <span data-ttu-id="d3830-106">À partir d’une référence à l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) d’un objet de point de terminaison, un client peut obtenir une référence à la Banque de propriétés de l’objet de point de terminaison en appelant la méthode [**IMMDevice :: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) .</span><span class="sxs-lookup"><span data-stu-id="d3830-106">Given a reference to the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of an endpoint object, a client can obtain a reference to the endpoint object's property store by calling the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method.</span></span>

<span data-ttu-id="d3830-107">L’objet de magasin de propriétés expose une interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="d3830-107">The property-store object exposes an **IPropertyStore** interface.</span></span> <span data-ttu-id="d3830-108">Les deux méthodes principales de cette interface sont **IPropertyStore :: GetValue**, qui obtient une valeur de propriété de périphérique, et **IPropertyStore :: SetValue**, qui définit une valeur de propriété d’appareil.</span><span class="sxs-lookup"><span data-stu-id="d3830-108">The two primary methods in this interface are **IPropertyStore::GetValue**, which gets a device property value, and **IPropertyStore::SetValue**, which sets a device property value.</span></span> <span data-ttu-id="d3830-109">Pour plus d’informations sur **IPropertyStore**, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="d3830-109">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="d3830-110">L’implémentation de l’API MMDevice de la Banque de propriétés est différente de l’objet de magasin de propriétés de Shell standard.</span><span class="sxs-lookup"><span data-stu-id="d3830-110">The MMDevice API's implementation of the property store is different from the standard shell property store object.</span></span> <span data-ttu-id="d3830-111">Pour modifier une valeur de propriété, l’application cliente doit appeler la méthode **IPropertyStore :: SetValue** .</span><span class="sxs-lookup"><span data-stu-id="d3830-111">To change a property value, the client application must call the **IPropertyStore::SetValue** method.</span></span> <span data-ttu-id="d3830-112">Pendant cet appel, les nouvelles valeurs sont définies et écrites dans le registre.</span><span class="sxs-lookup"><span data-stu-id="d3830-112">During this call, the new values are set and written in the registry.</span></span> <span data-ttu-id="d3830-113">Par conséquent, l’application n’a pas besoin d’appeler la méthode **IPropertyStore :: Commit** après l’appel **SetValue** .</span><span class="sxs-lookup"><span data-stu-id="d3830-113">Therefore, the application does not need to call the **IPropertyStore::Commit** method after the **SetValue** call.</span></span> <span data-ttu-id="d3830-114">Le descripteur du Registre est fermé uniquement lorsque le client libère le pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="d3830-114">The handle to the registry is closed only when the client releases the interface pointer.</span></span>

<span data-ttu-id="d3830-115">En règle générale, les applications clientes tierces appellent la méthode **GetValue** , mais pas la méthode **SetValue** .</span><span class="sxs-lookup"><span data-stu-id="d3830-115">Typically, third-party client applications call the **GetValue** method but not the **SetValue** method.</span></span> <span data-ttu-id="d3830-116">Le gestionnaire des points de terminaison définit les propriétés de l’appareil de base pour les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="d3830-116">The endpoint manager sets the basic device properties for endpoints.</span></span> <span data-ttu-id="d3830-117">Le gestionnaire des points de terminaison est le composant Windows Vista qui est chargé de détecter la présence d’appareils de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="d3830-117">The endpoint manager is the Windows Vista component that is responsible for detecting the presence of audio endpoint devices.</span></span>

<span data-ttu-id="d3830-118">Chaque \_ identificateur de propriété de type d’éléments de la liste suivante est une constante de type **PROPERTYKEY** définie dans le fichier d’en-tête Functiondiscoverykeys \_ devpkey. h.</span><span class="sxs-lookup"><span data-stu-id="d3830-118">Each PKEY\_Xxx property identifier in the following list is a constant of type **PROPERTYKEY** that is defined in header file Functiondiscoverykeys\_devpkey.h.</span></span> <span data-ttu-id="d3830-119">Tous les périphériques de point de terminaison audio possèdent ces trois propriétés d’appareil.</span><span class="sxs-lookup"><span data-stu-id="d3830-119">All audio endpoint devices have these three device properties.</span></span>



| <span data-ttu-id="d3830-120">Propriété</span><span class="sxs-lookup"><span data-stu-id="d3830-120">Property</span></span>                                                                         | <span data-ttu-id="d3830-121">Description</span><span class="sxs-lookup"><span data-stu-id="d3830-121">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3830-122">**\_Deviceinterface \_ FriendlyName FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="d3830-122">**PKEY\_DeviceInterface\_FriendlyName**</span></span>](pkey-deviceinterface-friendlyname.md) | <span data-ttu-id="d3830-123">Nom convivial de la carte audio à laquelle l’appareil de point de terminaison est attaché (par exemple, « carte audio XYZ »).</span><span class="sxs-lookup"><span data-stu-id="d3830-123">The friendly name of the audio adapter to which the endpoint device is attached (for example, "XYZ Audio Adapter").</span></span> <span data-ttu-id="d3830-124">Le membre **PROPVARIANT** **VT** est défini sur VT \_ LPWStr et le membre **pwszVal** pointe sur une chaîne de caractères larges se terminant par un caractère null qui contient le nom convivial.</span><span class="sxs-lookup"><span data-stu-id="d3830-124">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the friendly name.</span></span> |
| [<span data-ttu-id="d3830-125">**Périphérique de l' \_ appareil \_**</span><span class="sxs-lookup"><span data-stu-id="d3830-125">**PKEY\_Device\_DeviceDesc**</span></span>](pkey-device-devicedesc.md)                       | <span data-ttu-id="d3830-126">Description de l’appareil du point de terminaison (par exemple, « Speakers »).</span><span class="sxs-lookup"><span data-stu-id="d3830-126">The device description of the endpoint device (for example, "Speakers").</span></span> <span data-ttu-id="d3830-127">Le membre **PROPVARIANT** **VT** est défini sur VT \_ LPWStr et le membre **pwszVal** pointe sur une chaîne de caractères larges se terminant par un caractère null qui contient la description de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d3830-127">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the device description.</span></span>                                       |
| [<span data-ttu-id="d3830-128">**Périphérique de l' \_ appareil \_**</span><span class="sxs-lookup"><span data-stu-id="d3830-128">**PKEY\_Device\_FriendlyName**</span></span>](pkey-device-friendlyname.md)                   | <span data-ttu-id="d3830-129">Nom convivial de l’appareil de point de terminaison (par exemple, « Speakers (carte audio XYZ) »).</span><span class="sxs-lookup"><span data-stu-id="d3830-129">The friendly name of the endpoint device (for example, "Speakers (XYZ Audio Adapter)").</span></span> <span data-ttu-id="d3830-130">Le membre **PROPVARIANT** **VT** est défini sur VT \_ LPWStr et le membre **pwszVal** pointe sur une chaîne de caractères larges se terminant par un caractère null qui contient le nom convivial.</span><span class="sxs-lookup"><span data-stu-id="d3830-130">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the friendly name.</span></span>                             |



 

<span data-ttu-id="d3830-131">Certains périphériques de point de terminaison audio peuvent avoir des propriétés supplémentaires qui n’apparaissent pas dans la liste précédente.</span><span class="sxs-lookup"><span data-stu-id="d3830-131">Some audio endpoint devices might have additional properties that do not appear in the preceding list.</span></span> <span data-ttu-id="d3830-132">Pour plus d’informations sur les propriétés supplémentaires, consultez [Propriétés du point de terminaison audio](audio-endpoint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d3830-132">For more information about additional properties, see [Audio Endpoint Properties](audio-endpoint-properties.md).</span></span> <span data-ttu-id="d3830-133">Pour plus d’informations sur **PROPERTYKEY**, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="d3830-133">For more information about **PROPERTYKEY**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="d3830-134">L’exemple de code suivant imprime les noms complets de tous les appareils de point de terminaison de rendu audio dans le système :</span><span class="sxs-lookup"><span data-stu-id="d3830-134">The following code example prints the display names of all audio-rendering endpoint devices in the system:</span></span>


```C++
//-----------------------------------------------------------
// This function enumerates all active (plugged in) audio
// rendering endpoint devices. It prints the friendly name
// and endpoint ID string of each endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

void PrintEndpointNames()
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDeviceCollection *pCollection = NULL;
    IMMDevice *pEndpoint = NULL;
    IPropertyStore *pProps = NULL;
    LPWSTR pwszID = NULL;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->EnumAudioEndpoints(
                        eRender, DEVICE_STATE_ACTIVE,
                        &pCollection);
    EXIT_ON_ERROR(hr)

    UINT  count;
    hr = pCollection->GetCount(&count);
    EXIT_ON_ERROR(hr)

    if (count == 0)
    {
        printf("No endpoints found.\n");
    }

    // Each loop prints the name of an endpoint device.
    for (ULONG i = 0; i < count; i++)
    {
        // Get pointer to endpoint number i.
        hr = pCollection->Item(i, &pEndpoint);
        EXIT_ON_ERROR(hr)

        // Get the endpoint ID string.
        hr = pEndpoint->GetId(&pwszID);
        EXIT_ON_ERROR(hr)
        
        hr = pEndpoint->OpenPropertyStore(
                          STGM_READ, &pProps);
        EXIT_ON_ERROR(hr)

        PROPVARIANT varName;
        // Initialize container for property value.
        PropVariantInit(&varName);

        // Get the endpoint's friendly-name property.
        hr = pProps->GetValue(
                       PKEY_Device_FriendlyName, &varName);
        EXIT_ON_ERROR(hr)

        // Print endpoint friendly name and endpoint ID.
        printf("Endpoint %d: \"%S\" (%S)\n",
               i, varName.pwszVal, pwszID);

        CoTaskMemFree(pwszID);
        pwszID = NULL;
        PropVariantClear(&varName);
        SAFE_RELEASE(pProps)
        SAFE_RELEASE(pEndpoint)
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    return;

Exit:
    printf("Error!\n");
    CoTaskMemFree(pwszID);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    SAFE_RELEASE(pEndpoint)
    SAFE_RELEASE(pProps)
}
```



<span data-ttu-id="d3830-135">La macro ayant échoué dans l’exemple de code précédent est définie dans le fichier d’en-tête winerror. h.</span><span class="sxs-lookup"><span data-stu-id="d3830-135">The FAILED macro in the preceding code example is defined in header file Winerror.h.</span></span>

<span data-ttu-id="d3830-136">Dans l’exemple de code précédent, le corps de la boucle **for** de la fonction PrintEndpointNames appelle la méthode [**IMMDevice :: GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) pour obtenir la [chaîne d’ID de point de terminaison](endpoint-id-strings.md) pour le périphérique de point de terminaison audio représenté par l’instance d’interface **IMMDevice** .</span><span class="sxs-lookup"><span data-stu-id="d3830-136">In the preceding code example, the **for**-loop body in the PrintEndpointNames function calls the [**IMMDevice::GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) method to obtain the [endpoint ID string](endpoint-id-strings.md) for the audio endpoint device that is represented by the **IMMDevice** interface instance.</span></span> <span data-ttu-id="d3830-137">La chaîne identifie de façon unique l’appareil par rapport à tous les autres périphériques de point de terminaison audio dans le système.</span><span class="sxs-lookup"><span data-stu-id="d3830-137">The string uniquely identifies the device with respect to all of the other audio endpoint devices in the system.</span></span> <span data-ttu-id="d3830-138">Un client peut utiliser la chaîne d’ID de point de terminaison pour créer une instance du périphérique de point de terminaison audio ultérieurement ou dans un processus différent en appelant la méthode [**IMMDeviceEnumerator :: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .</span><span class="sxs-lookup"><span data-stu-id="d3830-138">A client can use the endpoint ID string to create an instance of the audio endpoint device at a later time or in a different process by calling the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="d3830-139">Les clients doivent traiter le contenu de la chaîne d’ID de point de terminaison comme opaque.</span><span class="sxs-lookup"><span data-stu-id="d3830-139">Clients should treat the contents of the endpoint ID string as opaque.</span></span> <span data-ttu-id="d3830-140">Autrement dit, les clients ne doivent pas tenter d’analyser le contenu de la chaîne pour obtenir des informations sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d3830-140">That is, clients should not attempt to parse the contents of the string to obtain information about the device.</span></span> <span data-ttu-id="d3830-141">La raison en est que le format de chaîne n’est pas défini et peut passer d’une implémentation de l’API MMDevice à la suivante.</span><span class="sxs-lookup"><span data-stu-id="d3830-141">The reason is that the string format is undefined and might change from one implementation of the MMDevice API to the next.</span></span>

<span data-ttu-id="d3830-142">Les noms d’appareil conviviaux et les chaînes d’ID de point de terminaison obtenus par la fonction PrintEndpointNames dans l’exemple de code précédent sont identiques aux noms de périphérique convivial et aux chaînes d’ID de point de terminaison fournis par DirectSound pendant l’énumération de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d3830-142">The friendly device names and endpoint ID strings that are obtained by the PrintEndpointNames function in the preceding code example are identical to the friendly device names and endpoint ID strings that are provided by DirectSound during device enumeration.</span></span> <span data-ttu-id="d3830-143">Pour plus d’informations, consultez [événements audio pour les applications audio héritées](audio-events-for-legacy-audio-applications.md).</span><span class="sxs-lookup"><span data-stu-id="d3830-143">For more information, see [Audio Events for Legacy Audio Applications](audio-events-for-legacy-audio-applications.md).</span></span>

<span data-ttu-id="d3830-144">Dans l’exemple de code précédent, la fonction PrintEndpointNames appelle la fonction **CoCreateInstance** pour créer un énumérateur pour les périphériques de point de terminaison audio dans le système.</span><span class="sxs-lookup"><span data-stu-id="d3830-144">In the preceding code example, the PrintEndpointNames function calls the **CoCreateInstance** function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="d3830-145">À moins que le programme appelant n’appelait auparavant la fonction **CoInitialize** ou **CoInitializeEx** pour initialiser la bibliothèque com, l’appel **CoCreateInstance** échouera.</span><span class="sxs-lookup"><span data-stu-id="d3830-145">Unless the calling program previously called either the **CoInitialize** or **CoInitializeEx** function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="d3830-146">Pour plus d’informations sur **CoCreateInstance**, **CoInitialize** et **CoInitializeEx**, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="d3830-146">For more information about **CoCreateInstance**, **CoInitialize**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="d3830-147">Pour plus d’informations sur les interfaces **IMMDeviceEnumerator**, **IMMDeviceCollection** et **IMMDevice** , consultez [API MMDevice](mmdevice-api.md).</span><span class="sxs-lookup"><span data-stu-id="d3830-147">For more information about the **IMMDeviceEnumerator**, **IMMDeviceCollection**, and **IMMDevice** interfaces, see [MMDevice API](mmdevice-api.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3830-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3830-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3830-149">Périphériques de point de terminaison audio</span><span class="sxs-lookup"><span data-stu-id="d3830-149">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> </dl>

 

 



