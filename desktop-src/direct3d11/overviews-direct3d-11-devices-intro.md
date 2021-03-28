---
title: Présentation d’un appareil dans Direct3D 11
description: Le modèle objet Direct3D 11 sépare les fonctionnalités de création et de rendu des ressources dans un appareil et un ou plusieurs contextes. Cette séparation est conçue pour faciliter le multithread.
ms.assetid: b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b03333c6594f17d85fee28880e46928241e06c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971398"
---
# <a name="introduction-to-a-device-in-direct3d-11"></a><span data-ttu-id="ccabd-103">Présentation d’un appareil dans Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ccabd-103">Introduction to a Device in Direct3D 11</span></span>

<span data-ttu-id="ccabd-104">Le modèle objet Direct3D 11 sépare les fonctionnalités de création et de rendu des ressources dans un appareil et un ou plusieurs contextes. Cette séparation est conçue pour faciliter le multithread.</span><span class="sxs-lookup"><span data-stu-id="ccabd-104">The Direct3D 11 object model separates resource creation and rendering functionality into a device and one or more contexts; this separation is designed to facilitate multithreading.</span></span>

-   [<span data-ttu-id="ccabd-105">Appareil</span><span class="sxs-lookup"><span data-stu-id="ccabd-105">Device</span></span>](#introduction-to-a-device-in-direct3d-11)
-   [<span data-ttu-id="ccabd-106">Contexte de périphérique</span><span class="sxs-lookup"><span data-stu-id="ccabd-106">Device Context</span></span>](#device-context)
    -   [<span data-ttu-id="ccabd-107">Contexte immédiat</span><span class="sxs-lookup"><span data-stu-id="ccabd-107">Immediate Context</span></span>](#immediate-context)
    -   [<span data-ttu-id="ccabd-108">Contexte différé</span><span class="sxs-lookup"><span data-stu-id="ccabd-108">Deferred Context</span></span>](#deferred-context)
-   [<span data-ttu-id="ccabd-109">Considérations relatives aux threads</span><span class="sxs-lookup"><span data-stu-id="ccabd-109">Threading Considerations</span></span>](#threading-considerations)
-   [<span data-ttu-id="ccabd-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ccabd-110">Related topics</span></span>](#related-topics)

## <a name="device"></a><span data-ttu-id="ccabd-111">Appareil</span><span class="sxs-lookup"><span data-stu-id="ccabd-111">Device</span></span>

<span data-ttu-id="ccabd-112">Un appareil est utilisé pour créer des ressources et énumérer les fonctionnalités d’un adaptateur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="ccabd-112">A device is used to create resources and to enumerate the capabilities of a display adapter.</span></span> <span data-ttu-id="ccabd-113">Dans Direct3D 11, un appareil est représenté par une interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .</span><span class="sxs-lookup"><span data-stu-id="ccabd-113">In Direct3D 11, a device is represented with an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface.</span></span>

<span data-ttu-id="ccabd-114">Chaque application doit avoir au moins un périphérique, la plupart des applications ne créent qu’un seul appareil.</span><span class="sxs-lookup"><span data-stu-id="ccabd-114">Each application must have at least one device, most applications only create one device.</span></span> <span data-ttu-id="ccabd-115">Créez un appareil pour l’un des pilotes matériels installés sur votre ordinateur en appelant [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) et spécifiez le type de pilote avec l’indicateur de [**\_ \_ type de pilote D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) .</span><span class="sxs-lookup"><span data-stu-id="ccabd-115">Create a device for one of the hardware drivers installed on your machine by calling [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) and specify the driver type with the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) flag.</span></span> <span data-ttu-id="ccabd-116">Chaque périphérique peut utiliser un ou plusieurs contextes de périphérique, en fonction de la fonctionnalité souhaitée.</span><span class="sxs-lookup"><span data-stu-id="ccabd-116">Each device can use one or more device contexts, depending on the functionality desired.</span></span>

## <a name="device-context"></a><span data-ttu-id="ccabd-117">Contexte de périphérique</span><span class="sxs-lookup"><span data-stu-id="ccabd-117">Device Context</span></span>

<span data-ttu-id="ccabd-118">Un contexte de périphérique contient la circonstance ou le paramètre dans lequel un appareil est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ccabd-118">A device context contains the circumstance or setting in which a device is used.</span></span> <span data-ttu-id="ccabd-119">Plus précisément, un contexte de périphérique est utilisé pour définir l’état du pipeline et générer des commandes de rendu à l’aide des ressources détenues par un appareil.</span><span class="sxs-lookup"><span data-stu-id="ccabd-119">More specifically, a device context is used to set pipeline state and generate rendering commands using the resources owned by a device.</span></span> <span data-ttu-id="ccabd-120">Direct3D 11 implémente deux types de contextes de périphérique, un pour le rendu immédiat et l’autre pour le rendu différé ; les deux contextes sont représentés par une interface [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="ccabd-120">Direct3D 11 implements two types of device contexts, one for immediate rendering and the other for deferred rendering; both contexts are represented with an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface.</span></span>

### <a name="immediate-context"></a><span data-ttu-id="ccabd-121">Contexte immédiat</span><span class="sxs-lookup"><span data-stu-id="ccabd-121">Immediate Context</span></span>

<span data-ttu-id="ccabd-122">Un contexte immédiat est restitué directement au pilote.</span><span class="sxs-lookup"><span data-stu-id="ccabd-122">An immediate context renders directly to the driver.</span></span> <span data-ttu-id="ccabd-123">Chaque appareil a un seul et unique contexte immédiat qui peut récupérer des données du GPU.</span><span class="sxs-lookup"><span data-stu-id="ccabd-123">Each device has one and only one immediate context which can retrieve data from the GPU.</span></span> <span data-ttu-id="ccabd-124">Un contexte immédiat peut être utilisé pour restituer (ou lire) immédiatement une [liste de commandes](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="ccabd-124">An immediate context can be used to immediately render (or play back) a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span>

<span data-ttu-id="ccabd-125">Il existe deux façons d’accéder à un contexte immédiat :</span><span class="sxs-lookup"><span data-stu-id="ccabd-125">There are two ways to get an immediate context:</span></span>

-   <span data-ttu-id="ccabd-126">En appelant [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="ccabd-126">By calling either [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>
-   <span data-ttu-id="ccabd-127">En appelant [**ID3D11Device :: GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).</span><span class="sxs-lookup"><span data-stu-id="ccabd-127">By calling [**ID3D11Device::GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).</span></span>

### <a name="deferred-context"></a><span data-ttu-id="ccabd-128">Contexte différé</span><span class="sxs-lookup"><span data-stu-id="ccabd-128">Deferred Context</span></span>

<span data-ttu-id="ccabd-129">Un contexte différé enregistre les commandes GPU dans une [liste de commandes](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="ccabd-129">A deferred context records GPU commands into a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="ccabd-130">Un contexte différé est principalement utilisé pour le multithreading et n’est pas nécessaire pour une application à thread unique.</span><span class="sxs-lookup"><span data-stu-id="ccabd-130">A deferred context is primarily used for multithreading and is not necessary for a single-threaded application.</span></span> <span data-ttu-id="ccabd-131">Un contexte différé est généralement utilisé par un thread de travail plutôt que par le thread de rendu principal.</span><span class="sxs-lookup"><span data-stu-id="ccabd-131">A deferred context is generally used by a worker thread instead of the main rendering thread.</span></span> <span data-ttu-id="ccabd-132">Lorsque vous créez un contexte différé, il n’hérite d’aucun État du contexte immédiat.</span><span class="sxs-lookup"><span data-stu-id="ccabd-132">When you create a deferred context, it does not inherit any state from the immediate context.</span></span>

<span data-ttu-id="ccabd-133">Pour obtenir un contexte différé, appelez [**ID3D11Device :: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span><span class="sxs-lookup"><span data-stu-id="ccabd-133">To get a deferred context, call [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span></span>

<span data-ttu-id="ccabd-134">Tout contexte (immédiat ou différé) peut être utilisé sur n’importe quel thread à condition que le contexte soit utilisé uniquement dans un thread à la fois.</span><span class="sxs-lookup"><span data-stu-id="ccabd-134">Any context -- immediate or deferred -- can be used on any thread as long as the context is only used in one thread at a time.</span></span>

## <a name="threading-considerations"></a><span data-ttu-id="ccabd-135">Considérations relatives aux threads</span><span class="sxs-lookup"><span data-stu-id="ccabd-135">Threading Considerations</span></span>

<span data-ttu-id="ccabd-136">Ce tableau met en évidence les différences entre le modèle de thread dans Direct3D 11 et les versions antérieures de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ccabd-136">This table highlights the differences in the threading model in Direct3D 11 from prior versions of Direct3D.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ccabd-137">Différences entre Direct3D 11 et les versions antérieures de Direct3D :</span><span class="sxs-lookup"><span data-stu-id="ccabd-137">Differences between Direct3D 11 and previous versions of Direct3D:</span></span><br/> <span data-ttu-id="ccabd-138">Toutes les méthodes de l’interface <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> sont libres de thread, ce qui signifie qu’il est possible d’avoir plusieurs threads qui appellent les fonctions en même temps.</span><span class="sxs-lookup"><span data-stu-id="ccabd-138">All <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> interface methods are free-threaded, which means it is safe to have multiple threads call the functions at the same time.</span></span><br/>
<ul>
<li><span data-ttu-id="ccabd-139">Toutes les interfaces dérivées de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>(<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>, etc.) sont libres de threads.</span><span class="sxs-lookup"><span data-stu-id="ccabd-139">All <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>-derived interfaces (<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>, etc.) are free-threaded.</span></span></li>
<li><span data-ttu-id="ccabd-140">Direct3D 11 fractionne la création et le rendu des ressources en deux interfaces.</span><span class="sxs-lookup"><span data-stu-id="ccabd-140">Direct3D 11 splits resource creating and rendering into two interfaces.</span></span> <span data-ttu-id="ccabd-141">Map, DEMAPPAGE, Begin, end et GetData sont implémentés sur <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> , car <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> définit fortement l’ordre des opérations.</span><span class="sxs-lookup"><span data-stu-id="ccabd-141">Map, Unmap, Begin, End, and GetData are implemented on <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> because <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> strongly defines the order of operations.</span></span> <span data-ttu-id="ccabd-142">Les interfaces <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> et <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> implémentent également des méthodes pour les opérations à thread libre.</span><span class="sxs-lookup"><span data-stu-id="ccabd-142"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> and <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> interfaces also implement methods for free-threaded operations.</span></span></li>
<li><span data-ttu-id="ccabd-143">Les méthodes <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> (à l’exception de celles qui existent sur <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) ne sont pas de thread libre, autrement dit, elles nécessitent un thread unique.</span><span class="sxs-lookup"><span data-stu-id="ccabd-143">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> methods (except for those that exist on <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) are not free-threaded, that is, they require single threading.</span></span> <span data-ttu-id="ccabd-144">Un seul thread peut appeler en toute sécurité l’une de ses méthodes (dessin, copie, mappage, etc.) à la fois.</span><span class="sxs-lookup"><span data-stu-id="ccabd-144">Only one thread may safely be calling any of its methods (Draw, Copy, Map, etc.) at a time.</span></span></li>
<li><span data-ttu-id="ccabd-145">En général, les threads libres réduisent le nombre de primitives de synchronisation utilisées, ainsi que leur durée.</span><span class="sxs-lookup"><span data-stu-id="ccabd-145">In general, free-threading minimizes the number of synchronization primitives used as well as their duration.</span></span> <span data-ttu-id="ccabd-146">Toutefois, une application qui utilise la synchronisation maintenue pendant une longue période peut avoir un impact direct sur la quantité de simultanéité qu’une application peut espérer atteindre.</span><span class="sxs-lookup"><span data-stu-id="ccabd-146">However, an application that uses synchronization held for a long time can directly impact how much concurrency an application can expect to achieve.</span></span></li>
</ul>
<span data-ttu-id="ccabd-147">Les méthodes d’interface ID3D10Device ne sont pas conçues pour être libres de threads.</span><span class="sxs-lookup"><span data-stu-id="ccabd-147">ID3D10Device interface methods are not designed to be free-threaded.</span></span> <span data-ttu-id="ccabd-148">ID3D10Device implémente toutes les fonctionnalités de création et de rendu (comme le fait ID3D9Device dans Direct3D 9).</span><span class="sxs-lookup"><span data-stu-id="ccabd-148">ID3D10Device implements all create and rendering functionality (as does ID3D9Device in Direct3D 9).</span></span> <span data-ttu-id="ccabd-149">Les mappages et les mappages sont implémentés sur les interfaces dérivées de ID3D10Resource, Begin, end et GetData sont implémentées sur les interfaces dérivées de ID3D10Asynchronous.</span><span class="sxs-lookup"><span data-stu-id="ccabd-149">Map and Unmap are implemented on ID3D10Resource-derived interfaces, Begin, End, and GetData are implemented on ID3D10Asynchronous-derived interfaces.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ccabd-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ccabd-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccabd-151">Appareils</span><span class="sxs-lookup"><span data-stu-id="ccabd-151">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





