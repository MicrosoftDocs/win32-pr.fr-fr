---
description: Récupération des événements de service pris en charge
ms.assetid: 1bf3aa08-7ffc-417f-a67e-9eee042337b9
title: Récupération des événements de service pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc1df4c8255a4dc2a1297ae99216437ac3b4c9
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423469"
---
# <a name="retrieving-supported-service-events"></a>Récupération des événements de service pris en charge

L’application WpdServicesApiSample comprend du code qui montre comment une application peut récupérer les événements pris en charge par un service de contacts donné en appelant des méthodes sur les interfaces suivantes.



| Interface                | Description    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Utilisé pour récupérer l’interface **IPortableDeviceServiceCapabilities** pour accéder aux événements pris en charge. |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Fournit l’accès aux événements et attributs d’événement pris en charge.                                         |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Contient la liste des événements pris en charge.                                                                |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | Contient les attributs d’un événement donné.                                                            |



 

Quand l’utilisateur choisit l’option « 4 » sur la ligne de commande, l’application appelle la méthode **ListSupportedEvents** qui se trouve dans le module ServiceCapabilities. cpp.

Notez qu’avant de récupérer la liste des événements, l’exemple d’application ouvre un service de contacts sur un appareil connecté.

Dans WPD, un événement est décrit par son nom, ses options et ses paramètres. Le nom de l’événement est une chaîne conviviale de script, par exemple « MyCustomEvent ». Les options d’événement indiquent si un événement donné est diffusé à tous les clients et si cet événement prend en charge l’exécution automatique. Les attributs du paramètre d’événement incluent les attributs PROPERTYKEY et VARTYPE d’un paramètre donné.

Quatre méthodes du module ServiceCapabilities. cpp prennent en charge la récupération des événements pris en charge pour le service de contacts donné : **ListSupportedEvents**, **DisplayEvent**, **DisplayEventOptions** et **DisplayEventParameters**. La méthode **ListSupportedEvents** récupère le nombre d’événements pris en charge et l’identificateur GUID pour chaque événement. La méthode **DisplayEvent** affiche le nom ou le GUID de l’événement, puis appelle **DisplayEventOptions** et **DisplayEventParameters** pour afficher les données liées aux événements.

La méthode **ListSupportedEvents** appelle la méthode [**IPortableDeviceService :: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) pour récupérer une interface [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . À l’aide de cette interface, elle récupère les événements pris en charge en appelant la méthode [**IPortableDeviceServiceCapabilities :: GetSupportedEvents**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedevents) . La méthode **GetSupportedEvents** récupère les GUID pour chaque événement pris en charge par le service et copie ces GUID dans un objet [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .

Le code suivant illustre la récupération des événements de service pris en charge.


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



Une fois que la méthode **ListSupportedEvents** a récupéré les GUID représentant chaque événement pris en charge par le service donné, elle appelle la méthode **DisplayEvent** pour récupérer des données spécifiques à l’événement. Ces données incluent le nom de l’événement, ses options (diffusion ou lecture automatique), les GUID des paramètres, les types de paramètres, etc.

La méthode **DisplayEvent** appelle la méthode [**IPortableDeviceServiceCapabilities :: GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) pour récupérer une collection d’attributs pour l’événement donné. Il appelle ensuite la méthode [**IPortableDeviceValues :: GetStringValue**](iportabledevicevalues-getstringvalue.md) et demande que le pilote retourne un nom convivial pour l’événement donné. Ensuite, **DisplayEvent** appelle [**IPortableDeviceValues :: GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md) pour récupérer les options d’événement. Enfin, DisplayEvent appelle [**IPortableDeviceValues :: GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) pour récupérer la liste des paramètres d’événement. Il passe les données retournées par ces méthodes aux fonctions d’assistance **DisplayEventOptions** et **DisplayEventParameters** , qui restituent les options et les informations de paramètre pour l’événement donné.

Le code suivant utilise la méthode **DisplayEvent** .


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



La fonction d’assistance **DisplayEventOptions** reçoit un objet [**IPortableDeviceValues**](iportabledevicevalues.md) qui contient les données d’option de l’événement. Il appelle ensuite la méthode [**IPortableDeviceValues :: GetBoolValue**](iportabledevicevalues-getboolvalue.md) pour récupérer les données d’options. À l’aide de ces données, elle affiche une chaîne indiquant si les options de diffusion et d’exécution automatique sont prises en charge.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



