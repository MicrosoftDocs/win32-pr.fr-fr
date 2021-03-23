---
title: Compteurs UAV
description: Vous pouvez utiliser des compteurs non ordonnés-Access-View (UAV) pour associer un compteur Atomic 32 bits à un mode d’accès non ordonné (UAV).
ms.assetid: 0B77E238-E8CF-466B-9188-3DE96AF97F42
ms.localizationpriority: high
ms.topic: article
ms.date: 02/10/2020
ms.openlocfilehash: 94bc1492e3b984d96c76788430d2e63c0672ca76
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104548529"
---
# <a name="uav-counters"></a><span data-ttu-id="c0715-103">Compteurs UAV</span><span class="sxs-lookup"><span data-stu-id="c0715-103">UAV Counters</span></span>
<span data-ttu-id="c0715-104">Vous pouvez utiliser des compteurs non ordonnés-Access-View (UAV) pour associer un compteur Atomic 32 bits à un mode d’accès non ordonné (UAV).</span><span class="sxs-lookup"><span data-stu-id="c0715-104">You can use unordered-access-view (UAV) counters to associate a 32-bit atomic counter with an unordered-access-view (UAV).</span></span>

## <a name="differences-in-uav-counters-from-direct3d-11-to-direct3d-12"></a><span data-ttu-id="c0715-105">Différences entre les compteurs UAV de Direct3D 11 et Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c0715-105">Differences in UAV counters from Direct3D 11 to Direct3D 12</span></span>
<span data-ttu-id="c0715-106">Les applications Direct3D 12 et Direct3D 11 utilisent toutes les deux les mêmes fonctions de nuanceur HLSL (High-Level Shader Language) pour accéder aux compteurs UAV.</span><span class="sxs-lookup"><span data-stu-id="c0715-106">Direct3D 12 apps and Direct3D 11 apps both use the same high-level shader language (HLSL) shader functions to access the UAV counters.</span></span>

-   <span data-ttu-id="c0715-107">**IncrementCounter**</span><span class="sxs-lookup"><span data-stu-id="c0715-107">**IncrementCounter**</span></span>
-   <span data-ttu-id="c0715-108">**DecrementCounter**</span><span class="sxs-lookup"><span data-stu-id="c0715-108">**DecrementCounter**</span></span>
-   <span data-ttu-id="c0715-109">**Append**</span><span class="sxs-lookup"><span data-stu-id="c0715-109">**Append**</span></span>
-   <span data-ttu-id="c0715-110">**Utiliser**</span><span class="sxs-lookup"><span data-stu-id="c0715-110">**Consume**</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="c0715-111">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c0715-111">Direct3D 12</span></span>
<span data-ttu-id="c0715-112">Dans Direct3D 12, les valeurs 32 bits sont allouées par l’application. par conséquent, les valeurs 32 bits peuvent être lues et écrites par le processeur ou le GPU, comme n’importe quelle autre ressource Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="c0715-112">In Direct3D 12, the 32-bit values are allocated by the application, so the 32-bit values can be read and written by either the CPU or the GPU, just like any other Direct3D 12 resource.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="c0715-113">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="c0715-113">Direct3D 11</span></span>
<span data-ttu-id="c0715-114">En dehors des nuanceurs, avec Direct3D 11, vous devez appeler les méthodes d’API pour accéder aux compteurs (par exemple, [ID3D11DeviceContext :: CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).</span><span class="sxs-lookup"><span data-stu-id="c0715-114">Outside of the shaders, with Direct3D 11 you need to call API methods in order to access the counters (for example, [ID3D11DeviceContext::CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).</span></span>

## <a name="using-uav-counters"></a><span data-ttu-id="c0715-115">Utilisation des compteurs UAV</span><span class="sxs-lookup"><span data-stu-id="c0715-115">Using UAV counters</span></span>
<span data-ttu-id="c0715-116">Votre application est chargée d’allouer 32 bits de stockage pour les compteurs UAV.</span><span class="sxs-lookup"><span data-stu-id="c0715-116">Your app is responsible for allocating 32-bits of storage for UAV counters.</span></span> <span data-ttu-id="c0715-117">Ce stockage peut être alloué dans une ressource différente de celle qui contient les données accessibles via le UAV.</span><span class="sxs-lookup"><span data-stu-id="c0715-117">This storage can be allocated in a different resource as the one that contains data accessible via the UAV.</span></span>

<span data-ttu-id="c0715-118">Reportez-vous à [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12 \_ buffer \_ UAV \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) et [**D3D12 \_ buffer \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).</span><span class="sxs-lookup"><span data-stu-id="c0715-118">Refer to [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12\_BUFFER\_UAV\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) and [**D3D12\_BUFFER\_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).</span></span>

<span data-ttu-id="c0715-119">Si *pCounterResource* est spécifié dans l’appel à [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), alors un compteur est associé au UAV.</span><span class="sxs-lookup"><span data-stu-id="c0715-119">If *pCounterResource* is specified in the call to [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), then there is a counter associated with the UAV.</span></span> <span data-ttu-id="c0715-120">Dans ce cas :</span><span class="sxs-lookup"><span data-stu-id="c0715-120">In this case:</span></span>

-   <span data-ttu-id="c0715-121">*StructureByteStride* doit être supérieur à zéro</span><span class="sxs-lookup"><span data-stu-id="c0715-121">*StructureByteStride* must be greater than zero</span></span>
-   <span data-ttu-id="c0715-122">Le format du format doit être DXGI \_ \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="c0715-122">Format must be DXGI\_FORMAT\_UNKNOWN</span></span>
-   <span data-ttu-id="c0715-123">L’indicateur brut ne doit pas être défini</span><span class="sxs-lookup"><span data-stu-id="c0715-123">The RAW flag must not be set</span></span>
-   <span data-ttu-id="c0715-124">Les deux ressources doivent être des mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="c0715-124">Both of the resources must be buffers</span></span>
-   <span data-ttu-id="c0715-125">*CounterOffsetInBytes* doit être un multiple de 4 octets</span><span class="sxs-lookup"><span data-stu-id="c0715-125">*CounterOffsetInBytes* must be a multiple of 4 bytes</span></span>
-   <span data-ttu-id="c0715-126">*CounterOffsetInBytes* doit se trouver dans la plage de la ressource de compteur</span><span class="sxs-lookup"><span data-stu-id="c0715-126">*CounterOffsetInBytes* must be within the range of the counter resource</span></span>
-   <span data-ttu-id="c0715-127">*pDesc* ne peut pas être null</span><span class="sxs-lookup"><span data-stu-id="c0715-127">*pDesc* cannot be NULL</span></span>
-   <span data-ttu-id="c0715-128">la *présource* ne peut pas être null</span><span class="sxs-lookup"><span data-stu-id="c0715-128">*pResource* cannot be NULL</span></span>

<span data-ttu-id="c0715-129">Et notez les cas d’utilisation suivants :</span><span class="sxs-lookup"><span data-stu-id="c0715-129">And note the following use cases:</span></span>

-   <span data-ttu-id="c0715-130">Si *pCounterResource* n’est pas spécifié, *CounterOffsetInBytes* doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="c0715-130">If *pCounterResource* is not specified, then *CounterOffsetInBytes* must be 0.</span></span>
-   <span data-ttu-id="c0715-131">Si l’indicateur brut est défini, le format doit être DXGI \_ format \_ R32 sans \_ type et la ressource UAV doit être une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c0715-131">If the RAW flag is set then the format must be DXGI\_FORMAT\_R32\_TYPELESS and the UAV resource must be a buffer.</span></span>
-   <span data-ttu-id="c0715-132">Si *pCounterResource* n’est pas défini, *CounterOffsetInBytes* doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="c0715-132">If *pCounterResource* is not set, then *CounterOffsetInBytes* must be 0.</span></span>
-   <span data-ttu-id="c0715-133">Si l’indicateur brut n’est pas défini et que *StructureByteStride* = 0, le format doit être un format UAV valide.</span><span class="sxs-lookup"><span data-stu-id="c0715-133">If the RAW flag is not set and *StructureByteStride* = 0, then the format must be a valid UAV format.</span></span>

<span data-ttu-id="c0715-134">Direct3D 12 supprime la distinction entre les UAVs d’ajout et de compteur (bien que la distinction existe toujours dans le bytecode HLSL).</span><span class="sxs-lookup"><span data-stu-id="c0715-134">Direct3D 12 removes the distinction between append and counter UAVs (although the distinction still exists in HLSL bytecode).</span></span>

<span data-ttu-id="c0715-135">Le runtime principal valide ces restrictions dans [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).</span><span class="sxs-lookup"><span data-stu-id="c0715-135">The core runtime will validate these restrictions inside of [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).</span></span>

<span data-ttu-id="c0715-136">Lors du traçage/Dispatch, la ressource de compteur doit être dans l’état [**D3D12 \_ accès non \_ \_ ordonné \_ à l’État**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)de la ressource.</span><span class="sxs-lookup"><span data-stu-id="c0715-136">During Draw/Dispatch, the counter resource must be in the state [**D3D12\_RESOURCE\_STATE\_UNORDERED\_ACCESS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).</span></span> <span data-ttu-id="c0715-137">En outre, dans un appel de dessin/distribution unique, il n’est pas valide pour une application d’accéder au même emplacement de mémoire 32 bits via deux compteurs UAV distincts.</span><span class="sxs-lookup"><span data-stu-id="c0715-137">Also, within a single Draw/Dispatch call, it is invalid for an application to access the same 32-bit memory location via two separate UAV counters.</span></span> <span data-ttu-id="c0715-138">La couche de débogage génère des erreurs si l’une ou l’autre est détectée.</span><span class="sxs-lookup"><span data-stu-id="c0715-138">The debug layer will issue errors if either of these is detected.</span></span>

<span data-ttu-id="c0715-139">Il n’existe pas de méthode « SetUnorderedAccessViewCounterValue » ou « CopyStructureCount », car les applications peuvent simplement copier des données vers et à partir de la valeur de compteur directement.</span><span class="sxs-lookup"><span data-stu-id="c0715-139">There are no "SetUnorderedAccessViewCounterValue" or "CopyStructureCount" methods because apps can simply copy data to and from the counter value directly.</span></span>

<span data-ttu-id="c0715-140">L’indexation dynamique de UAVs avec des compteurs est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c0715-140">Dynamic indexing of UAVs with counters is supported.</span></span>

<span data-ttu-id="c0715-141">Si un nuanceur tente d’accéder au compteur d’un UAV qui n’a pas de compteur associé, la couche de débogage émet un avertissement et une erreur de page GPU se produit et entraîne la suppression de l’appareil des applications.</span><span class="sxs-lookup"><span data-stu-id="c0715-141">If a shader attempts to access the counter of a UAV that does not have an associated counter, then the debug layer will issue a warning, and a GPU page fault will occur causing the apps’s device to be removed.</span></span>

<span data-ttu-id="c0715-142">Les compteurs UAV sont pris en charge dans tous les types de tas (par défaut, upload, readback).</span><span class="sxs-lookup"><span data-stu-id="c0715-142">UAV counters are supported in all heap types (default, upload, readback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0715-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c0715-143">Related topics</span></span>

* [<span data-ttu-id="c0715-144">Compteurs et requêtes</span><span class="sxs-lookup"><span data-stu-id="c0715-144">Counters and queries</span></span>](counters-and-queries.md)