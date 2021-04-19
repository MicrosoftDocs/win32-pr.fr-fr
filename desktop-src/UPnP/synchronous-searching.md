---
title: Recherche synchrone
description: L’objet de recherche d’appareils active les recherches synchrones et asynchrones. Les recherches synchrones sont terminées et retournent le contrôle à l’application appelante uniquement après la détection de tous les appareils disponibles.
ms.assetid: fa22cd53-6468-4958-b4e3-b1a41b3cb2f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1890829dfe8386cd79627dde039264dc81e473c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106538787"
---
# <a name="synchronous-searching"></a><span data-ttu-id="1c1b3-104">Recherche synchrone</span><span class="sxs-lookup"><span data-stu-id="1c1b3-104">Synchronous Searching</span></span>

<span data-ttu-id="1c1b3-105">L’objet de recherche d’appareils active les recherches synchrones et asynchrones.</span><span class="sxs-lookup"><span data-stu-id="1c1b3-105">The Device Finder object enables both synchronous and asynchronous searches.</span></span> <span data-ttu-id="1c1b3-106">Les recherches synchrones sont terminées et retournent le contrôle à l’application appelante uniquement après la détection de tous les appareils disponibles.</span><span class="sxs-lookup"><span data-stu-id="1c1b3-106">Synchronous searches are completed and return control to the calling application only after all available devices are found.</span></span> <span data-ttu-id="1c1b3-107">Pour effectuer une recherche synchrone, utilisez l’une des méthodes de recherche synchrone de l’interface [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) .</span><span class="sxs-lookup"><span data-stu-id="1c1b3-107">To perform a synchronous search, use one of the synchronous search methods of the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface.</span></span>

> [!Note]  
> <span data-ttu-id="1c1b3-108">Les recherches synchrones prennent au moins neuf secondes pour être retournées.</span><span class="sxs-lookup"><span data-stu-id="1c1b3-108">Synchronous searches take at least nine seconds to return.</span></span> <span data-ttu-id="1c1b3-109">Le délai est dû au fait que le message de recherche UDP initial doit être envoyé plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="1c1b3-109">The delay is caused because the initial UDP search message must be sent multiple times.</span></span> <span data-ttu-id="1c1b3-110">Cette duplication tient compte de l’infiabilité du protocole réseau sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="1c1b3-110">This duplication accounts for the unreliability of the underlying network protocol.</span></span> <span data-ttu-id="1c1b3-111">Les recherches synchrones sont idéales pour les interfaces de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="1c1b3-111">Synchronous searches are best for command-line interfaces.</span></span> <span data-ttu-id="1c1b3-112">Elles ne sont pas recommandées pour les interfaces utilisateur graphiques.</span><span class="sxs-lookup"><span data-stu-id="1c1b3-112">They are not recommended for graphical user interfaces.</span></span>

 

<span data-ttu-id="1c1b3-113">La méthode [**IUPnPDeviceFinder :: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) effectue une recherche par type d’appareil ou de service.</span><span class="sxs-lookup"><span data-stu-id="1c1b3-113">The [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method searches by device or service type.</span></span> <span data-ttu-id="1c1b3-114">Cette méthode prend un URI de type comme paramètre d’entrée et retourne une collection d’objets périphériques.</span><span class="sxs-lookup"><span data-stu-id="1c1b3-114">This method takes a type URI as an input parameter and returns a collection of Device objects.</span></span> <span data-ttu-id="1c1b3-115">Un objet appareil représente un appareil individuel.</span><span class="sxs-lookup"><span data-stu-id="1c1b3-115">A Device object represents an individual device.</span></span>

<span data-ttu-id="1c1b3-116">Les exemples suivants montrent comment effectuer une recherche synchrone des appareils dans VBScript.</span><span class="sxs-lookup"><span data-stu-id="1c1b3-116">The following examples demonstrate how to perform a synchronous search for devices in VBScript.</span></span> <span data-ttu-id="1c1b3-117">Chaque script utilise [**IUPnPDeviceFinder :: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), appelé avec l’URI de type (ID de service) pour le type d’appareil Media Player, *urn : schemas-UPnP-org : Device : MediaPlayer. v 1.00.00*.</span><span class="sxs-lookup"><span data-stu-id="1c1b3-117">Each script uses [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), called with the type URI (service ID) for the media player device type, *urn:schemas-upnp-org:device:mediaplayer.v1.00.00*.</span></span> <span data-ttu-id="1c1b3-118">La méthode retourne une collection d’objets Device qui correspond aux périphériques Media Player qui ont été trouvés.</span><span class="sxs-lookup"><span data-stu-id="1c1b3-118">The method returns a collection of Device objects that corresponds to media player devices that were found.</span></span> <span data-ttu-id="1c1b3-119">Pour plus d’informations sur l’extraction d’objets d’appareil individuels à partir d’une collection, consultez [regroupements de périphériques retournés par les recherches synchrones](device-collections-returned-by-synchronous-searches.md).</span><span class="sxs-lookup"><span data-stu-id="1c1b3-119">For information on extracting individual device objects from a collection, see [Device Collections Returned By Synchronous Searches](device-collections-returned-by-synchronous-searches.md).</span></span>

## <a name="search-for-devices-by-type-in-vbscript"></a><span data-ttu-id="1c1b3-120">Rechercher des appareils par type dans VBScript</span><span class="sxs-lookup"><span data-stu-id="1c1b3-120">Search for Devices by Type in VBScript</span></span>


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a><span data-ttu-id="1c1b3-121">Rechercher des appareils par type en C++</span><span class="sxs-lookup"><span data-stu-id="1c1b3-121">Search for Device by Type in C++</span></span>

<span data-ttu-id="1c1b3-122">L’exemple suivant illustre une recherche synchrone de périphériques Media Player à l’aide de C++.</span><span class="sxs-lookup"><span data-stu-id="1c1b3-122">The following example demonstrates a synchronous search for media player devices using C++.</span></span> <span data-ttu-id="1c1b3-123">La fonction prend un pointeur vers l’interface [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) comme entrée et retourne le pointeur d’interface [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .</span><span class="sxs-lookup"><span data-stu-id="1c1b3-123">The function takes a pointer to the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface as input, and returns the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface pointer.</span></span>

<span data-ttu-id="1c1b3-124">L’exemple alloue d’abord un **BSTR** pour représenter l’URI du type d’appareil, puis le transmet à la méthode [**IUPnPDeviceFinder :: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) .</span><span class="sxs-lookup"><span data-stu-id="1c1b3-124">The example first allocates a **BSTR** to represent the device type URI and then passes this to the [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method.</span></span> <span data-ttu-id="1c1b3-125">Il transmet également l’adresse d’un pointeur [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) local dans la mémoire tampon dans laquelle la méthode stocke ensuite la collection d’appareils trouvés.</span><span class="sxs-lookup"><span data-stu-id="1c1b3-125">It also passes the address of a local [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) pointer in the buffer in which the method then stores the collection of devices found.</span></span> <span data-ttu-id="1c1b3-126">Si l’appel de fonction réussit, il retourne le pointeur vers cette collection.</span><span class="sxs-lookup"><span data-stu-id="1c1b3-126">If the function call is successful, it returns the pointer to this collection.</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "oleaut32.lib")

IUPnPDevices *FindMediaPlayerDevices(IUPnPDeviceFinder *pDeviceFinder)
{
    HRESULT         hr = S_OK;
    IUPnPDevices    * pFoundDevices = NULL;
    BSTR            bstrTypeURI = NULL;

    bstrTypeURI = 
        SysAllocString(L"urn:schemas-upnp-org:device:multidisk-dvd");

    if (bstrTypeURI)
    {
        hr = pDeviceFinder->FindByType(bstrTypeURI, 
                                       0,
                                       &pFoundDevices);

        if (SUCCEEDED(hr))
        {
            wprintf(L"FindMediaPlayerDevices(): "
                    L"Search returned successfully\n");
        }
        else
        {
            fwprintf(stderr, L"FindMediaPlayerDevices(): "
                     L"FindByType search failed - returned "
                     L"HRESULT 0x%x\n",
                     hr);
            pFoundDevices = NULL;
        }
        SysFreeString(bstrTypeURI);
    }
    else
    {
        fwprintf(stderr, L"FindMediaPlayerDevices(): "
                 L"Could not allocate BSTR for type URI\n");
    }

    return pFoundDevices;
}
```



 

 




