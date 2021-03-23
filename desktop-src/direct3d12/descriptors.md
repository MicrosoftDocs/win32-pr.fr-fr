---
title: Descripteurs
description: Les descripteurs sont l’unité principale de liaison pour une seule ressource dans D3D12.
ms.assetid: f35b5776-46b0-4659-9e61-c6ebfdb55f87
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9576a2d40ade89c9c7a342feb6b069ca1321028e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104306"
---
# <a name="descriptors"></a><span data-ttu-id="9e863-103">Descripteurs</span><span class="sxs-lookup"><span data-stu-id="9e863-103">Descriptors</span></span>

<span data-ttu-id="9e863-104">Les descripteurs sont l’unité principale de liaison pour une seule ressource dans D3D12.</span><span class="sxs-lookup"><span data-stu-id="9e863-104">Descriptors are the primary unit of binding for a single resource in D3D12.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9e863-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="9e863-105">In this section</span></span>



| <span data-ttu-id="9e863-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="9e863-106">Topic</span></span>                                                       | <span data-ttu-id="9e863-107">Description</span><span class="sxs-lookup"><span data-stu-id="9e863-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e863-108">Vue d’ensemble des descripteurs</span><span class="sxs-lookup"><span data-stu-id="9e863-108">Descriptors Overview</span></span>](descriptors-overview.md)<br/> | <span data-ttu-id="9e863-109">Les descripteurs sont créés par des appels d’API et identifient les ressources.</span><span class="sxs-lookup"><span data-stu-id="9e863-109">Descriptors are created by API calls and identify resources.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="9e863-110">Création de descripteurs</span><span class="sxs-lookup"><span data-stu-id="9e863-110">Creating Descriptors</span></span>](creating-descriptors.md)<br/> | <span data-ttu-id="9e863-111">Décrit et montre des exemples pour créer des vues de mémoire tampon d’index, de vertex et de constantes ; la ressource de nuanceur, la cible de rendu, l’accès non ordonné, la sortie de flux et les vues de stencil de profondeur ; et les échantillonneurs.</span><span class="sxs-lookup"><span data-stu-id="9e863-111">Describes and shows examples for creating index, vertex, and constant buffer views; shader resource, render target, unordered access, stream output and depth-stencil views; and samplers.</span></span> <span data-ttu-id="9e863-112">Toutes les méthodes de création de descripteurs sont des threads libres.</span><span class="sxs-lookup"><span data-stu-id="9e863-112">All methods for creating descriptors are free threaded.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="9e863-113">Copie de descripteurs</span><span class="sxs-lookup"><span data-stu-id="9e863-113">Copying Descriptors</span></span>](copying-descriptors.md)<br/>   | <span data-ttu-id="9e863-114">Les méthodes [**ID3D12Device :: CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) et [**ID3D12Device :: CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) sur l’interface de l’appareil utilisent le processeur pour copier immédiatement les descripteurs.</span><span class="sxs-lookup"><span data-stu-id="9e863-114">The [**ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) and [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) methods on the device interface use the CPU to immediately copy descriptors.</span></span> <span data-ttu-id="9e863-115">Ils peuvent être appelés thread libre, à condition que plusieurs threads sur le processeur ou le GPU n’effectuent pas d’écriture potentiellement conflictuelle.</span><span class="sxs-lookup"><span data-stu-id="9e863-115">They can be called free threaded as long as multiple threads on the CPU or GPU do not perform any potentially conflicting writes.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="9e863-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9e863-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e863-117">Tas de descripteurs</span><span class="sxs-lookup"><span data-stu-id="9e863-117">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="9e863-118">Tables de descripteurs</span><span class="sxs-lookup"><span data-stu-id="9e863-118">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> <dt>

[<span data-ttu-id="9e863-119">Liaison de ressource</span><span class="sxs-lookup"><span data-stu-id="9e863-119">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="9e863-120">Signatures racines</span><span class="sxs-lookup"><span data-stu-id="9e863-120">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





