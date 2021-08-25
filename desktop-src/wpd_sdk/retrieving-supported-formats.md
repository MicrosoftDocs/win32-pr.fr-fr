---
description: Récupération des formats de service pris en charge
ms.assetid: b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec
title: Récupération des formats de service pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccbaa5678d12e4393f377bb0ae0a399634b247ceb9bd54e1d815d4e9f7e5a763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806669"
---
# <a name="retrieving-supported-service-formats"></a>Récupération des formats de service pris en charge

L’application WpdServicesApiSample comprend du code qui montre comment une application peut récupérer les formats pris en charge par un service de contacts donné en appelant les méthodes des interfaces dans le tableau suivant.



| Interface | Description   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Utilisé pour récupérer l’interface **IPortableDeviceServiceCapabilities** pour accéder aux événements pris en charge. |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Fournit l’accès aux événements et attributs d’événement pris en charge.                                         |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Contient la liste des formats pris en charge.                                                               |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | Contient les attributs d’un format donné.                                                           |



 

Quand l’utilisateur choisit l’option « 3 » sur la ligne de commande, l’application appelle la méthode **ListSupportedFormats** qui se trouve dans le module ServiceCapabilities. cpp.

Notez qu’avant de récupérer la liste des événements, l’exemple d’application ouvre un service de contacts sur un appareil connecté.

Dans WPD, un format est décrit par des attributs qui spécifient le nom et (éventuellement) le type MIME d’un format donné. Ces attributs sont définis dans le fichier d’en-tête thePortableDevice. h. Pour obtenir une description des attributs pris en charge, reportez-vous à la rubrique [attributs](attributes.md) .

Dans le cas de l’exemple d’application, si WpdServiceSampleDriver est le seul appareil installé, le pilote retourne deux formats pris en charge pour son service de contact : « AbstractContactFormat » et « VCard2Format ». Ces formats correspondent aux attributs **de \_ \_ \_ \_ contact abstrait au format d’objet wpd** et au format d' **\_ objet wpd \_ \_ VCARD2** trouvés dans PortableDevice. h.

Deux méthodes du module ServiceCapabilities. cpp prennent en charge la récupération des formats pris en charge pour le service de contacts : **ListSupportedFormats** et **displayFormat**. La première récupère l’identificateur GUID pour chaque format pris en charge. Ce dernier convertit ce GUID en une chaîne conviviale.

La méthode **ListSupportedFormats** appelle la méthode [**IPortableDeviceService :: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) pour récupérer une interface [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . À l’aide de cette interface, elle récupère les formats pris en charge en appelant la méthode [**IPortableDeviceServiceCapabilities :: GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) . La méthode **GetSupportedFormats** récupère le GUID pour chaque format pris en charge par le service et copie ce GUID dans un objet [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .

Le code suivant utilise la méthode **ListSupportedFormats** .


```C++
// List all supported formats on the service
void ListSupportedFormats(
    IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumFormats    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pFormats;

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

    // Get all formats supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedFormats(&pFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get supported formats from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported formats found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pFormats->GetCount(&dwNumFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported formats, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Formats Found on the service\n\n", dwNumFormats);

    // Loop through each format and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumFormats; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pFormats->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a format.  It is assumed that
                // formats are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayFormat(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



Une fois que la méthode **ListSupportedFormats** a extrait le GUID pour chaque format pris en charge par le service donné, elle appelle la méthode **displayFormat** pour afficher le nom convivial du script pour chaque format ; par exemple, « VCard2 ».

La méthode **displayFormat** appelle la méthode [**IPortableDeviceServiceCapabilities :: GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) pour récupérer une collection d’attributs pour le GUID de format donné. Il appelle ensuite la méthode [**IPortableDeviceValues :: GetStringValue**](iportabledevicevalues-getstringvalue.md) et demande que le pilote retourne un nom convivial du script pour le format donné.

Le code suivant utilise la méthode **displayFormat** .


```C++
// Display basic information about a format
void DisplayFormat(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Format)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    HRESULT hr = pCapabilities->GetFormatAttributes(Format, &pAttributes);

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        hr = pAttributes->GetStringValue(WPD_FORMAT_ATTRIBUTE_NAME, &pszFormatName);

        // Display the name of the format if it is available, otherwise fall back to displaying the GUID.
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszFormatName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Format));
        }       

        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



