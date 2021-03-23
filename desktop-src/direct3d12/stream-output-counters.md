---
title: Compteurs de sortie de flux
description: La sortie de flux est la capacité du GPU à écrire des vertex dans une mémoire tampon. Les compteurs de sortie de flux surveillent la progression.
ms.assetid: 7342DA09-25E9-4154-83BA-B03ADBB8B671
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4d2f3a823f5f4b5d2d5f365235d7e3f8817207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103557"
---
# <a name="stream-output-counters"></a><span data-ttu-id="9b1fa-104">Compteurs de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="9b1fa-104">Stream Output Counters</span></span>

<span data-ttu-id="9b1fa-105">La sortie de flux est la capacité du GPU à écrire des vertex dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-105">Stream output is the ability of the GPU to write vertices to a buffer.</span></span> <span data-ttu-id="9b1fa-106">Les compteurs de sortie de flux surveillent la progression.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-106">The stream output counters monitor progress.</span></span>

-   [<span data-ttu-id="9b1fa-107">Différences entre les compteurs de flux de Direct3D 11 et Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9b1fa-107">Differences in Stream Counters from Direct3D 11 to Direct3D 12</span></span>](#differences-in-stream-counters-from-direct3d-11-to-direct3d-12)
-   [<span data-ttu-id="9b1fa-108">BufferFilledSize</span><span class="sxs-lookup"><span data-stu-id="9b1fa-108">BufferFilledSize</span></span>](#bufferfilledsize)
-   [<span data-ttu-id="9b1fa-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b1fa-109">Related topics</span></span>](#related-topics)

## <a name="differences-in-stream-counters-from-direct3d-11-to-direct3d-12"></a><span data-ttu-id="9b1fa-110">Différences entre les compteurs de flux de Direct3D 11 et Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9b1fa-110">Differences in Stream Counters from Direct3D 11 to Direct3D 12</span></span>

<span data-ttu-id="9b1fa-111">Dans le cadre du processus de sortie de flux, le GPU doit connaître l’emplacement actuel dans la mémoire tampon dans laquelle il écrit.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-111">As a part of the stream output process, the GPU has to know the current location in the buffer that it is writing to.</span></span> <span data-ttu-id="9b1fa-112">Dans Direct3D 11, la mémoire pour stocker cet emplacement est allouée par le pilote et le seul moyen pour les applications de manipuler cette valeur est d’utiliser la méthode **SOSetTargets** .</span><span class="sxs-lookup"><span data-stu-id="9b1fa-112">In Direct3D 11, memory to store this location is allocated by the driver and the only way for applications to manipulate this value is via the **SOSetTargets** method.</span></span> <span data-ttu-id="9b1fa-113">Dans Direct3D 12, les applications allouent de la mémoire pour stocker cet emplacement actuel.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-113">In Direct3D 12, apps allocate memory to store this current location.</span></span> <span data-ttu-id="9b1fa-114">Il n’existe aucune manière spéciale de manipuler cette valeur, et les applications sont libres de lire/écrire la valeur avec le processeur ou le GPU.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-114">There are no special ways to manipulate this value, and apps are free to read/write the value with the CPU or GPU.</span></span>

## <a name="bufferfilledsize"></a><span data-ttu-id="9b1fa-115">BufferFilledSize</span><span class="sxs-lookup"><span data-stu-id="9b1fa-115">BufferFilledSize</span></span>

<span data-ttu-id="9b1fa-116">L’application est chargée d’allouer le stockage pour une quantité de 32 bits appelée *BufferFilledSize*.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-116">The application is responsible for allocating storage for a 32-bit quantity called the *BufferFilledSize*.</span></span> <span data-ttu-id="9b1fa-117">Contient le nombre d’octets de données dans la mémoire tampon de sortie de flux.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-117">This contains the number of bytes of data in the stream-output buffer.</span></span> <span data-ttu-id="9b1fa-118">Ce stockage peut être placé dans la même ressource, ou une ressource différente que celle qui contient les données de sortie de flux.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-118">This storage can be placed in the same, or a different, resource as the one that contains the stream-output data.</span></span> <span data-ttu-id="9b1fa-119">Cette valeur est accessible par le GPU dans l’étape de flux de sortie pour déterminer où ajouter les nouvelles données de vertex dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-119">This value is accessed by the GPU in the stream-output stage to determine where to append new vertex data in the buffer.</span></span> <span data-ttu-id="9b1fa-120">En outre, cette valeur est accessible par le GPU pour déterminer le moment où un dépassement s’est produit.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-120">Additionally, this value is accessed by the GPU to determine when overflow has occurred.</span></span>

<span data-ttu-id="9b1fa-121">Reportez-vous à la structure de [**\_ sortie du flux \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).</span><span class="sxs-lookup"><span data-stu-id="9b1fa-121">Refer to the structure [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).</span></span>

<span data-ttu-id="9b1fa-122">La couche de débogage validera les éléments suivants dans [**ID3D12GraphicsCommandList :: SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):</span><span class="sxs-lookup"><span data-stu-id="9b1fa-122">The debug layer will validate the following in [**ID3D12GraphicsCommandList::SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):</span></span>

-   <span data-ttu-id="9b1fa-123">*BufferFilledSize* se trouve dans la plage impliquée par {*OffsetInBytes*, *sizeInBytes*}, si une ressource non null est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-123">*BufferFilledSize* falls in the range implied by {*OffsetInBytes*, *SizeInBytes*}, if a non-NULL resource is specified.</span></span>
-   <span data-ttu-id="9b1fa-124">*BufferFilledSizeOffsetInBytes* est un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-124">*BufferFilledSizeOffsetInBytes* is a multiple of 4.</span></span>
-   <span data-ttu-id="9b1fa-125">*BufferFilledSizeOffsetInBytes* se trouve dans la plage de la ressource conteneur.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-125">*BufferFilledSizeOffsetInBytes* is within the range of the containing resource.</span></span>
-   <span data-ttu-id="9b1fa-126">La ressource spécifiée est une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-126">The specified resource is a buffer.</span></span>

<span data-ttu-id="9b1fa-127">Le runtime ne valide pas le type de tas associé à la mémoire tampon de sortie de flux, car la sortie de flux est prise en charge dans tous les types de tas.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-127">The runtime will not validate the heap type associated with the stream output buffer, as stream output is supported in all heap types.</span></span>

<span data-ttu-id="9b1fa-128">Les signatures racines doivent spécifier si la sortie de flux sera utilisée, à l’aide des indicateurs de [**\_ \_ signature \_ racine D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-128">Root signatures must specify if stream output will be used, by using the [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags.</span></span>

<span data-ttu-id="9b1fa-129">\_ \_ L’indicateur de signature racine D3D12 \_ \_ autorise \_ la sortie de flux \_ peut être spécifiée pour les signatures racines créées en HLSL, d’une manière similaire à la façon dont les autres indicateurs sont spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-129">D3D12\_ROOT\_SIGNATURE\_FLAG\_ALLOW\_STREAM\_OUTPUT can be specified for root signatures authored in HLSL, in a manner similar to how the other flags are specified.</span></span>

<span data-ttu-id="9b1fa-130">[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) échoue si le nuanceur Geometry contient un flux de sortie, mais que la signature racine n’a pas l’indicateur de \_ signature racine D3D12 allow de la sortie de \_ \_ \_ \_ flux \_ défini.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-130">[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) will fail if the geometry shader contains stream-output but the root signature does not have the D3D12\_ROOT\_SIGNATURE\_FLAG\_ALLOW\_STREAM\_OUTPUT flag set.</span></span>

<span data-ttu-id="9b1fa-131">Lorsqu’une ressource est utilisée en tant que cible de sortie de flux, les ressources utilisées doivent être dans \_ l' \_ \_ État de flux \_ sortant de l’état de ressource D3D12.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-131">When a resource is used as a stream-output target, the resources used must be in the D3D12\_RESOURCE\_STATE\_STREAM\_OUT state.</span></span> <span data-ttu-id="9b1fa-132">Cela s’applique à la fois aux données de vertex et au *BufferFilledSize* (qui peuvent être dans les mêmes ressources ou des ressources distinctes).</span><span class="sxs-lookup"><span data-stu-id="9b1fa-132">This applies to both the vertex data and the *BufferFilledSize* (which can be in the same or separate resources).</span></span>

<span data-ttu-id="9b1fa-133">Il n’existe pas d’API spéciales pour définir des décalages de mémoire tampon de sortie de flux, car les applications peuvent écrire directement sur le *BufferFilledSize* avec le processeur ou le GPU.</span><span class="sxs-lookup"><span data-stu-id="9b1fa-133">There are no special APIs to set stream-output buffer offsets because applications can write to the *BufferFilledSize* with the CPU or GPU directly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b1fa-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b1fa-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b1fa-135">Compteurs et requêtes</span><span class="sxs-lookup"><span data-stu-id="9b1fa-135">Counters and Queries</span></span>](counters-and-queries.md)
</dt> </dl>

 

 




