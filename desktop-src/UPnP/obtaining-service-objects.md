---
title: Obtention d’objets de service
description: Les objets appareil exposent une propriété appelée services qui retourne une collection d’objets de service qui contient un objet de service pour chaque service exporté par l’appareil.
ms.assetid: 8ef12b6e-cb9b-4406-95be-002117b8fc3f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf951c9c620c23c2d4919dc4a8bcf082159fa7a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842569"
---
# <a name="obtaining-service-objects"></a><span data-ttu-id="9d18f-103">Obtention d’objets de service</span><span class="sxs-lookup"><span data-stu-id="9d18f-103">Obtaining Service Objects</span></span>

<span data-ttu-id="9d18f-104">Les objets appareil exposent une propriété appelée [**services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) qui retourne une collection d’objets de service qui contient un objet de service pour chaque service exporté par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9d18f-104">Device objects expose a property called [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) that returns a collection of Service objects that contains one service object for each service exported by the device.</span></span> <span data-ttu-id="9d18f-105">Les applications peuvent parcourir cette collection séquentiellement ou demander un service particulier à l’aide de son ID de service.</span><span class="sxs-lookup"><span data-stu-id="9d18f-105">Applications are able to traverse this collection sequentially, or request a particular service by using its service ID.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="9d18f-106">Exemple VBScript</span><span class="sxs-lookup"><span data-stu-id="9d18f-106">VBScript Example</span></span>

<span data-ttu-id="9d18f-107">L’exemple suivant est un code VBScript qui extrait des objets de service pour deux des services exportés par un appareil.</span><span class="sxs-lookup"><span data-stu-id="9d18f-107">The following example is VBScript code that extracts Service objects for two of the services exported by a device.</span></span>


```VB
' Get the service objects
services = device.Services
    
Set appService = services( "urn:upnp-org:serviceId:DVDVideo" )
Set xportService = services( "urn:upnp-org:serviceId:AVTransport" )
```



<span data-ttu-id="9d18f-108">La première ligne extrait la collection services de l’objet Device en interrogeant la propriété [**services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) .</span><span class="sxs-lookup"><span data-stu-id="9d18f-108">The first line extracts the services collection from the Device object by querying the [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) property.</span></span> <span data-ttu-id="9d18f-109">Les deux lignes suivantes obtiennent les deux objets de service souhaités à partir de la collection en spécifiant leurs ID de service.</span><span class="sxs-lookup"><span data-stu-id="9d18f-109">The next two lines obtain the two desired Service objects from the collection by specifying their service IDs.</span></span> <span data-ttu-id="9d18f-110">La collection services peut également être parcourue de manière séquentielle à l’aide d’une boucle **for each... Next** .</span><span class="sxs-lookup"><span data-stu-id="9d18f-110">The services collection can also be traversed sequentially by using a **for each … next** loop.</span></span>

## <a name="c-example"></a><span data-ttu-id="9d18f-111">Exemple C++</span><span class="sxs-lookup"><span data-stu-id="9d18f-111">C++ Example</span></span>

<span data-ttu-id="9d18f-112">L’exemple suivant montre le code C++ requis pour obtenir des objets de service à partir d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="9d18f-112">The following example shows the C++ code required to obtain Service objects from a device.</span></span> <span data-ttu-id="9d18f-113">Tout d’abord, l’exemple de code interroge la propriété [**IUPnPDevice :: services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) sur l’interface qui a été passée à la fonction.</span><span class="sxs-lookup"><span data-stu-id="9d18f-113">First, the sample code queries the [**IUPnPDevice::Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) property on the interface that was passed to the function.</span></span> <span data-ttu-id="9d18f-114">Cela retourne une collection de services à l’aide de l’interface [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) .</span><span class="sxs-lookup"><span data-stu-id="9d18f-114">This returns a service collection using the [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) interface.</span></span> <span data-ttu-id="9d18f-115">Pour obtenir des objets de service individuels, utilisez la méthode [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) et spécifiez les ID de service demandés.</span><span class="sxs-lookup"><span data-stu-id="9d18f-115">To obtain individual Service objects, use the [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) method, and specify the requested service IDs.</span></span> <span data-ttu-id="9d18f-116">Pour parcourir la collection de manière séquentielle, utilisez les méthodes [**IEnumVARIANT :: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT :: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next)et [**IEnumVARIANT :: Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) .</span><span class="sxs-lookup"><span data-stu-id="9d18f-116">To traverse the collection sequentially, use the [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next), and [**IEnumVARIANT::Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) methods.</span></span> <span data-ttu-id="9d18f-117">Cet exemple est similaire à l’exemple utilisé pour parcourir la collection [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .</span><span class="sxs-lookup"><span data-stu-id="9d18f-117">This example is similar to the example used to traverse the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) collection.</span></span>


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")


HRESULT ExtractServices(IUPnPDevice * pDevice)
{
    // Create a BSTR to hold the service name
    BSTR bstrServiceName = SysAllocString(L"urn:upnp-org:servicId:DVDVideo");
    if (NULL == bstrServiceName)
    {
        return E_OUTOFMEMORY;
    }
    // Get the list of services available on the device
    IUPnPServices * pServices = NULL;
    HRESULT hr = pDevice->get_Services(&pServices);
    if (SUCCEEDED(hr))
    {
        // Retrieve the service we are interested in
        IUPnPService * pAppService = NULL;
        hr = pServices->get_Item(bstrServiceName, &pAppService);
        if (SUCCEEDED(hr))
        {
            // Do something interesting with the service object
            pAppService->Release();
        }
        pServices->Release();
    }
    SysFreeString(bstrServiceName);
    return hr;
}
```



 

 