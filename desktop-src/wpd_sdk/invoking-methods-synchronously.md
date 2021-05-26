---
description: Appel de méthodes de service
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: Appel de méthodes de service
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15b9540cf7378e13d56af2611d6216897c6750f6
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424199"
---
# <a name="invoking-service-methods"></a><span data-ttu-id="98b61-103">Appel de méthodes de service</span><span class="sxs-lookup"><span data-stu-id="98b61-103">Invoking Service Methods</span></span>

<span data-ttu-id="98b61-104">L’application WpdServicesApiSample comprend du code qui montre comment une application peut appeler de façon synchrone les méthodes prises en charge par un service de contacts donné.</span><span class="sxs-lookup"><span data-stu-id="98b61-104">The WpdServicesApiSample application includes code that demonstrates how an application can invoke the methods supported by a given Contacts service synchronously..</span></span> <span data-ttu-id="98b61-105">Cet exemple utilise les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="98b61-105">This sample uses the following interfaces</span></span>



| <span data-ttu-id="98b61-106">Interface</span><span class="sxs-lookup"><span data-stu-id="98b61-106">Interface</span></span>    | <span data-ttu-id="98b61-107">Description</span><span class="sxs-lookup"><span data-stu-id="98b61-107">Description</span></span>    |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98b61-108">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="98b61-108">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | <span data-ttu-id="98b61-109">Utilisé pour récupérer l’interface **IPortableDeviceServiceMethods** pour appeler des méthodes sur un service donné.</span><span class="sxs-lookup"><span data-stu-id="98b61-109">Used to retrieve the **IPortableDeviceServiceMethods** interface to invoke methods on a given service.</span></span>                                                                  |
| [<span data-ttu-id="98b61-110">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="98b61-110">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | <span data-ttu-id="98b61-111">Utilisé pour appeler une méthode de service.</span><span class="sxs-lookup"><span data-stu-id="98b61-111">Used to invoke a service method.</span></span>                                                                                                                                        |
| [<span data-ttu-id="98b61-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="98b61-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                 | <span data-ttu-id="98b61-113">Utilisé pour contenir les paramètres de méthode sortants et les résultats de méthode entrante.</span><span class="sxs-lookup"><span data-stu-id="98b61-113">Used to hold the outgoing method parameters, and the incoming method results.</span></span> <span data-ttu-id="98b61-114">La valeur peut être **null** si la méthode ne requiert pas de paramètres ou ne retourne aucun résultat.</span><span class="sxs-lookup"><span data-stu-id="98b61-114">This can be **NULL** if the method does not require any parameters or return any results.</span></span> |



 

<span data-ttu-id="98b61-115">Quand l’utilisateur choisit l’option « 9 » sur la ligne de commande, l’application appelle la méthode **InvokeMethods** qui se trouve dans le module ServiceMethods. cpp.</span><span class="sxs-lookup"><span data-stu-id="98b61-115">When the user chooses option "9" at the command line, the application invokes the **InvokeMethods** method that is found in the ServiceMethods.cpp module.</span></span> <span data-ttu-id="98b61-116">Notez qu’avant d’appeler les méthodes, l’exemple d’application ouvre un service de contacts sur un appareil connecté.</span><span class="sxs-lookup"><span data-stu-id="98b61-116">Note that prior to invoking the methods, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="98b61-117">Les méthodes de service encapsulent les fonctionnalités que chaque service définit et implémente.</span><span class="sxs-lookup"><span data-stu-id="98b61-117">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="98b61-118">Elles sont uniques à chaque type de service et sont représentées par un GUID.</span><span class="sxs-lookup"><span data-stu-id="98b61-118">They are unique to each type of service and are represented by a GUID.</span></span> <span data-ttu-id="98b61-119">Par exemple, le service contacts définit une méthode **BeginSync** que les applications appellent pour préparer l’appareil à la synchronisation des objets contact, et une méthode **EndSync** pour informer l’appareil que la synchronisation est terminée.</span><span class="sxs-lookup"><span data-stu-id="98b61-119">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span> <span data-ttu-id="98b61-120">Les applications exécutent une méthode en appelant [**IPortableDeviceServiceMethods :: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span><span class="sxs-lookup"><span data-stu-id="98b61-120">Applications execute a method by calling [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span></span>

<span data-ttu-id="98b61-121">Les méthodes de service ne doivent pas être confondues avec les commandes WPD.</span><span class="sxs-lookup"><span data-stu-id="98b61-121">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="98b61-122">Les commandes WPD font partie de l’interface de pilote de périphérique WPD standard (DDI) et constituent le mécanisme de communication entre une application WPD et le pilote.</span><span class="sxs-lookup"><span data-stu-id="98b61-122">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="98b61-123">Les commandes sont prédéfinies, regroupées par catégories, par exemple, la **\_ catégorie wpd \_ commun** et sont représentées par une structure **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="98b61-123">Commands are predefined, grouped by categories, for example, **WPD\_CATEGORY\_COMMON**, and are represented by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="98b61-124">Une application envoie des commandes au pilote de périphérique en appelant [**IPortableDeviceService :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="98b61-124">An application sends commands to the device driver by calling [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span> <span data-ttu-id="98b61-125">Pour plus d’informations, consultez la rubrique commandes.</span><span class="sxs-lookup"><span data-stu-id="98b61-125">For more information, see the Commands topic.</span></span>

<span data-ttu-id="98b61-126">La méthode **InvokeMethods** appelle la méthode [**IPortableDeviceService :: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) pour récupérer une interface [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="98b61-126">The **InvokeMethods** method invokes the [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) method to retrieve an [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="98b61-127">À l’aide de cette interface, il appelle les méthodes **BeginSync** et **EndSync** en appelant la méthode [**IPortableDeviceServiceMethods :: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) .</span><span class="sxs-lookup"><span data-stu-id="98b61-127">Using this interface, it invokes the **BeginSync** and **EndSync** methods by calling the [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) method.</span></span> <span data-ttu-id="98b61-128">À chaque fois qu’il appelle **Invoke**, l’application fournit le REFGUID pour la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="98b61-128">Each time it calls **Invoke**, the application supplies the REFGUID for the method that is invoked.</span></span>

<span data-ttu-id="98b61-129">Le code suivant utilise la méthode **InvokeMethods** .</span><span class="sxs-lookup"><span data-stu-id="98b61-129">The following code uses the **InvokeMethods** method.</span></span>


```C++
// Invoke methods on the Contacts Service.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethods(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke() the BeginSync method
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_BeginSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_EndSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        } 
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="98b61-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="98b61-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98b61-131">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="98b61-131">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="98b61-132">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="98b61-132">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[<span data-ttu-id="98b61-133">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="98b61-133">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



