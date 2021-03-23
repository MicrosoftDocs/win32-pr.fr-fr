---
title: Utilisation de tables de descripteurs
description: Les tables de descripteurs, chacune identifiant une plage dans un tas de descripteur, sont liées aux emplacements définis par la signature racine actuelle dans une liste de commandes.
ms.assetid: 4ECEC07A-7ABC-4C5F-B23C-36F0D92643FE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e589274fbb93e48e4d65e545a62999e654b7688f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104614"
---
# <a name="using-descriptor-tables"></a><span data-ttu-id="be998-103">Utilisation de tables de descripteurs</span><span class="sxs-lookup"><span data-stu-id="be998-103">Using Descriptor Tables</span></span>

<span data-ttu-id="be998-104">Les tables de descripteurs, chacune identifiant une plage dans un tas de descripteur, sont liées aux emplacements définis par la signature racine actuelle dans une liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="be998-104">Descriptor tables, each identifying a range in a descriptor heap, are bound at slots defined by the current root signature on a command list.</span></span>

-   [<span data-ttu-id="be998-105">Indexation des tables de descripteurs</span><span class="sxs-lookup"><span data-stu-id="be998-105">Indexing Descriptor Tables</span></span>](#indexing-descriptor-tables)
-   [<span data-ttu-id="be998-106">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be998-106">Related topics</span></span>](#related-topics)

<span data-ttu-id="be998-107">Les nuanceurs peuvent localiser les ressources référencées par les descripteurs qui composent la table du descripteur.</span><span class="sxs-lookup"><span data-stu-id="be998-107">Shaders can locate resources referenced by the descriptors that make up the descriptor table.</span></span> <span data-ttu-id="be998-108">D’autres liaisons de ressources-tampons d’index, tampons de vertex, mémoires tampons de sortie de flux, cibles de rendu et stencil de profondeur sont effectués directement sur une liste de commandes plutôt que via des descripteurs.</span><span class="sxs-lookup"><span data-stu-id="be998-108">Other resource bindings - Index Buffers, Vertex Buffer, Stream Output Buffers, Render Targets, and Depth Stencil are done directly on a command list rather than via descriptors.</span></span> <span data-ttu-id="be998-109">Pour récapituler :</span><span class="sxs-lookup"><span data-stu-id="be998-109">To summarize:</span></span>

<span data-ttu-id="be998-110">Les références de ressources suivantes peuvent partager les mêmes table de descripteur et tas :</span><span class="sxs-lookup"><span data-stu-id="be998-110">The following resource references can share the same descriptor table and heap:</span></span>

-   <span data-ttu-id="be998-111">Affichages des ressources de nuanceur</span><span class="sxs-lookup"><span data-stu-id="be998-111">Shader resource views</span></span>
-   <span data-ttu-id="be998-112">Vues d’accès non ordonnées</span><span class="sxs-lookup"><span data-stu-id="be998-112">Unordered access views</span></span>
-   <span data-ttu-id="be998-113">Vues de mémoire tampon constantes</span><span class="sxs-lookup"><span data-stu-id="be998-113">Constant buffer views</span></span>

<span data-ttu-id="be998-114">Les références de ressources suivantes doivent être dans leur propre tas de descripteur :</span><span class="sxs-lookup"><span data-stu-id="be998-114">The following resource references must be in their own descriptor heap:</span></span>

-   <span data-ttu-id="be998-115">Échantillonneurs</span><span class="sxs-lookup"><span data-stu-id="be998-115">Samplers</span></span>

<span data-ttu-id="be998-116">Les ressources suivantes ne sont pas placées dans les tables de descripteurs ou les segments de mémoire, mais sont directement liées à l’aide de listes de commandes :</span><span class="sxs-lookup"><span data-stu-id="be998-116">The following resources are not placed in descriptor tables or heaps, but are bound directly using command lists:</span></span>

-   <span data-ttu-id="be998-117">Mémoires tampons d’index</span><span class="sxs-lookup"><span data-stu-id="be998-117">Index buffers</span></span>
-   <span data-ttu-id="be998-118">Mémoires tampons de vertex</span><span class="sxs-lookup"><span data-stu-id="be998-118">Vertex buffers</span></span>
-   <span data-ttu-id="be998-119">Mémoires tampons de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="be998-119">Stream output buffers</span></span>
-   <span data-ttu-id="be998-120">Cibles de rendu</span><span class="sxs-lookup"><span data-stu-id="be998-120">Render targets</span></span>
-   <span data-ttu-id="be998-121">Vues du stencil de profondeur</span><span class="sxs-lookup"><span data-stu-id="be998-121">Depth stencil views</span></span>

## <a name="indexing-descriptor-tables"></a><span data-ttu-id="be998-122">Indexation des tables de descripteurs</span><span class="sxs-lookup"><span data-stu-id="be998-122">Indexing Descriptor Tables</span></span>

<span data-ttu-id="be998-123">Les nuanceurs ne peuvent pas indexer dynamiquement entre les limites des tables de descripteurs à partir d’un site d’appel donné dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="be998-123">Shaders cannot dynamically index across descriptor table boundaries from a given call-site in the shader.</span></span> <span data-ttu-id="be998-124">Toutefois, la sélection d’un descripteur au sein d’une table de descripteur peut être indexée dynamiquement dans le code du nuanceur dans des plages du même type de descripteur (telles que l’indexation dans une région contiguë de SRVs).</span><span class="sxs-lookup"><span data-stu-id="be998-124">However, the selection of a descriptor within a descriptor table is allowed to be dynamically indexed in shader code within ranges of the same descriptor type (such as indexing across a contiguous region of SRVs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="be998-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be998-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be998-126">Tables de descripteurs</span><span class="sxs-lookup"><span data-stu-id="be998-126">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> </dl>

 

 




