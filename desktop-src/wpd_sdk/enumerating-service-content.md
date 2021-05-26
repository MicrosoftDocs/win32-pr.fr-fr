---
description: Énumération du contenu du service
ms.assetid: 4af4201c-d3f6-4630-91ec-6509c51871a5
title: Énumération du contenu du service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2b701bdab867e96bc9658e2624ea18aa65dfc33
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424249"
---
# <a name="enumerating-service-content"></a><span data-ttu-id="8e6ce-103">Énumération du contenu du service</span><span class="sxs-lookup"><span data-stu-id="8e6ce-103">Enumerating Service Content</span></span>

<span data-ttu-id="8e6ce-104">Une fois que votre application a ouvert un service, elle peut commencer à effectuer des opérations liées au service.</span><span class="sxs-lookup"><span data-stu-id="8e6ce-104">After your application opens a service, it can begin performing service-related operations.</span></span> <span data-ttu-id="8e6ce-105">Dans le cas de l’application WpdServicesApiSample, l’une de ces opérations est l’énumération du contenu pour un service de contacts donné.</span><span class="sxs-lookup"><span data-stu-id="8e6ce-105">In the case of the WpdServicesApiSample application, one of these operations is the enumeration of content for a given Contacts service.</span></span> <span data-ttu-id="8e6ce-106">Le tableau suivant décrit les interfaces utilisées.</span><span class="sxs-lookup"><span data-stu-id="8e6ce-106">The following table describes the interfaces used.</span></span>



| <span data-ttu-id="8e6ce-107">Interface</span><span class="sxs-lookup"><span data-stu-id="8e6ce-107">Interface</span></span>                                                            | <span data-ttu-id="8e6ce-108">Description</span><span class="sxs-lookup"><span data-stu-id="8e6ce-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e6ce-109">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="8e6ce-109">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | <span data-ttu-id="8e6ce-110">Utilisé pour récupérer l’interface IPortableDeviceContent2 pour accéder au contenu sur le service.</span><span class="sxs-lookup"><span data-stu-id="8e6ce-110">Used to retrieve the IPortableDeviceContent2 interface to access content on the service.</span></span>         |
| [<span data-ttu-id="8e6ce-111">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="8e6ce-111">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | <span data-ttu-id="8e6ce-112">Utilisé pour récupérer l’interface IEnumPortableDeviceObjectIDs pour énumérer des objets sur le service.</span><span class="sxs-lookup"><span data-stu-id="8e6ce-112">Used to retrieve the IEnumPortableDeviceObjectIDs interface to enumerate objects on the service.</span></span> |
| [<span data-ttu-id="8e6ce-113">**IEnumPortableDeviceObjectIDs**</span><span class="sxs-lookup"><span data-stu-id="8e6ce-113">**IEnumPortableDeviceObjectIDs**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids) | <span data-ttu-id="8e6ce-114">Utilisé pour énumérer des objets sur le service.</span><span class="sxs-lookup"><span data-stu-id="8e6ce-114">Used to enumerate objects on the service.</span></span>                                                        |



 

<span data-ttu-id="8e6ce-115">Le code d’énumération du contenu se trouve dans le module ContentEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="8e6ce-115">The content enumeration code is found in the ContentEnumeration.cpp module.</span></span> <span data-ttu-id="8e6ce-116">Ce code se trouve dans les méthodes **EnumerateAllContent** et **RecursiveEnumerate** .</span><span class="sxs-lookup"><span data-stu-id="8e6ce-116">This code resides in the **EnumerateAllContent** and the **RecursiveEnumerate** methods.</span></span> <span data-ttu-id="8e6ce-117">La première méthode appelle la dernière.</span><span class="sxs-lookup"><span data-stu-id="8e6ce-117">The former method calls the latter.</span></span>

<span data-ttu-id="8e6ce-118">La méthode **EnumerateContent** prend un pointeur vers un objet [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) en tant que paramètre unique.</span><span class="sxs-lookup"><span data-stu-id="8e6ce-118">The **EnumerateContent** method takes a pointer to an [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) object as its one parameter.</span></span> <span data-ttu-id="8e6ce-119">Cet objet correspond à un service que l’application a ouvert précédemment quand elle a appelé la méthode [**IPortableDeviceService :: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) .</span><span class="sxs-lookup"><span data-stu-id="8e6ce-119">This object corresponds to a service that the application opened earlier when it called the [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) method.</span></span>

<span data-ttu-id="8e6ce-120">La méthode **EnumerateContent** crée un objet [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) et passe cet objet à la méthode [**IPortableDeviceService :: content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) .</span><span class="sxs-lookup"><span data-stu-id="8e6ce-120">The **EnumerateContent** method creates an [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) object and passes this object to the [**IPortableDeviceService::Content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) method.</span></span> <span data-ttu-id="8e6ce-121">Cette méthode récupère ensuite le contenu au niveau racine du service, puis commence à récupérer de façon récursive le contenu trouvé sous la racine.</span><span class="sxs-lookup"><span data-stu-id="8e6ce-121">This method, in turn, retrieves the content at the root level of the service, and then recursively begins to retrieve content found beneath the root.</span></span>

<span data-ttu-id="8e6ce-122">Le code suivant correspond à la méthode **EnumerateContent** .</span><span class="sxs-lookup"><span data-stu-id="8e6ce-122">The following code corresponds to the **EnumerateContent** method.</span></span>


```C++
// Enumerate all content on the service starting with the
// "DEVICE" object
void EnumerateAllContent(
    IPortableDeviceService* pService)
{
    HRESULT                          hr = S_OK;
    CComPtr<IPortableDeviceContent2> pContent;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    hr = pService->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



<span data-ttu-id="8e6ce-123">Le code suivant correspond à la méthode **RecursiveEnumerate** .</span><span class="sxs-lookup"><span data-stu-id="8e6ce-123">The following code corresponds to the **RecursiveEnumerate** method.</span></span> <span data-ttu-id="8e6ce-124">La méthode RecursiveEnumerate instancie une interface **IEnumPortableDeviceObjectIDs** pour l’objet parent fourni et appelle **IEnumPortableDeviceObjectIDs :: Next**, en extrayant un lot d’objets enfants immédiats.</span><span class="sxs-lookup"><span data-stu-id="8e6ce-124">The RecursiveEnumerate method instantiates an **IEnumPortableDeviceObjectIDs** interface for the supplied parent object, and calls **IEnumPortableDeviceObjectIDs::Next**, retrieving a batch of immediate child objects.</span></span> <span data-ttu-id="8e6ce-125">Pour chaque objet enfant, RecursiveEnumerate est rappelé pour retourner ses objets enfants descendants, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="8e6ce-125">For each child object, RecursiveEnumerate is called again to return its descendent child objects, and so on.</span></span>


```C++
// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                   pszObjectID,
    IPortableDeviceContent2* pContent)
{
    CComPtr<IEnumPortableDeviceObjectIDs> pEnumObjectIDs;

    // Print the object identifier being used as the parent during enumeration.
    printf("%ws\n",pszObjectID);

    // Get an IEnumPortableDeviceObjectIDs interface by calling EnumObjects with the
    // specified parent object identifier.
    HRESULT hr = pContent->EnumObjects(0,               // Flags are unused
                                       pszObjectID,     // Starting from the passed in object
                                       NULL,            // Filter is unused
                                       &pEnumObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent2, hr = 0x%lx\n",hr);
    }

    // Loop calling Next() while S_OK is being returned.
    while(hr == S_OK)
    {
        DWORD  cFetched = 0;
        PWSTR  szObjectIDArray[NUM_OBJECTS_TO_REQUEST] = {0};
        hr = pEnumObjectIDs->Next(NUM_OBJECTS_TO_REQUEST,   // Number of objects to request on each NEXT call
                                  szObjectIDArray,          // Array of PWSTR array which will be populated on each NEXT call
                                  &cFetched);               // Number of objects written to the PWSTR array
        if (SUCCEEDED(hr))
        {
            // Traverse the results of the Next() operation and recursively enumerate
            // Remember to free all returned object identifiers using CoTaskMemFree()
            for (DWORD dwIndex = 0; dwIndex < cFetched; dwIndex++)
            {
                RecursiveEnumerate(szObjectIDArray[dwIndex],pContent);

                // Free allocated PWSTRs after the recursive enumeration call has completed.
                CoTaskMemFree(szObjectIDArray[dwIndex]);
                szObjectIDArray[dwIndex] = NULL;
            }
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="8e6ce-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e6ce-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e6ce-127">**IEnumPortableDeviceObjectIDs**</span><span class="sxs-lookup"><span data-stu-id="8e6ce-127">**IEnumPortableDeviceObjectIDs**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[<span data-ttu-id="8e6ce-128">**Interface IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="8e6ce-128">**IPortableDeviceContent2 Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="8e6ce-129">**Interface IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="8e6ce-129">**IPortableDeviceService Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="8e6ce-130">Ouverture d’un service</span><span class="sxs-lookup"><span data-stu-id="8e6ce-130">Opening a Service</span></span>](opening-a-service.md)
</dt> <dt>

[<span data-ttu-id="8e6ce-131">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="8e6ce-131">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



