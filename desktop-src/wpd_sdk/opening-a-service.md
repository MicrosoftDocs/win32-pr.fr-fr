---
description: Ouverture d’un service
ms.assetid: 722d657d-332a-40df-ac30-bc2050deda74
title: Ouverture d’un service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0bcccc6c3769173bfee72e73d7cbf68435b0ba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529524"
---
# <a name="opening-a-service"></a><span data-ttu-id="e3de1-103">Ouverture d’un service</span><span class="sxs-lookup"><span data-stu-id="e3de1-103">Opening a Service</span></span>

<span data-ttu-id="e3de1-104">Pour que votre application puisse effectuer des opérations sur un service, par exemple, en énumérant du contenu ou en extrayant des descriptions d’événements ou de méthodes pris en charge, il doit ouvrir le service.</span><span class="sxs-lookup"><span data-stu-id="e3de1-104">Before your application can perform operations on a service, for example, enumerating content or retrieving descriptions of supported events or methods, it must open the service.</span></span> <span data-ttu-id="e3de1-105">Dans l’application WpdServicesApiSample, cette tâche est présentée dans le module ServiceEnumeration. cpp à l’aide des interfaces décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e3de1-105">In the WpdServicesApiSample application, this task is demonstrated in the ServiceEnumeration.cpp module using the interfaces described in the following table.</span></span>



|                                                                        |                                                    |
|------------------------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="e3de1-106">Interface</span><span class="sxs-lookup"><span data-stu-id="e3de1-106">Interface</span></span>                                                              | <span data-ttu-id="e3de1-107">Description</span><span class="sxs-lookup"><span data-stu-id="e3de1-107">Description</span></span>                                        |
| [<span data-ttu-id="e3de1-108">**IPortableDeviceServiceManager**</span><span class="sxs-lookup"><span data-stu-id="e3de1-108">**IPortableDeviceServiceManager**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager) | <span data-ttu-id="e3de1-109">Utilisé pour énumérer les services sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="e3de1-109">Used to enumerate the services on a device.</span></span>        |
| [<span data-ttu-id="e3de1-110">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="e3de1-110">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | <span data-ttu-id="e3de1-111">Utilisé pour ouvrir une connexion à un service d’appareil.</span><span class="sxs-lookup"><span data-stu-id="e3de1-111">Used to open a connection to a device service.</span></span>     |
| [<span data-ttu-id="e3de1-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="e3de1-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                 | <span data-ttu-id="e3de1-113">Utilisé pour contenir les informations du client de l’application.</span><span class="sxs-lookup"><span data-stu-id="e3de1-113">Used to hold the application's client information.</span></span> |



 

<span data-ttu-id="e3de1-114">La méthode qui ouvre un service est [**IPortableDeviceService :: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span><span class="sxs-lookup"><span data-stu-id="e3de1-114">The method that opens a service is [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span></span> <span data-ttu-id="e3de1-115">Cette méthode accepte deux arguments : un identificateur plug-and-Play (PnP) pour le service et un objet [**IPortableDeviceValues**](iportabledevicevalues.md) qui contient les informations sur le client de l’application.</span><span class="sxs-lookup"><span data-stu-id="e3de1-115">This method takes two arguments: a Plug-and-Play (PnP) identifier for the service and an [**IPortableDeviceValues**](iportabledevicevalues.md) object that contains the application's client information.</span></span>

<span data-ttu-id="e3de1-116">Pour obtenir un identificateur PnP pour un service donné, votre application appelle la méthode [**IPortableDeviceServiceManager :: GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) .</span><span class="sxs-lookup"><span data-stu-id="e3de1-116">To obtain a PnP identifier for a given service, your application calls the [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) method.</span></span> <span data-ttu-id="e3de1-117">Cette méthode récupère un tableau d’identificateurs PnP pour les services d’un GUID de catégorie de service (par exemple, contacts de SERVICE).</span><span class="sxs-lookup"><span data-stu-id="e3de1-117">This method retrieves an array of PnP identifiers for services of a service category GUID (for example SERVICE Contacts).</span></span>

<span data-ttu-id="e3de1-118">L’exemple d’application de service récupère un identificateur PnP pour les services de contacts au sein de la méthode **EnumerateContactsServices** dans le module ServiceEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="e3de1-118">The sample Service application retrieves a PnP identifier for Contacts services within the **EnumerateContactsServices** method in the ServiceEnumeration.cpp module.</span></span> <span data-ttu-id="e3de1-119">L’exemple de code suivant est extrait de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e3de1-119">The following code sample is taken from this method.</span></span>


```C++
// For each device found, find the contacts service
for (dwIndex = 0; dwIndex < cPnpDeviceIDs; dwIndex++)
{
    DWORD   cPnpServiceIDs = 0;
    PWSTR   pPnpServiceID  = NULL;

    // First, pass NULL as the PWSTR array pointer to get the total number
    // of contacts services (SERVICE_Contacts) found on the device.
    // To find the total number of all services on the device, use GUID_DEVINTERFACE_WPD_SERVICE.
    hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, NULL, &cPnpServiceIDs);
    
    if (SUCCEEDED(hr) && (cPnpServiceIDs > 0))
    {                               
        // For simplicity, we are only using the first contacts service on each device
        cPnpServiceIDs = 1;
        hr = pServiceManager->GetDeviceServices(pPnpDeviceIDs[dwIndex], SERVICE_Contacts, &pPnpServiceID, &cPnpServiceIDs);

        if (SUCCEEDED(hr))
        {
            // We've found the service, display it and save its PnP Identifier
            ContactsServicePnpIDs.Add(pPnpServiceID);

            printf("[%d] ", static_cast<DWORD>(ContactsServicePnpIDs.GetCount()-1));

            // Display information about the device that contains this service.
            DisplayDeviceInformation(pServiceManager, pPnpServiceID);

            // ContactsServicePnpIDs now owns the memory for this string
            pPnpServiceID = NULL;
        }
        else
        {
            printf("! Failed to get the first contacts service from '%ws, hr = 0x%lx\n",pPnpDeviceIDs[dwIndex],hr);
        }
    }
}
```



<span data-ttu-id="e3de1-120">Une fois que votre application a récupéré l’identificateur PnP pour le service, elle peut configurer les informations du client et appeler [**IPortableDeviceService :: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span><span class="sxs-lookup"><span data-stu-id="e3de1-120">After your application retrieves the PnP identifier for the service, it can set up the client information and call [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open).</span></span>

<span data-ttu-id="e3de1-121">Dans l’exemple d’application, cette méthode est appelée dans **ChooseDeviceService** dans le module ServiceEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="e3de1-121">In the sample application, this method is called within **ChooseDeviceService** in the ServiceEnumeration.cpp module.</span></span>

<span data-ttu-id="e3de1-122">[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) prend en charge deux CLSID pour **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="e3de1-122">[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) supports two CLSIDs for **CoCreateInstance**.</span></span> <span data-ttu-id="e3de1-123">**CLSID \_ PortableDeviceService** retourne un pointeur **IPortableDeviceService** qui n’agrège pas le marshaleur libre de threads. **CLSID \_ PortableDeviceServiceFTM** est un nouveau CLSID qui retourne un pointeur **IPortableDeviceService** qui agrège le marshaleur libre de threads.</span><span class="sxs-lookup"><span data-stu-id="e3de1-123">**CLSID\_PortableDeviceService** returns an **IPortableDeviceService** pointer that does not aggregate the free-threaded marshaler; **CLSID\_PortableDeviceServiceFTM** is a new CLSID that returns an **IPortableDeviceService** pointer that aggregates the free-threaded marshaler.</span></span> <span data-ttu-id="e3de1-124">Les deux pointeurs prennent en charge la même fonctionnalité dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e3de1-124">Both pointers support the same functionality otherwise.</span></span>

<span data-ttu-id="e3de1-125">Les applications qui résident dans des cloisonnements à thread unique doivent utiliser le **CLSID \_ PortableDeviceServiceFTM** , car cela élimine la surcharge du marshaling de pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="e3de1-125">Applications that live in Single Threaded Apartments should use **CLSID\_PortableDeviceServiceFTM** as this eliminates the overhead of interface pointer marshaling.</span></span> <span data-ttu-id="e3de1-126">**CLSID \_ PortableDeviceService** est toujours pris en charge pour les applications héritées.</span><span class="sxs-lookup"><span data-stu-id="e3de1-126">**CLSID\_PortableDeviceService** is still supported for legacy applications.</span></span>


```C++
hr = CoCreateInstance(CLSID_PortableDeviceServiceFTM,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pService));
if (SUCCEEDED(hr))
{
    hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);
    if (FAILED(hr))
    {
        if (hr == E_ACCESSDENIED)
        {
            printf("Failed to Open the service for Read Write access, will open it for Read-only access instead\n");

            pClientInformation->SetUnsignedIntegerValue(WPD_CLIENT_DESIRED_ACCESS, GENERIC_READ);

            hr = pService->Open(ContactsServicesArray[uiCurrentService], pClientInformation);

            if (FAILED(hr))
            {
                printf("! Failed to Open the service for Read access, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            printf("! Failed to Open the service, hr = 0x%lx\n",hr);
        }
    }
```



## <a name="related-topics"></a><span data-ttu-id="e3de1-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3de1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3de1-128">**Interface IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="e3de1-128">**IPortableDeviceService Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="e3de1-129">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="e3de1-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="e3de1-130">**Interface IPortableDeviceServiceManager**</span><span class="sxs-lookup"><span data-stu-id="e3de1-130">**IPortableDeviceServiceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)
</dt> <dt>

[<span data-ttu-id="e3de1-131">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="e3de1-131">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



