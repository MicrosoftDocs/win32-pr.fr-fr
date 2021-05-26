---
description: Appel des méthodes de service de façon asynchrone
ms.assetid: d3072e34-65f2-4eeb-bcfa-e2db2d34e680
title: Appel des méthodes de service de façon asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef4f0eb2e75b977b53300bed6eab4c909fa7796
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423849"
---
# <a name="invoking-service-methods-asynchronously"></a><span data-ttu-id="541b3-103">Appel des méthodes de service de façon asynchrone</span><span class="sxs-lookup"><span data-stu-id="541b3-103">Invoking Service Methods Asynchronously</span></span>

<span data-ttu-id="541b3-104">L’application WpdServiceApiSample comprend du code qui montre comment une application peut appeler les méthodes de service de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="541b3-104">The WpdServiceApiSample application includes code that demonstrates how an application can invoke the service methods asynchronously.</span></span> <span data-ttu-id="541b3-105">Cet exemple utilise les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="541b3-105">This sample uses the following interfaces.</span></span>



| <span data-ttu-id="541b3-106">Interface</span><span class="sxs-lookup"><span data-stu-id="541b3-106">Interface</span></span>    | <span data-ttu-id="541b3-107">Description</span><span class="sxs-lookup"><span data-stu-id="541b3-107">Description</span></span>          |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="541b3-108">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="541b3-108">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                                | <span data-ttu-id="541b3-109">Utilisé pour récupérer l’interface **IPortableDeviceServiceMethods** pour appeler des méthodes sur un service donné.</span><span class="sxs-lookup"><span data-stu-id="541b3-109">Used to retrieve the **IPortableDeviceServiceMethods** interface to invoke methods on a given service.</span></span>                                                                  |
| [<span data-ttu-id="541b3-110">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="541b3-110">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                  | <span data-ttu-id="541b3-111">Utilisé pour appeler une méthode de service.</span><span class="sxs-lookup"><span data-stu-id="541b3-111">Used to invoke a service method.</span></span>                                                                                                                                        |
| [<span data-ttu-id="541b3-112">**IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="541b3-112">**IPortableDeviceValues**</span></span>](iportabledevicevalues.md)                                  | <span data-ttu-id="541b3-113">Utilisé pour contenir les paramètres de méthode sortants et les résultats de méthode entrante.</span><span class="sxs-lookup"><span data-stu-id="541b3-113">Used to hold the outgoing method parameters, and the incoming method results.</span></span> <span data-ttu-id="541b3-114">La valeur peut être **null** si la méthode ne requiert pas de paramètres ou ne retourne aucun résultat.</span><span class="sxs-lookup"><span data-stu-id="541b3-114">This can be **NULL** if the method does not require any parameters or return any results.</span></span> |
| [<span data-ttu-id="541b3-115">**IPortableDeviceServiceMethodCallback**</span><span class="sxs-lookup"><span data-stu-id="541b3-115">**IPortableDeviceServiceMethodCallback**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback) | <span data-ttu-id="541b3-116">Implémenté par l’application pour recevoir les résultats de la méthode lorsqu’une méthode est terminée.</span><span class="sxs-lookup"><span data-stu-id="541b3-116">Implemented by the application to receive the method results when a method has completed.</span></span>                                                                               |



 

<span data-ttu-id="541b3-117">Quand l’utilisateur choisit l’option « 10 » sur la ligne de commande, l’application appelle la méthode **InvokeMethodsAsync** qui se trouve dans le module ServiceMethods. cpp.</span><span class="sxs-lookup"><span data-stu-id="541b3-117">When the user chooses option "10" at the command line, the application invokes the **InvokeMethodsAsync** method that is found in the ServiceMethods.cpp module.</span></span> <span data-ttu-id="541b3-118">Notez qu’avant d’appeler les méthodes, l’exemple d’application ouvre un service de contacts sur un appareil connecté.</span><span class="sxs-lookup"><span data-stu-id="541b3-118">Note that prior to invoking the methods, the sample application opens a Contacts service on a connected device.</span></span>

<span data-ttu-id="541b3-119">Les méthodes de service encapsulent les fonctionnalités que chaque service définit et implémente.</span><span class="sxs-lookup"><span data-stu-id="541b3-119">Service methods encapsulate functionality that each service defines and implements.</span></span> <span data-ttu-id="541b3-120">Elles sont uniques à chaque type de service et sont représentées par un GUID.</span><span class="sxs-lookup"><span data-stu-id="541b3-120">They are unique to each type of service and are represented by a GUID.</span></span> <span data-ttu-id="541b3-121">Par exemple, le service contacts définit une méthode **BeginSync** que les applications appellent pour préparer l’appareil à la synchronisation des objets contact, et une méthode **EndSync** pour informer l’appareil que la synchronisation est terminée.</span><span class="sxs-lookup"><span data-stu-id="541b3-121">For example, the Contacts service defines a **BeginSync** method that applications call to prepare the device for synchronizing Contact objects, and an **EndSync** method to notify the device that synchronization has completed.</span></span> <span data-ttu-id="541b3-122">Les applications exécutent une méthode de service d’appareil mobile en appelant [**IPortableDeviceServiceMethods :: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span><span class="sxs-lookup"><span data-stu-id="541b3-122">Applications execute a portable device service method by calling [**IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).</span></span>

<span data-ttu-id="541b3-123">Les méthodes de service ne doivent pas être confondues avec les commandes WPD.</span><span class="sxs-lookup"><span data-stu-id="541b3-123">Service methods should not be confused with WPD commands.</span></span> <span data-ttu-id="541b3-124">Les commandes WPD font partie de l’interface de pilote de périphérique WPD standard (DDI) et constituent le mécanisme de communication entre une application WPD et le pilote.</span><span class="sxs-lookup"><span data-stu-id="541b3-124">WPD commands are part of the standard WPD Device Driver Interface (DDI), and are the mechanism for communication between a WPD application and the driver.</span></span> <span data-ttu-id="541b3-125">Les commandes sont prédéfinies, regroupées par catégories (par exemple, la **\_ catégorie wpd \_ commun**) et sont représentées par une structure **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="541b3-125">Commands are predefined, grouped by categories (for example, **WPD\_CATEGORY\_COMMON**), and are represented by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="541b3-126">Une application envoie des commandes au pilote de périphérique en appelant [**IPortableDeviceService :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="541b3-126">An application sends commands to the device driver by calling [**IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span> <span data-ttu-id="541b3-127">Pour plus d’informations, consultez la rubrique commandes.</span><span class="sxs-lookup"><span data-stu-id="541b3-127">For more information, see the Commands topic.</span></span>

<span data-ttu-id="541b3-128">La méthode **InvokeMethodsAsync** appelle [**IPortableDeviceService :: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) pour récupérer une interface [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .</span><span class="sxs-lookup"><span data-stu-id="541b3-128">The **InvokeMethodsAsync** method invokes [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) to retrieve an [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) interface.</span></span> <span data-ttu-id="541b3-129">À l’aide de cette interface, elle appelle à deux reprises la fonction d’assistance **InvokeMethodAsync** . une fois pour la méthode **BeginSync** et une fois pour la méthode **EndSync** .</span><span class="sxs-lookup"><span data-stu-id="541b3-129">Using this interface, it invokes the **InvokeMethodAsync** helper function twice; once for the **BeginSync** method and once for the **EndSync** method.</span></span> <span data-ttu-id="541b3-130">Dans cet exemple,, **InvokeMethodAsync** attend indéfiniment qu’un événement global soit signalé lorsque [**IPortableDeviceServiceMethodCallback :: OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) est appelé.</span><span class="sxs-lookup"><span data-stu-id="541b3-130">In this example, , **InvokeMethodAsync** waits indefinitely for a global event to be signaled when [**IPortableDeviceServiceMethodCallback::OnComplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) is called.</span></span>

<span data-ttu-id="541b3-131">Le code suivant utilise la méthode **InvokeMethodsAsync** .</span><span class="sxs-lookup"><span data-stu-id="541b3-131">The following code uses the **InvokeMethodsAsync** method.</span></span>


```C++
// Invoke methods on the Contacts Service asynchornously.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethodsAsync(IPortableDeviceService* pService)
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

    // Invoke the BeginSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_BeginSync);

        // This method does not take any parameters, so we pass in NULL
        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_BeginSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_EndSync);

        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_EndSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
    }
}
```



<span data-ttu-id="541b3-132">La fonction d’assistance **InvokeMethodAsync** effectue les opérations suivantes pour chaque méthode qu’elle appelle :</span><span class="sxs-lookup"><span data-stu-id="541b3-132">The **InvokeMethodAsync** helper function does the following for each method that it invokes:</span></span>

-   <span data-ttu-id="541b3-133">Crée un handle d’événement global qu’il surveille pour déterminer la fin de la méthode.</span><span class="sxs-lookup"><span data-stu-id="541b3-133">Creates a global event handle that it monitors to determine method completion.</span></span>
-   <span data-ttu-id="541b3-134">Crée un objet **CMethodCallback** fourni en tant qu’argument pour [**IPortableDeviceServiceMethods : InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).</span><span class="sxs-lookup"><span data-stu-id="541b3-134">Creates a **CMethodCallback** object that is supplied as an argument to [**IPortableDeviceServiceMethods:InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).</span></span>
-   <span data-ttu-id="541b3-135">Appelle la méthode **IPortableDeviceServiceMethods :: InvokeAsync** pour appeler la méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="541b3-135">Calls the **IPortableDeviceServiceMethods::InvokeAsync** method to invoke the given method.</span></span>
-   <span data-ttu-id="541b3-136">Surveille l’achèvement du handle d’événement global.</span><span class="sxs-lookup"><span data-stu-id="541b3-136">Monitors the global event handle for completion.</span></span>
-   <span data-ttu-id="541b3-137">Effectue le nettoyage.</span><span class="sxs-lookup"><span data-stu-id="541b3-137">Performs cleanup.</span></span>

<span data-ttu-id="541b3-138">La classe **CMethodCallback** montre comment une application peut implémenter [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback).</span><span class="sxs-lookup"><span data-stu-id="541b3-138">The **CMethodCallback** class demonstrates how an application can implement [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback).</span></span> <span data-ttu-id="541b3-139">L’implémentation de **OnComplete** dans cette classe signale un événement pour avertir l’application que la méthode de service est terminée.</span><span class="sxs-lookup"><span data-stu-id="541b3-139">The implementation of **OnComplete** in this class signals an event to notify the application that the service method has completed.</span></span> <span data-ttu-id="541b3-140">En plus de la méthode **OnComplete** , cette classe implémente **AddRef**, **QueryInterface** et **Release**, qui sont utilisés pour maintenir le décompte de références de l’objet et les interfaces qu’il implémente.</span><span class="sxs-lookup"><span data-stu-id="541b3-140">In addition to the **OnComplete** method, this class implements **AddRef**, **QueryInterface**, and **Release**, which are used to maintain the object's reference count and the interfaces that it implements.</span></span>


```C++
class CMethodCallback : public IPortableDeviceServiceMethodCallback
{
public:
   CMethodCallback () : m_cRef(1)
   {
   }

   ~CMethodCallback ()
   {
   }

public:
    // IPortableDeviceServiceMethodCallback::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE OnComplete(
        HRESULT                 hrStatus,
        IPortableDeviceValues*  /*pResults*/) // We are ignoring results as our methods will not return any results
    {
        printf("** Method completed, status HRESULT = 0x%lx **\n", hrStatus);

        if (g_hMethodCompleteEvent != NULL)
        {
            SetEvent(g_hMethodCompleteEvent);
        }          
        return S_OK;
    }

    // IUnknown::AddRef
    virtual ULONG STDMETHODCALLTYPE AddRef(void)
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    // IUnknown::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE QueryInterface(
        REFIID  riid,
        LPVOID* ppvObj)
    {
        HRESULT hr = S_OK;
        if (ppvObj == NULL)
        {
            hr = E_INVALIDARG;
            return hr;
        }

        if ((riid == IID_IUnknown) ||
            (riid == IID_IPortableDeviceServiceMethodCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            *ppvObj = NULL;
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    // IUnknown::Release
    virtual ULONG STDMETHODCALLTYPE Release(void)
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

private:
    DWORD   m_cRef;
};
```



## <a name="related-topics"></a><span data-ttu-id="541b3-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="541b3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="541b3-142">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="541b3-142">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="541b3-143">**IPortableDeviceServiceMethodCallback**</span><span class="sxs-lookup"><span data-stu-id="541b3-143">**IPortableDeviceServiceMethodCallback**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)
</dt> <dt>

[<span data-ttu-id="541b3-144">**IPortableDeviceServiceMethods**</span><span class="sxs-lookup"><span data-stu-id="541b3-144">**IPortableDeviceServiceMethods**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[<span data-ttu-id="541b3-145">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="541b3-145">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 
