---
description: Récupération des formats de service pris en charge
ms.assetid: b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec
title: Récupération des formats de service pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed8021d8feefaaad3da7905e17e8c658dfb19e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521926"
---
# <a name="retrieving-supported-service-formats"></a><span data-ttu-id="b2f6b-103">Récupération des formats de service pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2f6b-103">Retrieving Supported Service Formats</span></span>

<span data-ttu-id="b2f6b-104">L’application WpdServicesApiSample comprend du code qui montre comment une application peut récupérer les formats pris en charge par un service de contacts donné en appelant les méthodes des interfaces dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b2f6b-104">The WpdServicesApiSample application includes code that demonstrates how an application can retrieve the formats supported by a given Contacts service by calling methods of the interfaces in the following table.</span></span>



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f6b-105">Interface</span><span class="sxs-lookup"><span data-stu-id="b2f6b-105">Interface</span></span>                                                                            | <span data-ttu-id="b2f6b-106">Description</span><span class="sxs-lookup"><span data-stu-id="b2f6b-106">Description</span></span>                                                                                           |
| [<span data-ttu-id="b2f6b-107">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="b2f6b-107">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | <span data-ttu-id="b2f6b-108">Utilisé pour récupérer l’interface **IPortableDeviceServiceCapabilities** pour accéder aux événements pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b2f6b-108">Used to retrieve the **IPortableDeviceServiceCapabilities** interface to access the supported events.</span></span> |
| [<span data-ttu-id="b2f6b-109">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b2f6b-109">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | <span data-ttu-id="b2f6b-110">Fournit l’accès aux événements et attributs d’événement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b2f6b-110">Provides access to the supported events and event attributes.</span></span>                                         |
| [<span data-ttu-id="b2f6b-111">**IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="b2f6b-111">**IPortableDevicePropVariantCollection**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="b2f6b-112">Contient la liste des formats pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b2f6b-112">Contains the list of supported formats.</span></span>                                                               |
| [<span data-ttu-id="b2f6b-113">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="b2f6b-113">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                               | <span data-ttu-id="b2f6b-114">Contient les attributs d’un format donné.</span><span class="sxs-lookup"><span data-stu-id="b2f6b-114">Contains the attributes for a given format.</span></span>                                                           |



 

<span data-ttu-id="b2f6b-115">Quand l’utilisateur choisit l’option « 3 » sur la ligne de commande, l’application appelle la méthode **ListSupportedFormats** qui se trouve dans le module ServiceCapabilities. cpp.</span><span class="sxs-lookup"><span data-stu-id="b2f6b-115">When the user chooses option "3" at the command line, the application invokes the **ListSupportedFormats** method that is found in the ServiceCapabilities.cpp module.</span></span>

<span data-ttu-id="b2f6b-116">Notez qu’avant de récupérer la liste des événements, l’exemple d’application ouvre un service de contacts sur un appareil connecté.</span><span class="sxs-lookup"><span data-stu-id="b2f6b-116">Note that prior to retrieving the list of events, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="b2f6b-117">Dans WPD, un format est décrit par des attributs qui spécifient le nom et (éventuellement) le type MIME d’un format donné.</span><span class="sxs-lookup"><span data-stu-id="b2f6b-117">In WPD, a format is described by attributes that specify the name and (optionally) the MIME type of a given format.</span></span> <span data-ttu-id="b2f6b-118">Ces attributs sont définis dans le fichier d’en-tête thePortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="b2f6b-118">These attributes are defined in thePortableDevice.h header file.</span></span> <span data-ttu-id="b2f6b-119">Pour obtenir une description des attributs pris en charge, reportez-vous à la rubrique [attributs](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="b2f6b-119">For a description of supported attributes, refer to the [Attributes](attributes.md) topic.</span></span>

<span data-ttu-id="b2f6b-120">Dans le cas de l’exemple d’application, si WpdServiceSampleDriver est le seul appareil installé, le pilote retourne deux formats pris en charge pour son service de contact : « AbstractContactFormat » et « VCard2Format ».</span><span class="sxs-lookup"><span data-stu-id="b2f6b-120">In the case of the sample application, if the WpdServiceSampleDriver is the only installed device, the driver returns two supported formats for its Contact service: "AbstractContactFormat" and "VCard2Format".</span></span> <span data-ttu-id="b2f6b-121">Ces formats correspondent aux attributs **de \_ \_ \_ \_ contact abstrait au format d’objet wpd** et au format d' **\_ objet wpd \_ \_ VCARD2** trouvés dans PortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="b2f6b-121">These formats correspond to the **WPD\_OBJECT\_FORMAT\_ABSTRACT\_CONTACT** and the **WPD\_OBJECT\_FORMAT\_VCARD2** attributes found in PortableDevice.h.</span></span>

<span data-ttu-id="b2f6b-122">Deux méthodes du module ServiceCapabilities. cpp prennent en charge la récupération des formats pris en charge pour le service de contacts : **ListSupportedFormats** et **displayFormat**.</span><span class="sxs-lookup"><span data-stu-id="b2f6b-122">Two methods in the ServiceCapabilities.cpp module support the retrieval of supported formats for the Contacts service: **ListSupportedFormats** and **DisplayFormat**.</span></span> <span data-ttu-id="b2f6b-123">La première récupère l’identificateur GUID pour chaque format pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b2f6b-123">The former retrieves the GUID identifier for each supported format.</span></span> <span data-ttu-id="b2f6b-124">Ce dernier convertit ce GUID en une chaîne conviviale.</span><span class="sxs-lookup"><span data-stu-id="b2f6b-124">The latter converts this GUID into a user-friendly string.</span></span>

<span data-ttu-id="b2f6b-125">La méthode **ListSupportedFormats** appelle la méthode [**IPortableDeviceService :: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) pour récupérer une interface [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="b2f6b-125">The **ListSupportedFormats** method invokes the [**IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="b2f6b-126">À l’aide de cette interface, elle récupère les formats pris en charge en appelant la méthode [**IPortableDeviceServiceCapabilities :: GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) .</span><span class="sxs-lookup"><span data-stu-id="b2f6b-126">Using this interface, it retrieves the supported formats by calling the [**IPortableDeviceServiceCapabilities::GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) method.</span></span> <span data-ttu-id="b2f6b-127">La méthode **GetSupportedFormats** récupère le GUID pour chaque format pris en charge par le service et copie ce GUID dans un objet [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="b2f6b-127">The **GetSupportedFormats** method retrieves the GUID for each format supported by the service and copies that GUID into an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="b2f6b-128">Le code suivant utilise la méthode **ListSupportedFormats** .</span><span class="sxs-lookup"><span data-stu-id="b2f6b-128">The following code uses the **ListSupportedFormats** method.</span></span>


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



<span data-ttu-id="b2f6b-129">Une fois que la méthode **ListSupportedFormats** a extrait le GUID pour chaque format pris en charge par le service donné, elle appelle la méthode **displayFormat** pour afficher le nom convivial du script pour chaque format ; par exemple, « VCard2 ».</span><span class="sxs-lookup"><span data-stu-id="b2f6b-129">After the **ListSupportedFormats** method retrieves the GUID for each format supported by the given service, it invokes the **DisplayFormat** method to display the script friendly name for each format; for example, "VCard2".</span></span>

<span data-ttu-id="b2f6b-130">La méthode **displayFormat** appelle la méthode [**IPortableDeviceServiceCapabilities :: GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) pour récupérer une collection d’attributs pour le GUID de format donné.</span><span class="sxs-lookup"><span data-stu-id="b2f6b-130">The **DisplayFormat** method invokes the [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method retrieve a collection of attributes for the given format GUID.</span></span> <span data-ttu-id="b2f6b-131">Il appelle ensuite la méthode [**IPortableDeviceValues :: GetStringValue**](iportabledevicevalues-getstringvalue.md) et demande que le pilote retourne un nom convivial du script pour le format donné.</span><span class="sxs-lookup"><span data-stu-id="b2f6b-131">It then calls the [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) method and requests that the driver return a script-friendly name for the given format.</span></span>

<span data-ttu-id="b2f6b-132">Le code suivant utilise la méthode **displayFormat** .</span><span class="sxs-lookup"><span data-stu-id="b2f6b-132">The following code uses the **DisplayFormat** method.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b2f6b-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2f6b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2f6b-134">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="b2f6b-134">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="b2f6b-135">**IPortableDeviceServiceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b2f6b-135">**IPortableDeviceServiceCapabilities**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[<span data-ttu-id="b2f6b-136">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="b2f6b-136">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="b2f6b-137">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="b2f6b-137">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



