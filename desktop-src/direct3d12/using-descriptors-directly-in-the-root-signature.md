---
title: Utilisation des descripteurs directement dans la signature racine
description: Les applications peuvent placer des descripteurs directement dans la signature racine pour éviter d’avoir à passer par un tas de descripteur.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd97a7d68f5c9b51b6d15d3b71c6e30d04bb36e5
ms.sourcegitcommit: 83afb2f3e9e5d37f3f5a11e975515e9ed8b044ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2020
ms.locfileid: "104548598"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a><span data-ttu-id="f6efe-103">Utilisation des descripteurs directement dans la signature racine</span><span class="sxs-lookup"><span data-stu-id="f6efe-103">Using descriptors directly in the root signature</span></span>

<span data-ttu-id="f6efe-104">Les applications peuvent placer des descripteurs directement dans la signature racine pour éviter d’avoir à passer par un tas de descripteur.</span><span class="sxs-lookup"><span data-stu-id="f6efe-104">Applications can put descriptors directly in the root signature to avoid having to go through a descriptor heap.</span></span> <span data-ttu-id="f6efe-105">Ces descripteurs occupent beaucoup d’espace dans la signature racine (voir la section limites de signature racine), de sorte que les applications doivent les utiliser avec modération.</span><span class="sxs-lookup"><span data-stu-id="f6efe-105">These descriptors take a lot of space in the root signature (see the root signature limits section), so applications have to use them sparingly.</span></span>

<span data-ttu-id="f6efe-106">Un exemple d’utilisation consiste à placer des vues de mémoire tampon constante (CBV) qui changent par dessin dans la disposition racine afin que l’espace du tas de descripteurs ne doit pas être alloué par l’application par dessin (et qu’il ne soit pas possible de l’enregistrer en pointant sur une table de descripteur au nouvel emplacement dans le tas du descripteur).</span><span class="sxs-lookup"><span data-stu-id="f6efe-106">An example usage would be to place a constant buffer views (CBV) that is changing per draw in the root layout so that descriptor heap space doesn't have to be allocated by the application per draw (and save pointing a descriptor table at the new location in the descriptor heap).</span></span> <span data-ttu-id="f6efe-107">En plaçant un texte dans la signature racine, l’application confie simplement la responsabilité du contrôle de version au pilote, mais il s’agit d’une infrastructure dont ils disposent déjà.</span><span class="sxs-lookup"><span data-stu-id="f6efe-107">By putting something in the root signature, the application is merely handing the versioning responsibility to the driver, but this is infrastructure that they already have.</span></span>

<span data-ttu-id="f6efe-108">Dans le cas d’un rendu qui utilise très peu de ressources, l’utilisation des tables ou des tas de descripteurs peut ne pas être nécessaire du tout si tous les descripteurs nécessaires peuvent être placés directement dans la signature racine.</span><span class="sxs-lookup"><span data-stu-id="f6efe-108">For rendering that uses extremely few resources, descriptor table/heap use may not be needed at all if all the needed descriptors can be placed directly in the root signature.</span></span>

<span data-ttu-id="f6efe-109">Les seuls types de descripteurs pris en charge dans la signature racine sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="f6efe-109">The only types of descriptors supported in the root signature are:</span></span>
- <span data-ttu-id="f6efe-110">CBVs.</span><span class="sxs-lookup"><span data-stu-id="f6efe-110">CBVs.</span></span>
- <span data-ttu-id="f6efe-111">Les vues des ressources de nuanceur (SRVs)/unordered Access views (UAVs) des ressources de mémoire tampon où le format SRV/UAV contient uniquement des composants 32 bits FLOAT/UINT/Saint (il n’y a pas de conversion de format).</span><span class="sxs-lookup"><span data-stu-id="f6efe-111">Shader Resource Views (SRVs)/Unordered Access Views (UAVs) of buffer resources where the SRV/UAV format contains only 32 bit FLOAT/UINT/SINT components (there is no format conversion).</span></span>
- <span data-ttu-id="f6efe-112">SRVs de structures d’accélération Raytracing, dans les signatures racines locales ou globales.</span><span class="sxs-lookup"><span data-stu-id="f6efe-112">SRVs of raytracing acceleration structures, in local or global root signatures.</span></span> 

<span data-ttu-id="f6efe-113">Les UAVs dans la racine ne peuvent pas être associés à des compteurs.</span><span class="sxs-lookup"><span data-stu-id="f6efe-113">UAVs in the root cannot have counters associated with them.</span></span> <span data-ttu-id="f6efe-114">Les descripteurs dans la signature racine apparaissent chacun sous forme de descripteurs distincts, &mdash; mais ils ne peuvent pas être indexés de manière dynamique.</span><span class="sxs-lookup"><span data-stu-id="f6efe-114">Descriptors in the root signature appear each as individual separate descriptors&mdash;they cannot be dynamically indexed.</span></span>

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

<span data-ttu-id="f6efe-115">Dans l’exemple ci-dessus, `mySceneData` ne peut pas être déclaré en tant que tableau, comme dans `cbuffer mySceneData[2]` s’il va être mappé à un descripteur dans la signature racine, puisque l’indexation entre les descripteurs n’est pas prise en charge dans la signature racine.</span><span class="sxs-lookup"><span data-stu-id="f6efe-115">In the above example, `mySceneData` cannot be declared as an array, as in `cbuffer mySceneData[2]` if it is going to be mapped onto a descriptor in the root signature, since indexing across descriptors is not supported in the root signature.</span></span> <span data-ttu-id="f6efe-116">L’application peut définir des tampons de constante individuels distincts et les définir comme une entrée distincte dans la signature racine, si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="f6efe-116">The application can define separate individual constant buffers and define them each as a separate entry in the root signature if desired.</span></span> <span data-ttu-id="f6efe-117">Notez que, dans le `mySceneData` cas ci-dessus, il existe un tableau `bar[2]` .</span><span class="sxs-lookup"><span data-stu-id="f6efe-117">Note that within `mySceneData` above, there is an array `bar[2]`.</span></span> <span data-ttu-id="f6efe-118">L’indexation dynamique dans la mémoire tampon constante est valide : un descripteur dans la signature racine se comporte de la même manière que le même descripteur, s’il est accessible via un tas de descripteur.</span><span class="sxs-lookup"><span data-stu-id="f6efe-118">Dynamic indexing within the constant buffer is valid - a descriptor in the root signature behaves just like the same descriptor would behave if accessed through a descriptor heap.</span></span> <span data-ttu-id="f6efe-119">Cela est différent avec les constantes d’incorporation directement dans la signature racine, qui apparaît également comme une mémoire tampon constante, sauf si la contrainte stipule que l’indexation dynamique dans les constantes inline n’est pas autorisée, ce qui n’est `bar[2]` pas autorisé ici.</span><span class="sxs-lookup"><span data-stu-id="f6efe-119">This is in contrast with inlining constants directly in the root signature, which also appears like a constant buffer except with the constraint that dynamic indexing within the inlined constants is not permitted, so `bar[2]` would not be allowed there.</span></span>

<span data-ttu-id="f6efe-120">Les API suivantes (à partir de l’interface [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) servent à définir des descripteurs directement sur la signature racine :</span><span class="sxs-lookup"><span data-stu-id="f6efe-120">The following APIs (from the [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface) are for setting descriptors directly on the root signature:</span></span>

-   [<span data-ttu-id="f6efe-121">**SetComputeRootConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="f6efe-121">**SetComputeRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [<span data-ttu-id="f6efe-122">**SetGraphicsRootConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="f6efe-122">**SetGraphicsRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [<span data-ttu-id="f6efe-123">**SetComputeRootShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="f6efe-123">**SetComputeRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [<span data-ttu-id="f6efe-124">**SetGraphicsRootShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="f6efe-124">**SetGraphicsRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [<span data-ttu-id="f6efe-125">**SetComputeRootUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="f6efe-125">**SetComputeRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [<span data-ttu-id="f6efe-126">**SetGraphicsRootUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="f6efe-126">**SetGraphicsRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!Note]  
> <span data-ttu-id="f6efe-127">Il n’existe aucun concept de « tableau de descripteur racine » dans Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="f6efe-127">There is no concept of a "root descriptor array" in Direct3D 12.</span></span> <span data-ttu-id="f6efe-128">Les tableaux de descripteurs sont pris en charge uniquement dans les tas de descripteurs.</span><span class="sxs-lookup"><span data-stu-id="f6efe-128">Descriptor arrays are only supported in descriptor heaps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6efe-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6efe-129">Related topics</span></span>

[<span data-ttu-id="f6efe-130">Signatures racines</span><span class="sxs-lookup"><span data-stu-id="f6efe-130">Root Signatures</span></span>](root-signatures.md)
