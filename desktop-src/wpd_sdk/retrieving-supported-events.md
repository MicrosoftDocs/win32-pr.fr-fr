---
description: Récupération des événements de service pris en charge
ms.assetid: 1bf3aa08-7ffc-417f-a67e-9eee042337b9
title: Récupération des événements de service pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f515b65b8ed062c346777224a64539f5229a704a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530206"
---
# <a name="retrieving-supported-service-events"></a><span data-ttu-id="d4fbe-103">Récupération des événements de service pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4fbe-103">Retrieving Supported Service Events</span></span>

<span data-ttu-id="d4fbe-104">L’application WpdServicesApiSample comprend du code qui montre comment une application peut récupérer les événements pris en charge par un service de contacts donné en appelant des méthodes sur les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-104">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the events supported by a given Contacts service by calling methods on the following interfaces.</span></span>



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4fbe-105">Interface</span><span class="sxs-lookup"><span data-stu-id="d4fbe-105">Interface</span></span>                                                                            | <span data-ttu-id="d4fbe-106">Description</span><span class="sxs-lookup"><span data-stu-id="d4fbe-106">Description</span></span>                                                                                           |
| [<span data-ttu-id="d4fbe-107">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="d4fbe-107">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="d4fbe-108">Utilisé pour récupérer l’interface **IPortableDeviceServiceCapabilities** pour accéder aux événements pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-108">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported events.</span></span> |
| [<span data-ttu-id="d4fbe-109">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d4fbe-109">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="d4fbe-110">Fournit l’accès aux événements et attributs d’événement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-110">Provides access to the supported events and event attributes.</span></span>                                         |
| [<span data-ttu-id="d4fbe-111">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="d4fbe-111">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="d4fbe-112">Contient la liste des événements pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-112">Contains the list of supported events.</span></span>                                                                |
| [<span data-ttu-id="d4fbe-113">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="d4fbe-113">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="d4fbe-114">Contient les attributs d’un événement donné.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-114">Contains the attributes for a given event.</span></span>                                                            |



 

<span data-ttu-id="d4fbe-115">Quand l’utilisateur choisit l’option « 4 » sur la ligne de commande, l’application appelle la méthode **ListSupportedEvents** qui se trouve dans le module ServiceCapabilities. cpp.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-115">When the user chooses option "4" at the command line, the application invokes the **ListSupportedEvents** method that is found in the ServiceCapabilities.cpp module.</span></span>

<span data-ttu-id="d4fbe-116">Notez qu’avant de récupérer la liste des événements, l’exemple d’application ouvre un service de contacts sur un appareil connecté.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-116">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="d4fbe-117">Dans WPD, un événement est décrit par son nom, ses options et ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-117">In WPD, an event is described by its name, options, and parameters.</span></span> <span data-ttu-id="d4fbe-118">Le nom de l’événement est une chaîne conviviale de script, par exemple « MyCustomEvent ».</span><span class="sxs-lookup"><span data-stu-id="d4fbe-118">The event name is a script-friendly string, for example, "MyCustomEvent".</span></span> <span data-ttu-id="d4fbe-119">Les options d’événement indiquent si un événement donné est diffusé à tous les clients et si cet événement prend en charge l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-119">The event options indicate whether a given event is broadcast to all clients and whether that event supports autoplay.</span></span> <span data-ttu-id="d4fbe-120">Les attributs du paramètre d’événement incluent les attributs PROPERTYKEY et VARTYPE d’un paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-120">The event parameter attributes includes a given parameter's PROPERTYKEY and VARTYPE.</span></span>

<span data-ttu-id="d4fbe-121">Quatre méthodes du module ServiceCapabilities. cpp prennent en charge la récupération des événements pris en charge pour le service de contacts donné : **ListSupportedEvents**, **DisplayEvent**, **DisplayEventOptions** et **DisplayEventParameters**.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-121">Four methods in the ServiceCapabilities.cpp module support the retrieval of supported events for the given Contacts service: **ListSupportedEvents**, **DisplayEvent**, **DisplayEventOptions**, and **DisplayEventParameters**.</span></span> <span data-ttu-id="d4fbe-122">La méthode **ListSupportedEvents** récupère le nombre d’événements pris en charge et l’identificateur GUID pour chaque événement.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-122">The **ListSupportedEvents** method retrieves a count of supported events and the GUID identifier for each event.</span></span> <span data-ttu-id="d4fbe-123">La méthode **DisplayEvent** affiche le nom ou le GUID de l’événement, puis appelle **DisplayEventOptions** et **DisplayEventParameters** pour afficher les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-123">The **DisplayEvent** method displays the event name or GUID, and then calls **DisplayEventOptions** and **DisplayEventParameters** to display the event-related data.</span></span>

<span data-ttu-id="d4fbe-124">La méthode **ListSupportedEvents** appelle la méthode [**IPortableDeviceService :: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) pour récupérer une interface [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="d4fbe-124">The **ListSupportedEvents** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="d4fbe-125">À l’aide de cette interface, elle récupère les événements pris en charge en appelant la méthode [**IPortableDeviceServiceCapabilities :: GetSupportedEvents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) .</span><span class="sxs-lookup"><span data-stu-id="d4fbe-125">Using this interface, it retrieves the supported events by calling the [**IPortableDeviceServiceCapabilities::GetSupportedEvents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) method.</span></span> <span data-ttu-id="d4fbe-126">La méthode **GetSupportedEvents** récupère les GUID pour chaque événement pris en charge par le service et copie ces GUID dans un objet [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="d4fbe-126">The **GetSupportedEvents** method retrieves the GUIDs for each event supported by the service and copies those GUIDs into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="d4fbe-127">Le code suivant illustre la récupération des événements de service pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-127">The following code illustrates retrieving supported service events.</span></span>


```C++
// List all supported events on the service
void ListSupportedEvents(
    IPortableDeviceService* pService)
{
    HRESULT hr          = S_OK;
    DWORD   dwNumEvents = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pEvents;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all events supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedEvents(&pEvents);
        if (FAILED(hr))
        {
            printf("! Failed to get supported events from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported events found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pEvents->GetCount(&dwNumEvents);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Events Found on the service\n\n", dwNumEvents);

    // Loop through each event and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumEvents; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pEvents->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have an event.  It is assumed that
                // events are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayEvent(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



<span data-ttu-id="d4fbe-128">Une fois que la méthode **ListSupportedEvents** a récupéré les GUID représentant chaque événement pris en charge par le service donné, elle appelle la méthode **DisplayEvent** pour récupérer des données spécifiques à l’événement.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-128">After the **ListSupportedEvents** method retrieves the GUIDs representing each event supported by the given service, it invokes the **DisplayEvent** method to retrieve event-specific data.</span></span> <span data-ttu-id="d4fbe-129">Ces données incluent le nom de l’événement, ses options (diffusion ou lecture automatique), les GUID des paramètres, les types de paramètres, etc.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-129">This data includes the event name, its options (broadcast or autoplay), parameter GUIDs, parameter types, and so on.</span></span>

<span data-ttu-id="d4fbe-130">La méthode **DisplayEvent** appelle la méthode [**IPortableDeviceServiceCapabilities :: GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) pour récupérer une collection d’attributs pour l’événement donné.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-130">The **DisplayEvent** method invokes the [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) method to retrieve a collection of attributes for the given event.</span></span> <span data-ttu-id="d4fbe-131">Il appelle ensuite la méthode [**IPortableDeviceValues :: GetStringValue**](iportabledevicevalues-getstringvalue.md) et demande que le pilote retourne un nom convivial pour l’événement donné.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-131">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method and requests that the driver return a user-friendly name for the given event.</span></span> <span data-ttu-id="d4fbe-132">Ensuite, **DisplayEvent** appelle [**IPortableDeviceValues :: GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) pour récupérer les options d’événement.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-132">Next, **DisplayEvent** calls the [**IPortableDeviceValues::GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) to retrieve the event options.</span></span> <span data-ttu-id="d4fbe-133">Enfin, DisplayEvent appelle [**IPortableDeviceValues :: GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) pour récupérer la liste des paramètres d’événement.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-133">Finally, DisplayEvent calls the [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) to retrieve the list of event parameters.</span></span> <span data-ttu-id="d4fbe-134">Il passe les données retournées par ces méthodes aux fonctions d’assistance **DisplayEventOptions** et **DisplayEventParameters** , qui restituent les options et les informations de paramètre pour l’événement donné.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-134">It passes the data returned by these methods to the **DisplayEventOptions** and the **DisplayEventParameters** helper functions, which render the options and parameter information for the given event.</span></span>

<span data-ttu-id="d4fbe-135">Le code suivant utilise la méthode **DisplayEvent** .</span><span class="sxs-lookup"><span data-stu-id="d4fbe-135">The following code uses the **DisplayEvent** method.</span></span>


```C++
// Display basic information about an event
void DisplayEvent(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Event)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the event attributes which describe the event
    HRESULT hr = pCapabilities->GetEventAttributes(Event, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the event attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the event if it is available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_EVENT_ATTRIBUTE_NAME, &pszFormatName);
        if (SUCCEEDED(hr))
        {
            printf("%ws\n", pszFormatName);
        }
        else
        {
            printf("%ws\n", (PWSTR)CGuidToString(Event));
        }       

        // Display the event options
        hr = pAttributes->GetIPortableDeviceValuesValue(WPD_EVENT_ATTRIBUTE_OPTIONS, &pOptions);
        if (SUCCEEDED(hr))
        {
            DisplayEventOptions(pOptions);
        }
        else
        {
            printf("! Failed to get the event options, hr = 0x%lx\n", hr);
        }       

        // Display the event parameters
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_EVENT_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayEventParameters(pCapabilities, Event, pParameters);
        }
        else
        {
            printf("! Failed to get the event parameters, hr = 0x%lx\n", hr);
        }       
        
        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



<span data-ttu-id="d4fbe-136">La fonction d’assistance **DisplayEventOptions** reçoit un objet [**IPortableDeviceValues**](iportabledevicevalues.md) qui contient les données d’option de l’événement.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-136">The **DisplayEventOptions** helper function receives an [**IPortableDeviceValues**](iportabledevicevalues.md) object which contains the event's option data.</span></span> <span data-ttu-id="d4fbe-137">Il appelle ensuite la méthode [**IPortableDeviceValues :: GetBoolValue**](iportabledevicevalues-getboolvalue.md) pour récupérer les données d’options.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-137">It then calls the [**IPortableDeviceValues::GetBoolValue**](iportabledevicevalues-getboolvalue.md) method to retrieve the options data.</span></span> <span data-ttu-id="d4fbe-138">À l’aide de ces données, elle affiche une chaîne indiquant si les options de diffusion et d’exécution automatique sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d4fbe-138">Using this data, it renders a string indicating whether the broadcast and autoplay options are supported.</span></span>


```C++
// Display the basic event options.
void DisplayEventOptions(
    IPortableDeviceValues* pOptions)
{
    printf("\tEvent Options:\n");
    // Read the WPD_EVENT_OPTION_IS_BROADCAST_EVENT value to see if the event is
    // a broadcast event. If the read fails, assume FALSE
    BOOL  bIsBroadcastEvent = FALSE;
    pOptions->GetBoolValue(WPD_EVENT_OPTION_IS_BROADCAST_EVENT, &bIsBroadcastEvent);
    printf("\tWPD_EVENT_OPTION_IS_BROADCAST_EVENT = %ws\n",bIsBroadcastEvent ? L"TRUE" : L"FALSE");
}
```



## <a name="related-topics"></a><span data-ttu-id="d4fbe-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d4fbe-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4fbe-140">**IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="d4fbe-140">**IPortableDeviceKeyCollection**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="d4fbe-141">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="d4fbe-141">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="d4fbe-142">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d4fbe-142">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="d4fbe-143">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="d4fbe-143">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d4fbe-144">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="d4fbe-144">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



