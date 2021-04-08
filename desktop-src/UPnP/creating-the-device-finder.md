---
title: Création du Finder d’appareils
description: Les exemples suivants montrent comment créer une instance de l’objet Device Finder en C++, Visual Basic et VBScript.
ms.assetid: 0084a64d-458e-471c-a6be-aeb6ed0962d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a12fc7e269f2c0ce5b577fe2f49b6d13fe3b5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840530"
---
# <a name="creating-the-device-finder"></a><span data-ttu-id="0aa80-103">Création du Finder d’appareils</span><span class="sxs-lookup"><span data-stu-id="0aa80-103">Creating the Device Finder</span></span>

<span data-ttu-id="0aa80-104">Les exemples suivants montrent comment créer une instance de l’objet Device Finder en C++, Visual Basic et VBScript.</span><span class="sxs-lookup"><span data-stu-id="0aa80-104">The following examples demonstrate how to create an instance of the Device Finder object in C++, Visual Basic, and VBScript.</span></span> <span data-ttu-id="0aa80-105">Les langages de script utilisent l’ID programmatique (ProgID) [**UPnP. UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) pour identifier la classe Device Finder.</span><span class="sxs-lookup"><span data-stu-id="0aa80-105">The script languages use the programmatic ID (ProgID) [**UPnP.UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) to identify the Device Finder class.</span></span> <span data-ttu-id="0aa80-106">Le code C++ utilise l’identificateur de classe.</span><span class="sxs-lookup"><span data-stu-id="0aa80-106">The C++ code uses the class identifier.</span></span>

## <a name="c-example"></a><span data-ttu-id="0aa80-107">Exemple C++</span><span class="sxs-lookup"><span data-stu-id="0aa80-107">C++ Example</span></span>


```C++
HRESULT hr = S_OK;
IUPnPDeviceFinder *pDeviceFinder = NULL;

hr = CoCreateInstance(CLSID_UPnPDeviceFinder, 
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IUPnPDeviceFinder,
                      (void **) &pDeviceFinder);
```



<span data-ttu-id="0aa80-108">Comme l’indique cet exemple C++, l’objet de recherche d’appareil expose une interface par défaut, [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder).</span><span class="sxs-lookup"><span data-stu-id="0aa80-108">As this C++ example indicates, the Device Finder object exposes a default interface, [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder).</span></span> <span data-ttu-id="0aa80-109">Les méthodes de cette interface effectuent des recherches en fonction des critères de recherche valides pour un périphérique UPnP.</span><span class="sxs-lookup"><span data-stu-id="0aa80-109">The methods of this interface perform searches according to the valid search criteria for a UPnP-based device.</span></span> <span data-ttu-id="0aa80-110">Cette interface étant capable d’automatiser, ses méthodes peuvent être appelées par du code de script.</span><span class="sxs-lookup"><span data-stu-id="0aa80-110">This interface is Automation capable, so its methods can be called by scripting code.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="0aa80-111">Exemple VBScript</span><span class="sxs-lookup"><span data-stu-id="0aa80-111">VBScript Example</span></span>


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )
```



 

 




