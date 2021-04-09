---
title: Regroupements de périphériques retournés par les recherches synchrones
description: Les regroupements d’appareils sont des objets qui contiennent un ou plusieurs objets appareil. Une collection de périphériques expose l’interface IUPnPDevices qui fournit des méthodes et des propriétés pour parcourir la collection et extraire des objets périphériques individuels.
ms.assetid: 45455c3f-7281-4f96-a609-2efd2cf36aa2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd581b7c79fe67a825e411d53e8c44c0f3d4326
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102052"
---
# <a name="device-collections-returned-by-synchronous-searches"></a><span data-ttu-id="e74e3-104">Regroupements de périphériques retournés par les recherches synchrones</span><span class="sxs-lookup"><span data-stu-id="e74e3-104">Device Collections Returned By Synchronous Searches</span></span>

<span data-ttu-id="e74e3-105">Les regroupements d’appareils sont des objets qui contiennent un ou plusieurs objets appareil.</span><span class="sxs-lookup"><span data-stu-id="e74e3-105">Device collections are objects that contain one or more Device objects.</span></span> <span data-ttu-id="e74e3-106">Une collection de périphériques expose l’interface [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) qui fournit des méthodes et des propriétés pour parcourir la collection et extraire des objets périphériques individuels.</span><span class="sxs-lookup"><span data-stu-id="e74e3-106">A Device collection exposes the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface that provides methods and properties for traversing the collection and extracting individual device objects.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="e74e3-107">Exemple VBScript</span><span class="sxs-lookup"><span data-stu-id="e74e3-107">VBScript Example</span></span>

<span data-ttu-id="e74e3-108">Les applications VBScript peuvent accéder aux objets de la collection de deux façons.</span><span class="sxs-lookup"><span data-stu-id="e74e3-108">VBScript applications can access the objects in the collection in two ways.</span></span> <span data-ttu-id="e74e3-109">Tout d’abord, ils peuvent traverser les éléments de manière séquentielle à l’aide d’une boucle for...</span><span class="sxs-lookup"><span data-stu-id="e74e3-109">First, they can traverse the elements sequentially using a for …</span></span> <span data-ttu-id="e74e3-110">chaque... Next, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="e74e3-110">each ... next loop as shown in the following example:</span></span>


```VB
for each deviceObj in devices
    MsgBox(deviceObj.FriendlyName)
next
```



<span data-ttu-id="e74e3-111">Dans cet exemple, la variable Devices est supposée avoir été initialisée avec le résultat d’une recherche antérieure.</span><span class="sxs-lookup"><span data-stu-id="e74e3-111">In this example, the devices variable is assumed to have been initialized with the result of a prior search.</span></span> <span data-ttu-id="e74e3-112">La boucle parcourt les objets d’appareil de la collection, en affectant la variable deviceObj la valeur de chaque objet d’appareil.</span><span class="sxs-lookup"><span data-stu-id="e74e3-112">The loop steps through the Device objects in the collection, assigning the variable deviceObj the value of each Device object in turn.</span></span> <span data-ttu-id="e74e3-113">Le corps de la boucle peut contenir du code qui traite l’objet appareil.</span><span class="sxs-lookup"><span data-stu-id="e74e3-113">The body of the loop can contain code that processes the Device object.</span></span>

## <a name="c-example"></a><span data-ttu-id="e74e3-114">Exemple C++</span><span class="sxs-lookup"><span data-stu-id="e74e3-114">C++ Example</span></span>

<span data-ttu-id="e74e3-115">L’exemple suivant montre le code C++ requis pour accéder aux objets dans une collection d’objets appareil.</span><span class="sxs-lookup"><span data-stu-id="e74e3-115">The following example shows the C++ code required to access the objects in a collection of device objects.</span></span> <span data-ttu-id="e74e3-116">La fonction illustrée, **TraverseCollection**, reçoit un pointeur vers l’interface [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) en tant que paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e74e3-116">The function shown, **TraverseCollection**, receives a pointer to the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface as an input parameter.</span></span> <span data-ttu-id="e74e3-117">Ce pointeur d’interface peut être retourné par la méthode [**FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) , ou d’autres méthodes **Find** , de l’objet de recherche d’appareil.</span><span class="sxs-lookup"><span data-stu-id="e74e3-117">This interface pointer could be returned by the [**FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method, or other **Find** methods, of the Device Finder object.</span></span>


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")

HRESULT TraverseCollection(IUPnPDevices * pDevices)
{
    IUnknown * pUnk = NULL;
    HRESULT hr = pDevices->get__NewEnum(&pUnk);
    if (SUCCEEDED(hr))
    {
        IEnumVARIANT * pEnumVar = NULL;
        hr = pUnk->QueryInterface(IID_IEnumVARIANT, (void **) &pEnumVar);
        if (SUCCEEDED(hr))
        {
            VARIANT varCurDevice;
            VariantInit(&varCurDevice);
            pEnumVar->Reset();
            // Loop through each device in the collection
            while (S_OK == pEnumVar->Next(1, &varCurDevice, NULL))
            {
                IUPnPDevice * pDevice = NULL;
                IDispatch * pdispDevice = V_DISPATCH(&varCurDevice);
                if (SUCCEEDED(pdispDevice->QueryInterface(IID_IUPnPDevice, (void **) &pDevice)))
                {
                    // Do something interesting with pDevice
                    BSTR bstrName = NULL;
                    if (SUCCEEDED(pDevice->get_FriendlyName(&bstrName)))
                    {
                        OutputDebugStringW(bstrName);
                        SysFreeString(bstrName);
                    }
                }
                VariantClear(&varCurDevice);
                pDevice->Release();
            }
            pEnumVar->Release();
        }
        pUnk->Release();
    }
    return hr;
}
```



<span data-ttu-id="e74e3-118">La première étape consiste à demander un nouvel énumérateur pour la collection à l’aide de la propriété [**\_ NewEnum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) .</span><span class="sxs-lookup"><span data-stu-id="e74e3-118">The first step is to request a new enumerator for the collection using the [**\_NewEnum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) property.</span></span> <span data-ttu-id="e74e3-119">Cela retourne un énumérateur comme interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e74e3-119">This returns an enumerator as the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e74e3-120">L’exemple de code appelle [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir l’interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="e74e3-120">The sample code invokes [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain the [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface.</span></span> <span data-ttu-id="e74e3-121">L’exemple de code définit ensuite l’énumérateur au début de la collection en appelant la méthode [**IEnumVARIANT :: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) .</span><span class="sxs-lookup"><span data-stu-id="e74e3-121">The sample code then sets the enumerator to the beginning of the collection by invoking the [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) method.</span></span> <span data-ttu-id="e74e3-122">Enfin, l’exemple de code appelle la méthode [**IEnumVARIANT :: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) pour parcourir la collection.</span><span class="sxs-lookup"><span data-stu-id="e74e3-122">Finally, the sample code invokes the [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) method to traverse the collection.</span></span> <span data-ttu-id="e74e3-123">Les objets d’appareil de la collection sont contenus dans des structures de **variantes** .</span><span class="sxs-lookup"><span data-stu-id="e74e3-123">The device objects in the collection are contained within **VARIANT** structures.</span></span> <span data-ttu-id="e74e3-124">Ces structures contiennent des pointeurs vers des interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) sur les objets d’appareil.</span><span class="sxs-lookup"><span data-stu-id="e74e3-124">These structures contain pointers to [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces on the device objects.</span></span> <span data-ttu-id="e74e3-125">Pour obtenir l’interface [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) , l’exemple de code appelle **QueryInterface** sur l’interface **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="e74e3-125">To obtain the [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) interface, the sample code invokes **QueryInterface** on the **IDispatch** interface.</span></span>

 

 